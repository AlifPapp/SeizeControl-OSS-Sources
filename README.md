# SeizeControl open-source component sources

Source code for the open-source components that ship inside
[SeizeControl](https://store.steampowered.com/app/4496300/SeizeControl/) and its DLC, published to meet the
source-availability terms of their licences (GPL section 3 and similar). Each
release of this repository corresponds to one shipped component build and carries:

- the binary archive exactly as shipped (a mirror, so the build stays reproducible
  after the upstream project rotates its releases),
- the build system that produced it,
- the corresponding source of every library linked into it, and
- a manifest naming the commit or file each source archive was taken from.

Nothing here is modified: SeizeControl ships these builds unchanged. The licence
texts travel with the binaries inside the app; this repository is the source offer
they refer to.

## Releases

| Release | Component | Shipped in |
| --- | --- | --- |
| `mpv-source-20261021` | mpv, shinchiro mpv-winbuild-cmake build `20261021` (mpv `e471496c56`, x86_64) | SeizeControl Wallpapers DLC |

The `manifests/` folder keeps a browsable copy of each release's manifest.

## Rebuilding

Each release's build-system snapshot is the shinchiro `mpv-winbuild-cmake` tree at the
tagged release. Its README describes the toolchain and the build steps. The package
definitions under `packages/` fetch sources from upstream; to build from the archived
sources instead, unpack the matching tarball from the release where the package
definition expects its source tree.

Compilers and build tools (GCC, binutils, mingw-w64, CMake, Meson, Ninja, NASM) are
generally available free programs used unmodified; the manifests name their versions
but this repository does not archive them.

## Questions

Open an issue here, or ask on the SeizeControl Steam community hub.
