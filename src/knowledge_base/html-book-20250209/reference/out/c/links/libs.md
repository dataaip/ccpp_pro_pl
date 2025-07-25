# A list of open source C libraries

From cppreference.com
< c‎ | links

The objective of this page is to build a comprehensive list of open-source C libraries, so that when one needs an implementation of particular functionality, one needn’t to waste time searching on web (DuckDuckGo, Google, Bing, etc.)

If you know a library that might be useful to others, please add a link to it here. There are no restrictions on what can be included except that the ****source**** of the library must be readily ****available**** to download.

The page is provided “as is” - with the hope of being useful, but without any warranties. Outdated, misleading or wrong links might appear here. If you’ve noticed one of these, it would be great if you fixed the error.

# Package managers

| Package manager | Description |
| --- | --- |
| build2 | An open-source (MIT), cross-platform build toolchain that aims to approximate Rust Cargo’s convenience for developing and packaging C/C++ projects while providing more depth and flexibility, especially in the build system. |
| cget | Cmake package retrieval. This can be used to download and install cmake packages. |
| cmodule | Non-intrusive cmake dependency management. |
| conan | Decentralized, open-source (MIT), C/C++ package manager. |
| CPM.cmake | A cmake script that adds dependency management capabilities to cmake. It’s built as a thin wrapper around cmake’s FetchContent module that adds version control, caching, a simple API and more. |
| hunter | A cmake driven cross-platform package manager for C/C++ projects. |
| spack | A package manager for supercomputers, Linux, and macOS. It makes installing scientific software easy. It isn’t tied to a particular language. |
| teaport | A cocoapods inspired dependency manager. |
| vcpkg | A C/C++ package manager for Windows, Linux, and macOS. |
| xmake | A cross-platform Lua-based C/C++ build tool and package manager. |

# Libraries

## Operating system

Access control

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| acl |  |  |  |
| apparmor |  |  |  |

Extended attributes

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| attr |  |  |  |

## Graphical user interface

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| IUP |  |  |  |
| Nuklear | A single-header ANSI C immediate mode cross-platform GUI library. (Doc) |  |  |
| lvgl | Powerful and easy-to-use embedded GUI library with many widgets, advanced visual effects (opacity, anti-aliasing, animations) and low memory requirements (16K RAM, 64K Flash). (Doc) |  |  |
| tiny file dialogs | A single C cross-platform file (no init, no main loop, 6 modal function calls) |  |  |

## Gtk+ widgets

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| appmenu-gtk |  |  |  |
| ghex |  |  |  |
| goocanvas |  |  |  |
| gtkhotkey |  |  |  |
| gtk+ |  |  |  |
| gtksourceview |  |  |  |
| gtkspell |  |  |  |
| gucharmap |  |  |  |
| webkitgtk |  |  |  |

## Microsoft Excel

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libxlsxwriter |  |  |  |
| xlsx_drone |  |  |  |

## Audio

CD

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| cdparanoia |  |  |  |

Codecs

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| aften |  |  |  |
| faad2 |  |  |  |
| wavpack |  |  |  |

Infrastructure

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| alsa-lib |  |  |  |
| portaudio |  |  |  |

Speech synthesis

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| espeak |  |  |  |
| flite |  |  |  |

## Video

Codecs

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| schroedinger |  |  |  |
| video4linux |  |  |  |

## Files

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gmime |  |  |  |

## Maths

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gsl | The GNU Scientific Library (GSL) is a numerical library for C and C++ (Src) | GPL | make |

Integer Multi-Dimensional Interpolation

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| argyll |  |  |  |

Linear algebra

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| atlas |  |  |  |
| blas |  |  |  |
| eigen |  |  |  |

Finance

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ta-lib |  |  |  |

FFT

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| fftw3 |  |  |  |

Multiprecision

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gmp |  |  |  |

Signal Processing

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| liquid-dsp |  |  |  |
| vsipl |  |  |  |
| vsipl++ |  |  |  |

