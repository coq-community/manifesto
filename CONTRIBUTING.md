# Contributing guide #

This is a shared contributing guide applying to all the projects of
coq-community, including this meta-project.

*Note this contributing guide itself is a work in progress and is meant to be
collaboratively improved. Please contribute!*

## Proposing a new package ##

[Open a new issue using the appropriate template][move_project].
Fill in the requested information. In particular here are some requirements to
move a project to coq-community:

- The project must have a license that is either
  [approved as an open source license by OSI][osi-approved-license]
  or [considered a free software license by FSF][fsf-free-software-license]
  (non-commercial / academic licenses are not acceptable).
- The main authors of the package must either consent to this move or be
  completely unresponsive. Therefore, once a project is proposed, we will
  open an issue at the original project URL (or send an e-mail when this
  option is not available) to try to get consent or at least confirm the
  unresponsiveness.
- We must find a volunteer to become the official maintainer. When
  packages are proposed without a volunteer maintainer, the corresponding
  issue will be labeled as looking for a maintainer until it finds one.

## Contributing to a coq-community package ##

- Report bugs on the specific project's issue tracker. Include as many details
  as possible (version of the package and how you installed it, version of Coq,
  version of OCaml if you built the package yourself...).

- Propose changes by submitting a pull request. This implies that you accept to
  put your contribution under the project's license. If the change is a large
  one, consider opening an issue first to get an idea whether your change is
  likely to be accepted.

  If you are working on a bug fix, report the bug first and self-assign the issue
  (you need to be part of the coq-community organization to self-assign an issue,
  if you are not you may still post a comment saying you are working on this).

  If you have time on your hands but don't know what to work on, have a look
  at [this list of coq-community issues where external help was requested][help-wanted].

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

Templates for setting up CI, an OPAM file, etc., [are available][templates]
and advice and guidelines on how to maintain a project may be found in the
[wiki](https://github.com/coq-community/manifesto/wiki).

## Contributing to this meta-project ##

The processes and policies of coq-community are very much a work in progress.
Always feel free to [open a meta-issue][meta] or a pull request to propose
some improvements, discuss some policies, etc.

Opening a pull request on this meta-project implies that you accept to put
your contribution under the CC0 license: see [`LICENSE.md`](LICENSE.md).

[move_project]: https://github.com/coq-community/manifesto/issues/new?labels=move-project&template=1-move-a-project.md&title=Proposal+to+move+project+X+to+coq-community

[osi-approved-license]: https://opensource.org/licenses/alphabetical

[fsf-free-software-license]: https://www.gnu.org/licenses/license-list.html

[change_maintainer]: https://github.com/coq-community/manifesto/issues/new?labels=change-maintainer&template=2-change-maintainer.md&title=Change+maintainer+of+project+X

[meta]: https://github.com/coq-community/manifesto/issues/new?labels=meta&template=3-meta.md

[templates]: https://github.com/coq-community/templates

[help-wanted]: https://github.com/issues?q=is%3Aopen+is%3Aissue+archived%3Afalse+user%3Acoq-community+label%3A%22help+wanted%22
