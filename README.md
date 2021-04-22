# Verified Programming of Turing Machines in Coq

This repository accompanies the paper [Verified Programming of Turing Machines in Coq](https://dl.acm.org/doi/abs/10.1145/3372885.3373816) by Yannick Forster, Fabian Kunze, and Maximilian Wuttke, which appeared at the [CPP 2019 - The 8th ACM SIGPLAN International Conference on Certified Programs and Proofs](https://popl19.sigplan.org/track/CPP-2019). The paper can also be found [here](https://www.ps.uni-saarland.de/Publications/documents/ForsterEtAl_2019_VerifiedTMs.pdf).

The repository is a static fork of the [Coq Library of Undecidability Proofs](https://github.com/uds-psl/coq-library-undecidability).

## How to build

### Required packages

You need `Coq 8.8.1` or `8.8.2` built on OCAML `> 4.02.3` and the [Equations](https://mattam82.github.io/Coq-Equations/) package for Coq. If you're using opam 2 you can use the following commands to install the dependencies on a new switch:

```
opam switch create coq-library-undecidability 4.07.1+flambda
eval $(opam env)
opam install . --deps-only
```

### Build external libraries

The Undecidability libraries depends on several external libraries. Initialise and build them once as follows:

``` sh
git submodule init
git submodule update
make deps
```

### Building the undecidability library

- `make all` builds the library
- `make html` generates clickable coqdoc `.html` in the `website` subdirectory
- `make clean` removes all build files in `theories` and `.html` files in the `website` directory
- `make realclean` also removes all build files in the `external` directory. You have to run `make deps` again after this.

