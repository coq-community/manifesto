# Contributing guide #

This is a shared contributing guide applying to all the projects of
coq-community, including this meta-project.

*Note this contributing guide itself is a work in progress and is meant to be
collaboratively improved. Please contribute!*

## Proposing a new package ##

[Open a new issue using the appropriate template][move_project].
Fill in the requested information. In particular here are some requirements to
move a project to coq-community:

- The project must have an open source license (non-commercial / academic
  licenses are not acceptable).
- The main authors of the package must either consent to this move or be
  completely unresponsive. Therefore, once a project is proposed, we will
  open an issue at the original project URL (or send an e-mail when this
  option is not available) to try to get consent or at least confirm the
  unresponsiveness. Projects that are currently part of
  [coq-contribs](https://github.com/coq-contribs) do not require this step.
- We must find a volunteer to become the official maintainer. When
  packages are proposed without a volunteer maintainer, the corresponding
  issue will be labelled as looking for a maintainer until it finds one.

## Contributing to a coq-community package ##

Report bugs on the specific project's issue tracker. Include as many details
as possible (version of the package and how you installed it, version of Coq,
version of OCaml if you built the package yourself...).

Propose changes by submitting a pull request. This implies that you accept to
put your contribution under the project's license. If the change is a large
one, consider opening an issue first to get an idea whether your change is
likely to be accepted.

If you are working on a bug fix, report the bug first and self-assign the issue
(you need to be part of the coq-community organization to self-assign an issue,
if you are not you may still post a comment saying you are working on this).

## Maintaining a coq-community package ##

As a maintainer, your main role is to handle incoming pull requests (review and
merge them) and to make sure that incoming issues are not left without answer
(even if you don't have to fix them). You may delegate part of this role to
secondary maintainers.

If you are unresponsive and there are no secondary maintainers, maintainers of
other coq-community projects may act as secondary maintainers. If you are
unresponsive really often or if you wish to step down, you may be replaced by
a new maintainer.

To replace a maintainer,
[open a new issue using the appropriate template][change_maintainer].

## Contributing to this meta-project ##

The processes and policies of coq-community are very much a work in progress.
Always feel free to [open a meta-issue][meta] or a pull request to propose
some improvements, discuss some policies, etc.

Opening a pull request on this meta-project implies that you accept to put
your contribution under the CC0 license: see [`LICENSE.md`](LICENSE.md).

[move_project]: https://github.com/coq-community/manifesto/issues/new?template=move_project.md
[change_maintainer]: https://github.com/coq-community/manifesto/issues/new?template=change_maintainer.md
[meta]: https://github.com/coq-community/manifesto/issues/new?template=meta.md
