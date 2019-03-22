This directory contains a few reusable files for coq-community (or external)
Coq projects.

Files ending with `.mustache` have values to fill in to use (and the
`.mustache` extension should be removed).

This can (and should) be done automatically using a mustache command-line (many
`mustache` implementations are available from <https://mustache.github.io/>).
To do so, you must write a `meta.yml` file containing the requested values.
For instance, the files in the [`examples/`](examples/) sub-directories were generated in the
following way:

``` shell
for dir in examples/*; do
  for f in default.nix.mustache README.md.mustache .travis.yml.mustache; do
    mustache $dir/meta.yml $f > $dir/${f%.mustache} && \
    echo "$dir/${f%.mustache}"
  done
  mustache $dir/meta.yml coq.opam.mustache > $dir/coq-${dir#examples/}.opam && \
  echo "$dir/coq-${dir#examples/}.opam"
done
```
You may find documentation, advice and guidelines on how to maintain a project
in the [wiki](https://github.com/coq-community/manifesto/wiki).