## Graphics

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| allegro | Allegro-5 is a cross-platform multimedia library mainly aimed at video game and multimedia programming. |  |  |
| babl |  |  |  |
| Bgfx | A cross-platform, graphics API agnostic, "Bring Your Own Engine/Framework" style rendering library. | BSD 2 |  |
| cairo |  |  |  |
| raylib | A cross-platform C99 gamedev library featuring OpenGL hardware acceleration, full 3D support, skeletal animation, shaders, fonts, audio, math, GUI, etc. (Src) (Doc) | Zlib | cmake, make, vcpkg, zig |
| SAIL | ****S****quirrel ****A****bstract ****I****mage ****L****ibrary is a small, fast, and cross-platform image decoding library. |  |  |
| SDL | ****S****imple ****D****irectMedia ****L****ayer is a cross-platform library for input, audio, drawing and much more. |  |  |
| SIGIL |  |  |  |
| Simple2d | A small, simple, cross-platform SDL2/OpenGL wrapper that provides drawing, media, windowing, and input capabilities. | MIT |  |

## Generic

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libmixf |  |  |  |

## Interprocess

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| dbus |  |  |  |
| dee |  |  |  |
| gdbus |  |  |  |

## Databases

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| berkeley_db |  |  |  |
| libfmrt |  |  |  |
| libmongoc | Official C driver library for MongoDB (Doc). It offers optimized APIs for CRUD operations, comprehensive feature support (including BSON) and support for different authentication mechanisms enabling efficient integration of MongoDB functionality into C-based applications. | Apache 2.0 | CMake |
| lmdb |  |  |  |
| SQLite | A C library that implements a small, fast, self-contained, high-reliability, full-featured, SQL database engine. SQLite is the most used database engine in the world. (Src) (Doc) | Public Domain |  |

## Configuration

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libconfig |  |  |  |
| libconfini |  |  |  |

## Environment

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| libXDGdirs |  |  |  |

## Communications

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| gsoap |  |  |  |
| KCP | A fast and reliable ARQ protocol that helps applications to reduce network latency. | MIT |  |
| libcurl |  |  |  |
| libmicrohttpd |  |  |  |
| libsagui |  |  |  |
| MQTT-C | Github URL | MIT |  |
| nanomsg | A socket library that provides common communication patterns; has no dependencies; cross-platform. Superceded by the nng. | MIT/X11 |  |
| UCX | Unified Communication X (UCX) provides an optimized communication layer for Message Passing (MPI), Shared Memory (PGAS) and RPC/data-centric applications. | BSD3 |  |
| zeromq |  |  |  |
| libusb | A portable C library that provides generic access to USB devices. |  |  |

## Compression

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| bzip2 |  |  |  |
| lz4 |  |  |  |
| zlib |  |  |  |

## Concurrency

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| ck |  |  |  |
| MutexGear | Mutex-only synchronization (wheel, rwlock, work queues). | The MutexGear Library |  |

## Data types

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| bstrlib |  |  |  |
| datastd |  |  |  |
| str | Yet another string library for C language. |  |  |

## PDF

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| PDFio | A simple C library for reading and writing PDF files. | Apache-2.0 | make |

## XML

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| expat |  |  |  |
| gsoap |  |  |  |

## Metrics

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| edlib |  |  |  |

## Object oriented programming

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| Cello |  |  |  |
| GObject |  |  |  |

## Web Frontend

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| cgit |  |  |  |

## Debug

| Library | Description | License | Configuration |
| --- | --- | --- | --- |
| dbg-macro | A few macros that print and return the value of a given expression for quick and dirty debugging, inspired by Rust’s dbg!(...) macro and its C++ variant. | MIT |  |

### See also

|  |  |
| --- | --- |
| C++ documentation for Non-ANSI/ISO Libraries | |

### External links

|  |  |
| --- | --- |
| 1. | A list of C unit testing frameworks — at Wikipedia |
| 2. | A curated list of (awesome) C and C++ libraries — at GitHub |
| 3. | A list of C open-source games and frameworks — at GitHub.io |

Retrieved from "<https://en.cppreference.com/mwiki/index.php?title=c/links/libs&oldid=180169>"

##### Navigation

- Online version
- Offline version retrieved 2025-02-09 16:39.

- This page was last modified on 4 February 2025, at 23:49.