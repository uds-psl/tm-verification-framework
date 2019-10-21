# Verified Programming of Turing Machines in Coq

This repository contains the Coq formalisation of the paper "Verified Programming of Turing Machines in Coq". As it is meant to be integrated into a larger project, this project contain much unrelated code.

The code for this paper  paper is in theories/TM. 


## How to compile the code

Assuming coq is installed with `opam`, necessary dependencies need to be installed by 


``` sh
opam install coq-equations.1.2+8.8 coq-metacoq.1.0~alpha+8.8

```

Then , the project can be build by calling `make -j 5`.
