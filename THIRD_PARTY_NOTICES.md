# Third-party components

## Game content

The tool contains **no content from the games**: no ROM, no APK, no game text, picture or sound. Everything is read on the user's computer, from the user's own European DS ROM and from the APK files of the user's own copy of the game. The French texts written by the tool (`games` folder) stay on that computer.

*Dragon Quest* and all related names, characters and content are the property of their respective owners (Square Enix and its licensors). This project is unofficial and not affiliated with or endorsed by Square Enix, Nintendo or Google.

## Components included in `DQ456_Tool.exe`

The exe is built with PyInstaller from the tool's Python code. It contains:

| Component | Use | License |
|---|---|---|
| [Python](https://www.python.org/) (standard library) | runs the tool | Python Software Foundation License |
| [Tcl/Tk](https://www.tcl.tk/) (with Python's `tkinter`) | window of the tool | Tcl/Tk license (BSD-style) |
| [PyInstaller](https://pyinstaller.org/) bootloader | starts the bundled Python | GPL v2 with the PyInstaller bootloader exception (allows distributing the exe under any terms) |
| [UnityPy](https://github.com/K0lb3/UnityPy) | reads and writes the Unity data of the title screen option | MIT |
| [Pillow](https://python-pillow.org/) | pictures of the title screen option | MIT-CMU (HPND) |
| [NumPy](https://numpy.org/) | used by UnityPy and Pillow | BSD 3-Clause (with bundled components under compatible licenses, such as OpenBLAS: BSD 3-Clause) |
| [astc-encoder-py](https://github.com/K0lb3/astc-encoder-py), [etcpak](https://github.com/K0lb3/etcpak), [texture2ddecoder](https://github.com/K0lb3/texture2ddecoder) | texture formats of the game (title screen option) | MIT (the encoders they include: ARM ASTC Encoder, Apache 2.0; etcpak, BSD 3-Clause) |
| [Brotli](https://github.com/google/brotli), [lz4](https://github.com/python-lz4/python-lz4) | decompression of the Unity data | MIT; BSD 3-Clause (LZ4 library: BSD 2-Clause) |
| [attrs](https://www.attrs.org/), [fsspec](https://github.com/fsspec/filesystem_spec), [tpk_ar](https://github.com/K0lb3/tpk_ar), [archspec](https://github.com/archspec/archspec) | used by UnityPy | MIT; BSD 3-Clause; MIT; Apache 2.0 or MIT |

The sound part of UnityPy (fmod_toolkit, pyfmodex and the FMOD library, which is not free) is **not** included: the tool never reads sounds.

The launcher of the exe (installs the tool next to it, then starts it) is compiled at build time with the C# compiler that comes with Windows; it uses only the .NET Framework of Windows.

## Programs downloaded by the tool on demand (not included)

At the first launch, with the user's approval, the tool downloads these programs from their official sites into its `dependencies` folder. None of them is in this repository or in the exe.

| Program | Use | License |
|---|---|---|
| [SDK Platform-Tools](https://developer.android.com/tools/releases/platform-tools) (Google), from dl.google.com | `adb`: talks to the phone over USB (copies the APKs and the saves, installs the game) | Android Software Development Kit License Agreement (`adb` source code: Apache 2.0) |
| [Eclipse Temurin](https://adoptium.net/) 17 JRE (Eclipse Adoptium), from adoptium.net, only if no Java 11 or newer is installed | runs uber-apk-signer | GPL v2 with the Classpath Exception |
| [uber-apk-signer](https://github.com/patrickfav/uber-apk-signer) 1.3.0 (Patrick Favre-Bulle), from github.com | signs the patched APKs | Apache 2.0 |

