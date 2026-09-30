# AgenticEMT releases

Official downloads of **AgenticEMT**, a plugin package for editing PSCAD `.pscx` projects. This
repository contains no source code, only published release packages and their release notes.

**Latest release: <https://github.com/AgenticEMT/agentic-emt-releases/releases/latest>**

## Install

AgenticEMT is not a standalone program, and not a VS Code extension on its own: it runs inside an
application that supports it. There are two ways to install it there:

- **In one step:** run **Install AgenticEMT** from the Command Palette, or click **Install
  AgenticEMT** on a `.pscx` that says AgenticEMT is not installed. It downloads the latest release
  from this repository, checks its SHA-256 and installs it.
- **From a download:** download `agentic-emt-<version>.zip` from the latest release, run **Install
  AgenticEMT from ZIP…** from the Command Palette, and pick that file. There is no need to unpack
  it. Use this when the application cannot reach GitHub.

Either way, an open `.pscx` switches to the editor once AgenticEMT is ready. If the application is
too old to load a release, it says so when the package is installed.

AgenticEMT draws PSCAD components with the artwork of the PSCAD installed on your own Windows
machine. Nothing derived from PSCAD's component library is in these downloads, and the artwork it
extracts stays on your machine.

## Verify your download

**Install AgenticEMT** checks this for you. For a file you downloaded yourself, every release
publishes the SHA-256 of its package, in the release notes and in `SHA256SUMS`:

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
