# TollGuru Country Coverage API - Wiki Repository

This repository hosts the documentation for the **TollGuru Country Coverage API**.

The primary documentation is maintained in the **GitHub Wiki** associated with this repository.

## Documentation

Please refer to the Wiki for detailed information about supported countries:

➡ Wiki: https://github.com/mapup/tollguru-country-coverage-toll-api/wiki

The wiki currently includes:

- Region-wise list of countries supported by TollGuru.
- Each region contains the corresponding supported countries.

Regions covered include:
- North America
- Europe
- Asia
- Australia
- Latin America
- Africa

## Setup after cloning

Run this once per clone (and once per new `git worktree`):

```bash
./hooks/install.sh
```

It points `core.hooksPath` at the tracked `hooks/` directory and installs
[gitleaks](https://github.com/gitleaks/gitleaks) if it is missing, so a `pre-commit`
scan blocks any commit that contains a secret. The wiring lives in `.git/config`, which
is not part of the repo — cloning gets you the hook files but not the wiring, so this
command is required.

Verify both halves took:

```bash
git config --get core.hooksPath   # -> hooks
gitleaks version
```

The `Gitleaks Secret Scan` workflow in `.github/workflows/gitleaks.yml` is the CI
backstop for clones where the hook was never installed.

Emergency bypass for a single commit: `GITLEAKS_SKIP=1 git commit ...`

## Note

This repository exists to maintain and organize the documentation for the TollGuru Country Coverage API.

Please update or add documentation through the **Wiki pages**.
