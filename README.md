[![Gitter chat](https://badges.gitter.im/gitterHQ/gitter.png)][gitter]
[![Code of Conduct](https://img.shields.io/badge/%E2%9D%A4-code%20of%20conduct-blue.svg?style=flat)](CODE_OF_CONDUCT.md)

# coq-community #

A project for a collaborative, community-driven effort for the long-term
maintenance and advertisement of Coq packages.

*Note that this README (the manifesto) is a work in progress and is meant to be
collaboratively improved. Please contribute!*

## Who runs this organization? ##

This organization is run by volunteer Coq users. Everyone is welcome
(you don't need to be a very experimented Coq user to participate).
Please [get involved](CONTRIBUTING.md)!

## What are its goals? ##

### Providing a place to maintain packages that were left over by their author ###

*This is the main objective in the first phase of the coq-community effort.*

Unmaintained packages that are raising enough interest (either because they are
libraries or plugins with many users, or because they represent interesting
mathematical proofs or nice achievements) can be taken over by coq-community.

Each project under the umbrella of coq-community has an official maintainer
but the maintenance effort is done collaboratively. Users need not be afraid
of volunteering to be the official maintainer of a coq-community project
because they can step down at anytime. Changing the maintainer of a
coq-community project can be done very easily without the hassle of moving its
location too. That's why it can also make sense for a project which is actively
maintained but not actively developed to move to coq-community.

Maintenance is allowed to go much further than just updating the package to
keep it compiling with newer Coq versions. It can also include refactorization
of the code, uniformization of the style, merging with other packages, taking
pieces out to put them in other libraries, and even removal of some parts that
are not raising sufficient interest. These changes must, nonetheless, always be
done with consideration for compatibility as soon as the package is a library
or plugin that has users.

*The following two objectives will be addressed as part of a second phase of the coq-community effort.*

### Collaborative writing of documentation ###

Some Coq proofs present a particular pedagogical interest because their
statements are easy to understand, but they require some non-trivial
mathematical tools and their mechanization illustrates interesting proof
patterns, or demonstrate the use of specific libraries. They could be used as
the basis for tutorials which explain the tricks and interesting parts.
Gathering such packages and their documentation could give rise to a new,
interactive “book” that would target advanced Coq learners.

### Advertising interesting packages ###

Not all the packages that will be taken over will be of the same initial
quality. While this should not stop packages from being taken over, and new
maintainers should strive to improve the package quality, some editorial work
will be also required to put forward the most interesting packages, be it for
their usefulness as a library or plugin, because they demonstrate interesting
proof techniques, or because they represent an important achievement.

This work will be done by an editorial board which will be constituted of
experimented users and prominent members of the Coq community. They will have
to decide what packages to put forward and on what criteria to take these
decisions. The editorial board will also oversee the collaborative writing of
documentation.

## FAQ ##

- **What is the difference with coq-contribs?**

  Coq's *contribs* started out as a distribution method: the Coq development
  team encouraged people to submit their projects as a contrib, then all such
  contribs would be distributed to all users, as a big archive.
  It had two nice side-effects: the Coq development team would maintain
  these contribs to ensure that they kept compiling with the most recent
  versions of Coq; moreover doing this maintenance work would give them an idea
  of the impact of their compatibility breaking changes to Coq.

  Then, under the impulse of Thomas Braibant, Coq started using OPAM, the OCaml
  package manager, to deliver contribs to users.
  This allowed for a distributed maintenance model where developers of Coq
  packages could maintain their packages on their own, while continuing to
  reach users easily.

  Since then, [Continuous Integration has been put in place in the Coq repository][Coq-CI],
  and it does not depend on contribs anymore, while giving a better assessment
  of the impact of compatibility breaking changes.

  The webform to submit new contribs was eventually taken down, and only the
  long-term maintenance of contribs by the Coq development team has not found
  any replacement mechanism. This is this role that coq-community intends to
  take. That's why contribs are good candidates to join coq-community.

- **What is the relation with the Coq package index?**

  The [Coq package index](https://coq.inria.fr/packages) is the present
  OPAM-based way of distributing Coq packages. As such, all projects of
  coq-community will have a corresponding package in the Coq package index.

- **What is the difference with the Coq plugin developer program?**

  The Coq plugin developer program doesn't exist yet but it's a project to have
  a community of Coq plugin developers to discuss best practices, how to
  correctly use the Coq API, etc. Whenever this program is finally introduced,
  it will make sense for coq-community plugins to also be part of this
  program.

- **Can I propose a project of which I am the author?**

  Yes, you can propose a project of which you are the author, as a way of
  preparing to pass on the maintenance to other community members. You can
  start up by proposing yourself as the primary maintainer for this project;
  but if you become less available for this task, we'll be able to pass on this
  role to someone else.

- **Will all the projects of coq-community have some Continous Integration (CI) setup?**

  Yes, CI plays a big role in keeping code projects more stable over time. In
  the case of a Coq package, it helps to ensure that the project stays
  compatible with the various versions of Coq that are claimed to be supported
  (as well as various versions of OCaml in the case of a Coq plugin).

- **Which versions of Coq must be supported by projects of coq-community?**

  At least the last stable version of Coq must be supported at any given time.
  Support for older versions or the development version of Coq can be decided
  project by project. Note that supporting the development version of Coq is
  a requirement to get into [Coq's CI][Coq-CI], which can be interesting to get
  patches from Coq developers when they introduce a breaking change.

- **How to remove a package?**

  When a package loses its interest because a newer, better alternative has
  been found, or for some other reason, the package can be marked as deprecated
  and stop being maintained. We will generally [archive][archive] the
  repository rather than removing it completely though.

- **What to do in case of conflicts?**

  We will have a governance process to make sure that we can handle conflicts
  that are bound to arise about the management of specific projects. Please
  contribute to [meta-issue #2](https://github.com/coq-community/manifesto/issues/2)
  which is about this.

- **Why wait for a second phase of the project for the second and the third objectives?**

  We want to attract experimented users and prominent members of the Coq
  community to form the editorial board. Because these people are usually very
  busy, being able to show them that the organization is already active will
  help convince them to join the board. If you are already interested in
  joining this board, please let us know at theo@irif.fr and
  pierre.casteran@labri.fr.

  Furthermore, we will propose a format for the documentation packages based
  on a preliminary work by Pierre Castéran.

- **Why this name?**

  The coq-community organization takes its inspiration from the similar-named
  [elm-community](https://github.com/elm-community).

Is anything still unclear? Please [open an issue][meta] or
[go to our Gitter room][gitter] to ask a question.

[archive]: https://github.com/coq-community?utf8=%E2%9C%93&q=&type=archived

[Coq-CI]: https://github.com/coq/coq/blob/master/dev/ci/README.md

[gitter]: https://gitter.im/coq-community/Lobby

[meta]: https://github.com/coq-community/manifesto/issues/new?template=meta.md
