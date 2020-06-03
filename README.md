Bitcoin Core packaging
=======

Bitcoin Core is packaged and distributed through different channels.

Advanced users can compile Bitcoin Core from source. Static binaries for Linux, as well as installers for Windows and macOS are
provided on the [website](https://bitcoincore.org/en/download/).

In addition, this repository contains packaging metadata for package managers running on Linux. Currently

* [Snappy](/snap)
* [Debian](/debian)

A spec file for flathub is maintained under their organization: https://github.com/flathub/org.bitcoincore.bitcoin-qt

An RPM spec file was removed in commit fa7c698cb24bab350b40ee2d825c443dabdd9633, because is was unmaintained and
outdated.
