# Local development and review

## Start with a clean, explicit checkout

This is a document repository. On NixOS, Git and a text editor are sufficient to review the current artifact. There is no environment to activate, no package installation command and no native service to launch. Inspect `git status --short --branch`, the latest commit and the file inventory before changing anything. Use a topic branch and preserve unrelated changes. Publication targets the canonical primary branch through a human-reviewed PR; routine hosted validation is not a substitute for local review.

Do not run application setup commands copied from an example prompt in an unrelated working directory. A proposed vault is not a supplied dataset, and a suggested integration is not an installed adapter. The ordinary editing loop is to read the relevant contract, edit the smallest related document, check internal references, and review the diff for unsupported claims and private material.

## Reproduce the content review

These read-only checks work in Bash from the repository root:

```bash
git status --short --branch
git ls-files
rg -n '^(#|name:|description:)|session_events|memory_notes|memory_links' README.md docs skills
git diff --check
```

The search locates contracts rather than validating YAML. `git diff --check` finds whitespace errors, not incorrect architecture. There is no committed linter or test command. A future schema validator would require a deliberate dependency choice and tests; installing an arbitrary YAML parser does not make it an established project toolchain.

## What counts as a meaningful review

Check that each field's meaning is consistent in the README, skill and schema reference. Confirm that a status cannot accidentally become confidence, that runtime proposals are labeled proposals, and that examples contain no secrets, real customer data or private machine paths. Inspect wiki-link syntax with any parser selected by a future implementation. Follow every local documentation link from the receiving document's directory, because relative paths are resolved there.

Do not claim NixOS runtime support for an application that does not exist. The current documentation can be read and edited on NixOS. An eventual executable implementation would need a reproducible development environment, supported parser versions and native checks before claiming that larger support boundary.
