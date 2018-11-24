# Overloaded lemmas

[![Travis][travis-shield]][travis-link]
[![Contributing][contributing-shield]][contributing-link]
[![Code of Conduct][conduct-shield]][conduct-link]
[![Gitter][gitter-shield]][gitter-link]

[travis-shield]: https://travis-ci.com/coq-community/lemma-overloading.svg?branch=master
[travis-link]: https://travis-ci.com/coq-community/lemma-overloading/builds

[contributing-shield]: https://img.shields.io/badge/contributions-welcome-%23f7931e.svg
[contributing-link]: https://github.com/coq-community/manifesto/blob/master/CONTRIBUTING.md

[conduct-shield]: https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-%23f15a24.svg
[conduct-link]: https://github.com/coq-community/manifesto/blob/master/CODE_OF_CONDUCT.md

[gitter-shield]: https://img.shields.io/badge/chat-on%20gitter-%23c1272d.svg
[gitter-link]: https://gitter.im/coq-community/Lobby

This project contains Hoare Type Theory libraries from
[How to make ad hoc proof automation less ad hoc][paper] paper.

The project presents a series of design patterns for *canonical structure*
programming that enable one to carefully and predictably coax Coq’s type
inference engine into triggering the execution of user-supplied algorithms
during unification, and illustrates these patterns through several realistic
examples drawn from Hoare Type Theory. The project also contains a
typeclasses-based re-implementation for comparison.

[paper]: https://software.imdea.org/~aleks/papers/lessadhoc/journal.pdf


## Meta

- Initial author(s):
  - Georges Gonthier
  - Beta Ziliani
  - Aleksandar Nanevski
  - Derek Dreyer
- Coq-community maintainer(s):
  - Anton Trunov ([**@anton-trunov**](https://github.com/anton-trunov))
- License: [GNU General Public License v3](LICENSE.md)
- Compatible Coq versions: Coq 8.8 or greater
- Additional dependencies:
  - Mathcomp 1.6.2 or greater (mathcomp/ssreflect package suffices)


## Building and installation instructions

The easiest way to install the latest released version is via
[OPAM](https://opam.ocaml.org/doc/Install.html):

```shell
opam repo add coq-released https://coq.inria.fr/opam/released
opam install coq-lemma-overloading
```

To instead build and install manually, do:

``` shell
git clone https://github.com/coq-community/lemma-overloading
cd lemma-overloading
make   # or make -j <number-of-cores-on-your-machine>
make install
```

After installation, the included modules are available under
the `LemmaOverloading` namespace.


