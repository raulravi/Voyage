.PHONY: default all build clean compile release shell powershell tar

rebar='./rebar3'

default: compile
all: clean compile test
build: test release
compile:
	@$(rebar) compile
clean:
	@$(rebar) clean
cleanall:
	@$(rebar) clean -a
test:
	@$(rebar) do ct,cover,dialyzer
release:
	@$(rebar) release
shell:
	@$(rebar) shell
run:
	@$(rebar) run
tar:
	@$(rebar) as prod tar
