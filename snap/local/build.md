# Build the snap for Snapcraft via Launchpad

- Push the latest version to `main` (if applicable), e.g. https://github.com/bitcoin-core/packaging/pull/168

- Create a new branch for the major release "VV.x" from `main` (used to build the snap package) and request the
  track (if applicable), e.g. https://forum.snapcraft.io/t/track-request-for-bitcoin-core-snap-24-x/33072

- Use `bitcoin-core` on launchpad so that launchpad can start building the snap package

  - https://code.launchpad.net/~bitcoin-core/bitcoin-core-snap/+git/packaging (Click "Import Now" to fetch the branch)
  - https://code.launchpad.net/~bitcoin-core/bitcoin-core-snap/+git/packaging/+ref/VV.x (Click "Create snap package")
  - Name it "bitcoin-core-snap-VV.x"
  - Leave owner and series as-is
  - Select architectures that are compiled via guix
  - Leave "automatically build when branch changes" unticked
  - Tick "automatically upload to store"
  - Put "bitcoin-core" in the registered store package name field
  - Create a channel with "VV.x" as track, "Edge" as risk
  - Click "create snap package"
  - Click "Request builds" for every new release on this branch (after updating the snapcraft.yml in the branch to reflect the latest guix results)
  - Promote release on https://snapcraft.io/bitcoin-core/releases if it passes sanity checks
