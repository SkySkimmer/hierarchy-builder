# Changelog

## UNRELEASED

- Use Coq's elaborator to typecheck factories and structures (coercions are
  now inserted properly)
- New attribute `#[mathcomp]` for `HB.structure` to synthesize backward
  compatibility code for the Mathematical Components library.
  When the mixin contains a single axiom its name can be given as
  `#[mathcomp(axiom="eq_axiom")]`.
- `HB.instance Definition name : factory T := term` works even if term is not
  a known builder. In this case the type (key) is read from the factory
  (the type of the definition).

## [0.10.0] - 2020-08-08

- HB now supports parameters (experimental).
- Port to Coq-Elpi 1.5.
- Better error message in case classes are not defined in the right order.
- Structure operations are not reexported by substructures.
- Spurious trivial `TYPE` structure removed from demo1.

## [0.9.1] - 2020-06-03

- `HB.instance` can be applied directly to a definition as in
  `HB.instance Definition foo := Bar.Build T ...`
- Port to Coq-Elpi version 1.4
- Operations `op` from factory `f` are not bound to `f_op` anymore,
  they are now bound to `op` and potentially masked operations
  are accessible via `Super.op`.

## [0.9.0] - 2020-03-11

First public release for Coq 8.10 and 8.11.
