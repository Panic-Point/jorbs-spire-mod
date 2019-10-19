# Jorbs Mod
[![GitHub release version badge](https://img.shields.io/github/v/release/dbjorge/jorbs-spire-mod?color=blue&label=latest%20release&sort=semver)](https://github.com/dbjorge/sts-jorbs-mod/releases)
[![GitHub Release download counter badge](https://img.shields.io/github/downloads/dbjorge/jorbs-spire-mod/total?color=blue)](https://github.com/dbjorge/sts-jorbs-mod/releases)

[Slay the Spire]() mod with character and game design by [Jorbs](https://twitch.tv/jorbs) and Twitch Chat.

* Design info: [Mod Character Package spreadsheet](https://docs.google.com/spreadsheets/d/1GY0eJsooEp361hWFL2lD-uPVa5-l-7g4f4FtyKs-k7Q/edit#gid=0)
* Discussion and updates: [Jorbs Discord](https://discord.gg/invite/jorbs) **#jorbs-spire-mod-char**

Many people have contributed code and art for this mod; thanks to all the contributors listed among the [mod authors](./src/main/resources/ModTheSpire.json).

This mod would not have been possible without the excellent documentation and guidance from all of the contributors at [ModTheSpire](), [BaseMod](), [StSLib](), [StS-DefaultModBase](https://github.com/Gremious/StS-DefaultModBase), and [Slay the Spire Discord](https://discordapp.com/invite/SlayTheSpire) **#modding**.

## Table of contents

* [How to Install](#how-to-install)
* [How to build from source](#how-to-build-from-source)
* [How to contribute card art](#how-to-contribute-card-art)
* [How to contribute sound effects](#how-to-contribute-sound-effects)
* [How to contribute changes](#how-to-contribute-changes)

## How to install

1. Through Steam, install Slay the Spire (stable branch)
1. From the Steam Workshop, install "Mod the Spire", "BaseMod", and "StSLib"
1. Download `JorbsMod.jar` from the latest release: [![GitHub release version badge](https://img.shields.io/github/v/release/dbjorge/jorbs-spire-mod?color=blue&label=latest%20release&sort=semver)](https://github.com/dbjorge/sts-jorbs-mod/releases)
1. Launch Mod the Spire by right clicking on Slay the Spire in your Steam Library "Play with Mods"
1. In the Mod the Spire launcher, select the "open mods folder" button
1. Copy `JorbsMod.jar` into this mods folder
1. Close and relaunch Mod the Spire
1. Make sure "BaseMod", "StSLib", and "JorbsMod" are all checked
1. Play!

## How to build from source

1. Create an environment variable named `STEAMAPPS_PATH`
    * On Windows, open a Command Prompt run `setx STEAMAPPS_PATH "C:\Program Files (x86)\Steam\steamapps"`
    * On Mac, open `~/.bash_profile` and add a line like `export STEAMAPPS_PATH="~/Library/Application Support/Steam/steamapps"`
    * Adjust the paths accordingly if you have installed Steam to a different location 
1. Install the Oracle Java 8 JDK (not Java 9+)
1. Install IntelliJ IDEA (the free Community edition is fine)
1. Through Steam, install Slay the Spire (stable branch)
1. From the Steam Workshop, install "Mod the Spire", "BaseMod", and "StSLib"
1. Clone the repository
1. Open the project in IntelliJ IDEA:
    1. Choose "Import Project"
    1. Choose the repository folder
    1. Select "Maven"
    1. Press next a few times, all other settings can be left at defaults 
1. Follow the [these instructions from the StS-DefaultModBase wiki](https://github.com/Gremious/StS-DefaultModBase/wiki/Step-3:-Packaging-and-Playing-the-Default;-Writing-Your-First-Mod!) to build the mod package and debug it

## How to contribute card art

See the [.../images/cards/README.md](src/main/resources/stsjorbsmodResources/images/cards/README.md) file in the resources folder.

## How to contribute sound effects

See the [.../audio/README.md](src/main/resources/stsjorbsmodResources/audio/README.md) file in the resources folder.

## How to contribute changes

*Note: if this is too complicated and you just want to send us some paint art for cards, feel free to reach out on the [Jorbs Discord](https://discord.gg/invite/jorbs) in *#jorbs-spire-mod-char* - someone there will give you a hand!*

This project uses GitHub Pull Requests to handle merging contributed changes. If you're new to using GitHub or Pull Requests, here's the TL;DR for the workflow I like to use:

### First-time setup

1. Create your own fork of this repository by clicking the "Fork" button at the top right of this page (you'll need a GitHub account)
1. [Install Git](https://git-scm.com/downloads)
1. From a command prompt, run the following (replace `your_username` with your GitHub username):
    ```sh
    cd C:/path/to/code
   
    git clone --origin upstream https://github.com/dbjorge/jorbs-spire-mod.git
    cd jorbs-spire-mod
   
    git remote add my_fork https://github/your_username/jorbs-spire-mod.git
   
    git config --global alias.newfeature "!git checkout master && git pull && git checkout -b"
    git config --global alias.pushtofork "!git push --set-upstream my_fork HEAD"
    ```

### Each time you want to start a new feature/contribution...

1. (recommended) Discuss your idea on the [Discord #jorbs-spire-mod-char channel](https://discord.gg/invite/jorbs) first, to make sure noone else is already working on the same thing
1. Run `git newfeature my-cool-feature-name`
1. Make your code changes, build and test locally
1. Use `git add *` and `git commit -m 'description of changes'` to make *local* commits

### When you're ready to submit your changes to be reviewed and merged...

1. Run `git pushtofork` from your feature branch
1. [Create a Pull Request on GitHub](https://github.com/dbjorge/jorbs-spire-mod/compare)