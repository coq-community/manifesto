include ../Makefile.common

all: README.md default.nix coq-chapar.opam coq-chapar-stores.opam

coq-chapar-stores.opam: meta.yml $(TEMPLATES)/extracted.opam.mustache
	mustache $^ > $@
