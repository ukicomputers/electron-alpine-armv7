# electron-alpine-armv7
Lot of people need to run a web UIs on embedded systems, with architectures like **armv7** (Raspberry Pi Zero 2W uses it for example). Also, that devices need to run minimal, bloat-free distributions, like Alpine Linux is. Since Alpine Linux uses *musl* as main C++ library, which differs from most standard libaries (usually provided by gcc and clang), some big projects, that require deep level usage of STD's, can't compile, nor run, even with translation layer. There is "Electron/Chromium port" on *pkgs.alpinelinux.org* (testing/electron), but it isn't compiled for **armv7**. This repository provides **apk**s for **armv7** architecture for *electron* package. It is being rebuilt on *every 1st* of each month.

See **Releases**, choose version of *electron* package, and download it's **apk**.  
Also [view](https://github.com/ukicomputers/electron-alpine-armv7/actions/workflows/compile.yml) current workflows (some of them may be manually triggered, so then "build status dot" at the commit name isn't visible).

## Note
Since build packages **aren't signed**, while installing it with apk, you need to use option **--allow-untrusted** option (example `apk add --allow-untrusted <path to the executable>`).

## License
You can relate to license for [aports/testing/electron](https://gitlab.alpinelinux.org/alpine/aports/-/tree/master/testing/electron). There isn't any license in particular for usage of this **apk**s.
