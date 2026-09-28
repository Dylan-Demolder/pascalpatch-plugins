# PascalPatch plugins

The plugin site for PascalPatch, served by GitHub Pages at https://dylan-demolder.github.io/pascalpatch-plugins/

`index.json` is signed offline by the maintainer (Ed25519, key `bae2cb542510218e`); the PascalPatch app installs only what it lists, after checking each package's SHA-256. `catalog.json` is display data only.

**Write your own plugin:** start with the guide at [PascalPatch/docs/plugins](https://github.com/Dylan-Demolder/PascalPatch/blob/master/docs/plugins/README.md), then add it here as `community/<id>/` in a pull request ([CONTRIBUTING.md](CONTRIBUTING.md)). Pull requests carry source only; the maintainer builds, signs and publishes the packages.
