# Meta

## Commits Messages

Commit Messages follow [`Conventional Commits`], but with custom types and
scopes as those defined in the spec are useful for development, but less so for
notes.

- types
  - `init`: initialization of the project
  - `doc`: some added/changed documentation
    - note that docs might also added as part of a bigger change to not split
      documentation and the change it entails
- scopes
  - `readme`: changes of the readme (likely as part of `doc(readme)`)

[`Conventional Commits`]: https://www.conventionalcommits.org/en/v1.0.0/

## Todo: Commit Messages 

- types
  - adding notes
  - updating notes
    - updating in general
    - fixing spelling mistakes
  - moving notes
  - resolving an idea
    - (because it was implemented or something)
  - general formatting changes
- scopes?

- for now just push everything to `dev` and be done with it
- might change the commits later and then push that to `main`, when I'm happy
  with it

