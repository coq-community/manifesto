# AAC tactics

[![Travis][travis-shield]][travis-link]
[![Contributing][contributing-shield]][contributing-link]
[![Code of Conduct][conduct-shield]][conduct-link]
[![Gitter][gitter-shield]][gitter-link]

[travis-shield]: https://travis-ci.com/coq-community/aac-tactics.svg?branch=master
[travis-link]: https://travis-ci.com/coq-community/aac-tactics/builds

[contributing-shield]: https://img.shields.io/badge/contributions-welcome-%23f7931e.svg
[contributing-link]: https://github.com/coq-community/manifesto/blob/master/CONTRIBUTING.md

[conduct-shield]: https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-%23f15a24.svg
[conduct-link]: https://github.com/coq-community/manifesto/blob/master/CODE_OF_CONDUCT.md

[gitter-shield]: https://img.shields.io/badge/chat-on%20gitter-%23c1272d.svg
[gitter-link]: https://gitter.im/coq-community/Lobby

This Coq plugin provides tactics for rewriting universally quantified
equations, modulo associativity and commutativity of some operator.

The tactics can be applied for custom operators by registering the
operators and their properties as type class instances. Many common
operator instances, such as for Z binary arithmetic and booleans, are
provided with the plugin.

The implementation and underlying theory is decribed in the paper
[Tactics for Reasoning modulo AC in Coq](https://arxiv.org/abs/1106.4448).


## Meta

- Initial author(s):
  - Thomas Braibant
  - Damien Pous
- Coq-community maintainer(s):
  - [Fabian Kunze](https://github.com/fakusb) (**@fakusb**)
  - [Karl Palmskog](https://github.com/palmskog) (**@palmskog**)
- License: [GNU Lesser General Public License v3](LICENSE)
- Compatible Coq versions: Coq master (use the corresponding branch or release for other Coq versions)
- Compatible OCaml versions: all versions supported by Coq
- Additional dependencies: none

## Building and installation instructions

The easiest way to install the latest released version is via
[OPAM](https://opam.ocaml.org/doc/Install.html):

```shell
opam repo add coq-released https://coq.inria.fr/opam/released
opam install coq-aac-tactics
```

To instead build and install manually, do:

``` shell
git clone https://github.com/coq-community/aac-tactics
cd aac-tactics
make   # or make -j <number-of-cores-on-your-machine>
make install
```

After installation, the various modules from [`theories/`](theories/) are
available under the `AAC_tactics` namespace.

