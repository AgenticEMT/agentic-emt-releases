# AgenticEMT releases

Official downloads of **AgenticEMT** — PSCAD `.pscx` editing for Modex. This repository contains no
source code, only published release packages and their release notes.

**Latest release: <https://github.com/AgenticEMT/agentic-emt-releases/releases/latest>**

## Install

AgenticEMT runs inside **Modex for VS Code 0.1.15 or later**, the first version that opens `.pscx`
projects. Download `agentic-emt-<version>.zip` from the latest release, then in VS Code:

1. Run **Modex: Install AgenticEMT Package…** from the Command Palette.
2. Choose **Install from a downloaded .zip** and pick the file you downloaded. There is no need to
   unpack it.
3. Reopen any `.pscx` you had open.

AgenticEMT draws PSCAD components with the artwork of the PSCAD installed on your own Windows
machine. Nothing derived from PSCAD's component library is in these downloads, and the artwork it
extracts stays on your machine.

## Verify your download

Every release publishes the SHA-256 of its package, in the release notes and in `SHA256SUMS`:

```powershell
Get-FileHash .\agentic-emt-<version>.zip -Algorithm SHA256
```

```bash
sha256sum -c SHA256SUMS
```

If the value does not match, delete the file and do not install it, and report it privately (see
[SECURITY.md](SECURITY.md)).

## Reporting a problem

- **A bug or a question:** open an issue in this repository. Leave out anything from your projects you
  would not want public — an issue here is readable by anyone.
- **A security vulnerability:** never in an issue. Use **Security → Report a vulnerability**, which
  only the maintainers can read; [SECURITY.md](SECURITY.md) says what to include.

## Release tags

Releases are tagged `v<version>`. Published releases are **immutable**: once a release exists, its
tag and its files cannot be replaced. A problem in a shipped package is fixed by publishing a new
version, never by swapping a file you have already verified.

## Licence

Each package carries its terms in `LICENSE`, and the notices of the third-party software it includes
in `THIRD-PARTY-NOTICES.md` and `THIRD-PARTY-LICENSES.md`.

PSCAD and EMTDC are trademarks of Manitoba Hydro International Ltd. AgenticEMT is not affiliated with
or endorsed by Manitoba Hydro International.
