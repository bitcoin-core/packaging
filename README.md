Bitcoin Core packaging
=======

Bitcoin Core is packaged and distributed through different channels.

Advanced users can compile Bitcoin Core from source. Static binaries for Linux, as well as installers for Windows and macOS are
provided on the [website](https://bitcoincore.org/en/download/).

Bitcoin Core is also distributed in third-party package managers. Inside this repo, those are:

* The `bitcoin-core` snap package for https://snapcraft.io/bitcoin-core is maintained in [/snap](/snap)
* The [/debian](/debian) packaging is currently unmaintained, see https://github.com/bitcoin-core/packaging/issues/36

An RPM spec file was removed in commit fa7c698cb24bab350b40ee2d825c443dabdd9633, because is was unmaintained and
outdated.
