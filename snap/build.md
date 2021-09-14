# Build the snap for Snapcraft via Launchpad

- Push the latest version to master (if applicable), e.g. https://github.com/bitcoin-core/packaging/pull/32

- Create a new branch for the major release "VV.x" from master (used to build the snap package) and request the
  track (if applicable), e.g. https://forum.snapcraft.io/t/track-request-for-bitcoin-core-snap/10112/7

- Notify MarcoFalke so that he can start building the snap package

  - https://code.launchpad.net/~bitcoin-core/bitcoin-core-snap/+git/packaging (Click "Import Now" to fetch the branch)
  - https://code.launchpad.net/~bitcoin-core/bitcoin-core-snap/+git/packaging/+ref/VV.x (Click "Create snap package")
  - Name it "bitcoin-core-snap-VV.x"
  - Leave owner and series as-is
  - Select architectures that are compiled via guix
  - Leave "automatically build when branch changes" unticked
  - Tick "automatically upload to store"
  - Put "bitcoin-core" in the registered store package name field
  - Tick the "edge" box
  - Put "VV.x" in the track field
  - Click "create snap package"
  - Click "Request builds" for every new release on this branch (after updating the snapcraft.yml in the branch to reflect the latest guix results)
  - Promote release on https://snapcraft.io/bitcoin-core/releases if it passes sanity checks
