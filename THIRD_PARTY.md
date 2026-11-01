# Third-party components / Üçüncü taraf bileşenleri

Mavio's original application code is proprietary. The following independent components keep their own licences and copyright notices. The Windows package includes licence texts under `licenses/`. The Qt and libmpv libraries remain separate, replaceable DLLs; Mavio does not prohibit modification or debugging rights granted by their licences.

| Component | Distributed version | Licence and corresponding upstream sources |
| --- | --- | --- |
| libmpv | v0.41.0-1373-g9e2ed65eb, official project development-build artifact 41103006513, Windows x64 **LGPL variant** | LGPLv3; [exact mpv revision](https://github.com/mpv-player/mpv/tree/9e2ed65eb0c02f99a352dfa1ad3c85ecceefe005), [build recipe and subprojects](https://github.com/mpv-player/mpv/blob/9e2ed65eb0c02f99a352dfa1ad3c85ecceefe005/ci/build-win32.ps1), [upstream build and licence description](https://github.com/mpv-player/mpv/releases/tag/git-release) |
| python-mpv | 1.0.8 | LGPL when used with LGPL libmpv; [source and licence](https://github.com/jaseg/python-mpv/tree/v1.0.8) |
| Qt / PySide6 / Shiboken6 | 6.11.2 | LGPLv3 for the modules used here; [Qt sources](https://download.qt.io/official_releases/qt/6.11/6.11.2/submodules/), [Qt for Python sources](https://code.qt.io/cgit/pyside/pyside-setup.git/?h=6.11.2), [licensing](https://doc.qt.io/qt-6/licensing.html) |
| Python | 3.11.9 | PSF; [source and licence](https://www.python.org/downloads/release/python-3119/) |
| Requests | 2.34.2 | Apache-2.0; [source](https://github.com/psf/requests/tree/v2.34.2) |
| urllib3, certifi, charset-normalizer / chardet | Versions recorded in package notices | MIT / MPL-2.0 / MIT / LGPL; their installed distribution notices are included |
| cryptography | 50.0.2 | Apache-2.0 or BSD-3-Clause; [source](https://github.com/pyca/cryptography/tree/50.0.2), includes OpenSSL under its own licence |
| defusedxml | 0.7.1 | PSF; [source](https://github.com/tiran/defusedxml/tree/v0.7.1) |
| Nuitka | 4.3.4, build tool | Apache-2.0; [source](https://github.com/Nuitka/Nuitka/tree/4.3.4) |

libmpv includes FFmpeg and other open-source libraries. Refer to the exact upstream build recipe, dependency source locations and bundled `LICENSE.LGPL`. GPL-only Qt QML modules and the GPL variant of libmpv are not included in this Mavio distribution.

The original Mavio icon and synthetic screenshots in this repository were created for Mavio. Screenshot demo titles and artwork are illustrative; no TV channels, streaming subscriptions or provider accounts are bundled.

## Library replacement

You may replace the LGPL libraries with compatible modified builds for your own use. Keep the same ABI, file names and platform architecture. `libmpv-2.dll` is beside `MavioPlayer.exe`; the Qt DLLs and QML plugins are included separately. Such changes can affect playback or interface compatibility. Original application source code is not required to replace these dynamically loaded libraries.
