[![DegateBanner](https://raw.githubusercontent.com/DegateCommunity/Degate/develop/etc/degate_banner.png)](https://github.com/DegateCommunity)

<p align="center">
    <a href="https://gitter.im/DegateCommunity/Degate" alt="Gitter">
        <img src="https://badges.gitter.im/DegateCommunity/Degate.svg" /></a>
    <a href="https://github.com/DegateCommunity/Degate/blob/master/LICENSE.TXT" alt="License">
        <img src="https://img.shields.io/github/license/DegateCommunity/Degate" /></a>
    <a href="https://github.com/DegateCommunity/Degate/issues" alt="GitHub Issues">
        <img src="https://img.shields.io/github/issues/DegateCommunity/Degate" /></a>
    <a href="https://github.com/DegateCommunity/Degate/commits/develop" alt="Last Commit">
        <img src="https://img.shields.io/github/last-commit/DegateCommunity/Degate/develop" /></a>
    <a href="https://github.com/DegateCommunity/Degate/releases" alt="Last Release">
        <img src="https://img.shields.io/github/release-date-pre/DegateCommunity/Degate" /></a>
    <a href="https://github.com/DegateCommunity/Degate/graphs/contributors" alt="Contributors">
        <img src="https://img.shields.io/github/contributors/DegateCommunity/Degate" /></a>
</p>

&nbsp;

Degate is a multi-platform software for semi-automatic VLSI reverse engineering of digital logic in chips. This project is a fork of the initial Degate project, the final goal is to replace it. For more please visit our [wiki](https://github.com/DegateCommunity/Degate/wiki) page and, if you want to chat, visit our [Gitter](https://gitter.im/DegateCommunity/Degate). The current project maintainer is [Dorian Bachelot](https://github.com/DorianBDev).

&nbsp;

- [Degate updates repository](#degate-updates-repository)
  - [Explanations](#explanations)
  - [Create a release/pre-release](#create-a-releasepre-release)
- [License](#license)

&nbsp;

# Degate updates repository

## Explanations

This repository store Degate updates. It's here every maintenance tool (see Qt Installer Framework) will check for new updates. There is two "channels" : a release one and a nightly one. The release channel store only updates for full releases and the nightly channel store all updates (releases and pre-releases).

## Create a release/pre-release

To create a release/pre-release you need to:
- Check deploy scripts (mostly URL links, like ifw ones).
- Change the version in the VERSION file of the main Degate repository (add a release date).
- Merge the develop branch in the master branch (also in the release and hotfix branches).
- Trigger manually the three github actions : "Windows deploy", "Linux deploy" and "Mac deploy".
- Create a new release/pre-release with the proper version tag.
- Upload all artifacts generated by the three github actions EXCEPT updates ones.
- Extract update artifacts here, in proper folders (OS/release OR nightly/configuration).
- Publish the release/pre-release.
- Update the website downloads [here](https://github.com/DegateCommunity/degatecommunity.github.io/blob/main/config.json).

Update release and nightly channels for every release (just paste generated artifacts content in the proper folder(s), don't forget to delete previous content), but update only nightly channel for pre-release. A pre-release version is a version of the form 'X.X.X-[alpha|beta|rc].X' and a release version will have the form 'X.X.X'.

# License

Degate is released under the GNU General Public License Version 3. See LICENSE.TXT for details.

The current main maintainer of Degate is Dorian Bachelot dev@dorianb.net and the original Degate maintainer is Martin Schobert martin@mailbeschleuniger.de.
