# ethon CLI

[![Latest release](https://img.shields.io/github/v/release/ethonAI/ethon-cli?sort=semver)](https://github.com/ethonAI/ethon-cli/releases/latest)
![License: Proprietary](https://img.shields.io/badge/license-proprietary-blue)

The `ethon` command-line tool for deploying and updating Ethon edge applications. Learn more about Ethon at [ethon.com](https://ethon.com).

## Prerequisites

The CLI deploys apps as Docker containers, so it needs [Docker](https://docs.docker.com/get-docker/) installed and running on the host (`docker compose` is included with current Docker versions).

## Install

Download the archive for your platform from the [latest release](https://github.com/ethonAI/ethon-cli/releases/latest), extract it, and place the `ethon` binary somewhere on your `PATH`.

Prebuilt binaries are available for Linux, macOS, and Windows (amd64 and arm64).

**Linux / macOS:**

```sh
# pick the archive matching your OS and architecture
tar -xzf ethon_<version>_<os>_<arch>.tar.gz
sudo mv ethon /usr/local/bin/
```

**Windows:** extract the `.zip` and move `ethon.exe` to a directory on your `PATH`.

Optionally verify the download against the `checksums.txt` from the same release:

```sh
sha256sum --ignore-missing -c checksums.txt
```

Verify the install:

```sh
ethon version
```

### First run on macOS / Windows

The released binaries are not yet code-signed, so the operating system may warn you the first time you run `ethon`. This is expected; the download is verified by `checksums.txt`.

- **macOS:** if you see *"cannot be opened because it is from an unidentified developer"*, remove the quarantine flag once with `xattr -d com.apple.quarantine ./ethon`, then run it. (Alternatively: System Settings → Privacy & Security → "Open Anyway".)
- **Windows:** if SmartScreen shows *"Windows protected your PC"*, click **More info → Run anyway**.

## Keeping it up to date

The CLI updates itself in place:

```sh
ethon upgrade          # upgrade to the latest release
ethon upgrade --check  # report whether a newer version exists, without changing anything
```

On a machine without internet access, download a release archive (and its `checksums.txt`) on a connected machine, copy both across, and apply it offline:

```sh
ethon upgrade --from ethon_<version>_<os>_<arch>.tar.gz
```

## Documentation

Usage documentation for the `ethon` CLI is coming soon.

## Support

The `ethon` CLI is for users of the Ethon platform. If you have any questions, please contact Ethon support.

## License

Proprietary — © 2026 EthonAI AG. See [LICENSE](LICENSE). Third-party attributions are bundled in each release archive (`THIRD_PARTY_LICENSES.txt`) and can be printed with `ethon licenses`.
