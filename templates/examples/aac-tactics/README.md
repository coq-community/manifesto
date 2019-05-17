# AAC Tactics

[![Travis][travis-shield]][travis-link]
[![Contributing][contributing-shield]][contributing-link]
[![Code of Conduct][conduct-shield]][conduct-link]
[![Gitter][gitter-shield]][gitter-link]
[![DOI][doi-shield]][doi-link]

[travis-shield]: https://travis-ci.com/coq-community/aac-tactics.svg?branch=master
[travis-link]: https://travis-ci.com/coq-community/aac-tactics/builds

[contributing-shield]: https://img.shields.io/badge/contributions-welcome-%23f7931e.svg
[contributing-link]: https://github.com/coq-community/manifesto/blob/master/CONTRIBUTING.md

[conduct-shield]: https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-%23f15a24.svg
[conduct-link]: https://github.com/coq-community/manifesto/blob/master/CODE_OF_CONDUCT.md

[gitter-shield]: https://img.shields.io/badge/chat-on%20gitter-%23c1272d.svg
[gitter-link]: https://gitter.im/coq-community/Lobby

[doi-shield]: https://zenodo.org/badge/DOI/10.1007/978-3-642-25379-9_14.svg
[doi-link]: https://doi.org/10.1007/978-3-642-25379-9_14

This Coq plugin provides tactics for rewriting universally quantified
equations, modulo associativity and commutativity of some operator.
The tactics can be applied for custom operators by registering the
operators and their properties as type class instances. Many common
operator instances, such as for Z binary arithmetic and booleans, are
provided with the plugin.


More details about the project can be found in the paper
[Tactics for Reasoning modulo AC in Coq](https://arxiv.org/abs/1106.4448).

## Meta

- Author(s):
  - Thomas Braibant (initial)
  - Damien Pous (initial)
  - Fabian Kunze
- Coq-community maintainer(s):
  - Fabian Kunze ([**@fakusb**](https://github.com/fakusb))
  - Karl Palmskog ([**@palmskog**](https://github.com/palmskog))
- License: [GNU Lesser General Public License v3.0 or later](LICENSE)
- Compatible Coq versions: master (use the corresponding branch or release for other Coq versions)
- Compatible OCaml versions: all versions supported by Coq
- Additional Coq dependencies: none

## Building and installation instructions

The easiest way to install the latest released version of AAC Tactics
is via [OPAM](https://opam.ocaml.org/doc/Install.html):

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

After installation, the included modules are available under
the `AAC_tactics` namespace.


## Documentation

The following example shows an application of the tactics for reasoning over Z binary numbers:
```coq
Require Import AAC_tactics.AAC.
Require AAC_tactics.Instances.
Require Import ZArith.

Section ZOpp.
  Import Instances.Z.
  Variables a b c : Z.
  Hypothesis H: forall x, x + Z.opp x = 0.

  Goal a + b + c + Z.opp (c + a) = b.
    aac_rewrite H.
    aac_reflexivity.
  Qed.
End ZOpp.
```

The file [Tutorial.v](theories/Tutorial.v) provides a succinct introduction
and more examples of how to use this plugin.

The file [Instances.v](theories/Instances.v) defines several type class instances
for frequent use-cases of this plugin, that should allow you to use it off-the-shelf.
Namely, it contains instances for:

- Peano naturals	(`Import Instances.Peano.`)
- Z binary numbers	(`Import Instances.Z.`)
- N binary numbers	(`Import Instances.N.`)
- P binary numbers	(`Import Instances.P.`)
- Rational numbers	(`Import Instances.Q.`)
- Prop			(`Import Instances.Prop_ops.`)
- Booleans		(`Import Instances.Bool.`)
- Relations		(`Import Instances.Relations.`)
- all of the above	(`Import Instances.All.`)

To understand the inner workings of the tactics, please refer to
the `.mli` files as the main source of information on each `.ml` file.

## Acknowledgements

The initial authors are grateful to Evelyne Contejean, Hugo Herbelin,
Assia Mahboubi, and Matthieu Sozeau for highly instructive discussions.
The plugin took inspiration from the plugin tutorial "constructors" by
Matthieu Sozeau, distributed under the LGPL 2.1.

