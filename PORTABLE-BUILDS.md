# Download Craft 0.9.7

Use [the current release instructions](RELEASE-NOTES.md) for Windows, universal
Mac, Fedora/RPM, Debian-family DEB and AppImage installation and media helpers.

`VERSION` contains the public app version. Cargo, UI, CLI and browser versions
are aligned at 0.9.7.

Build native binaries with Cargo. Package with `scripts/package.py`, or build
Linux glibc-2.28 binaries using cargo-zigbuild and run `scripts/package_linux.py`.
Mac cross-packaging accepts `--signer <rcodesign>` to sign the app's resources as
well as its universal executable. Native Mac packaging uses system codesign.

The GitHub Actions workflow builds and uploads desktop packages on pushes to
`main`/`master`, pull requests, and manual runs. Pushing a `v*` tag builds all
platforms and publishes their artifacts as a GitHub release with
GitHub-generated release notes.

All previous deep-review fixes are included; proposals in REVIEW-0.9.6.1.md are
not implemented. Paused/failed downloads may retain `.dcmeta` for resuming;
successful jobs remove it.
