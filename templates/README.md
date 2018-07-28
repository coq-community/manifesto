This directory contains a few reusable files for coq-community (or external)
Coq projects.

Files ending with `.mustache` have values to fill in to use (and the
`.mustache` extension should be removed).

This can even be done automatically using a mustache command-line (many
`mustache` implementations are available from <https://mustache.github.io/>).
To do so, you must write a `.yml` file containing the requested values, for
instance:

``` shell
for f in *.mustache; do
  mustache lemma-overloading.yml $f > /tmp/${f%.mustache} && \
  echo "/tmp/${f%.mustache}"
done
```
