# NomOS Assets

Non-code assets used by NomOS live here so product source changes do not have
to carry large binary files through the main repository.

## Layout

```text
themes/
└── <theme-slug>/
    └── backgrounds/
        └── ...
```

Future asset families may get their own top-level directories (for example
branding or media), but product code should consume them through stable,
documented paths rather than depending on an ad-hoc repository layout.

## Product integration

The NomOS product repository consumes this repository as a pinned non-flake
input. Theme metadata and behaviour remain product code; this repository owns
only the binary/content assets.

A product checkout must continue to build deterministically from the exact
revision recorded in its lock file.

## Licensing and provenance

The repository-level LICENSE covers material for which the repository has the
right to grant that licence. It does not replace source-specific attribution
or licence obligations for third-party assets.

Every distributable asset must have its source, author/owner, and licence
status recorded in [PROVENANCE.md](PROVENANCE.md). Assets whose rights are
unclear should be removed or replaced rather than distributed on assumption.
