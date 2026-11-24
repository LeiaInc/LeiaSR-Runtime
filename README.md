# LeiaSR Runtime

> **Developer preview.** Builds published here are beta, non-production builds for developers.
> They are not Leia's official production releases. Display owners should get the runtime
> from Leia or their display manufacturer.

The runtime and SDK for Leia autostereoscopic 3D displays. Eye tracking drives a weaver that
interlaces left and right views for the panel's lenticular lens, so the image is 3D without glasses.

This repository is where Leia publishes developer previews of:

- **Runtime installers**, one GitHub release per version, each with a `SHA256SUMS` file:
  Windows x64 (`.exe`) and Linux (`.deb`), with macOS (`.pkg`) and Windows on ARM previews
  added as they become available.
- **The v2 C SDK**: the `sr_*.h` headers, the loader and a CMake package
  (`find_package(LeiaSR)`), so an application or plugin can build without the runtime installed.

## Releases

A version appears here only after it has passed Leia's internal QA. Release candidates
(`v1.39.0-rcN`) are tested internally and are not published here. Every release here is
marked as a pre-release (preview).

The Windows installer is Authenticode-signed by **Leia, Inc.** Check every download against the
release's `SHA256SUMS`.

Install silently with `LeiaSR-Runtime-<version>-win64.exe /S`. Installing over an earlier
LeiaSR runtime, including 1.34.x installed by a display manufacturer, upgrades it in place, and
applications built on older SDKs keep working.

## Pairing with DisplayXR

[DisplayXR](https://displayxr.org) runs on Leia displays through its Leia plugin, which needs a
LeiaSR runtime installed. Each release lists the DisplayXR runtime and Leia plugin versions it was
tested with. Older LeiaSR runtimes (1.34.8 and later) still work, but DisplayXR recommends an update.

| LeiaSR Runtime | DisplayXR runtime | Leia plugin |
|---|---|---|
| 1.39.0 (coming) | to be filled in at release | 2.23 or later |

## Redistribution

Anyone may download the runtime installers, and redistribute them unmodified, including
installing them automatically from another product (for example, DisplayXR). The exact terms are
in the licences below.

## Licences

- SDK headers, loader, CMake files and examples: [Apache License 2.0](LICENSE).
- Runtime binaries and installers: the LeiaSR Runtime Licence (`LICENSE-RUNTIME.md`, coming with
  the first release).

## Support

help@leiainc.com
