# Phorepoc

**Phorepoc keeps Symbian alive as an open operating system.** It builds the Symbian platform source that Nokia and the
Symbian Foundation released in 2010 (EPL) with a modern GCC toolchain and runs it on hardware of today: an x86-64 PC
or virtual machine, and the PINE64 PinePhone. The full S60 (Symbian^3) user interface, its applications, networking
with modern TLS, and new parts of our own (a download app, a developer shell, an OpenGL ES stack through Mesa).

## Try it

| | |
|---|---|
| **VirtualBox** | download the `.ova` from the [adaptation-pc releases](https://github.com/Phorepoc/adaptation-pc/releases) and import it (File > Import Appliance) |
| **PinePhone** | download the `.img.xz` from the [adaptation-pinephone releases](https://github.com/Phorepoc/adaptation-pinephone/releases) and write it to a microSD card with [balenaEtcher](https://etcher.balena.io); the phone boots the card when it is in, its own system when it is out |

## Repositories

| | |
|---|---|
| [core](https://github.com/Phorepoc/core) | the OS: our changes to Symbian, our own components, the component registry, the pinned source |
| [pdk](https://github.com/Phorepoc/pdk) | the platform development kit: `ph` (build, images, packages) and PhoneLab (a phone's debug link as a web UI, REST API and MCP server) |
| [toolchain](https://github.com/Phorepoc/toolchain) | the build images (`ghcr.io/phorepoc/...`) |
| [adaptation-x86-64](https://github.com/Phorepoc/adaptation-x86-64), [adaptation-pc](https://github.com/Phorepoc/adaptation-pc) | x86-64 (x32 ABI) and PCs: QEMU, VirtualBox, real hardware |
| [adaptation-a64](https://github.com/Phorepoc/adaptation-a64), [adaptation-pinephone](https://github.com/Phorepoc/adaptation-pinephone) | the Allwinner A64 and the PinePhone |
| [tls](https://github.com/Phorepoc/tls) | SSL.DLL and libssl.dll over mbedTLS (TLS 1.2/1.3), also for older Symbian phones |
| [mesa-symbian](https://github.com/Phorepoc/mesa-symbian) | OpenGL ES through Mesa |
| [cxxrt](https://github.com/Phorepoc/cxxrt), [webkit-symbian](https://github.com/Phorepoc/webkit-symbian) | a modern C++ runtime and the WebKit engine port |
| [codecpack](https://github.com/Phorepoc/codecpack) | FFmpeg and OpenH264 media support, installed through the download app |
| [index](https://github.com/Phorepoc/index) | the curated list of apps the download app offers |
| [symbian-2010](https://github.com/Phorepoc/symbian-2010) | the 2010 release itself, minimally changed, booting on QEMU Syborg |
| [qemu-syborg](https://github.com/Phorepoc/qemu-syborg) | the Symbian QEMU (Syborg board) as a container image |
| forks of the SymbianSource packages | pristine mirrors of the 2010 source, pinned by core |

## Licences

Phorepoc's OS code is EPL-2.0 (with GPL-2.0-or-later as a Secondary License; the Nokia-derived files are relicensed from the Symbian source's EPL-1.0 under its section 7); the pdk is Apache-2.0; ported third-party code
keeps its own licence (Mesa: MIT, mbedTLS: Apache-2.0, FFmpeg: LGPL). Copyright: The Phorepoc Authors (founded by
Kyriakos Bompotis). Contributions are welcome -- see each repository's README.
