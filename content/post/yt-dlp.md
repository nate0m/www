+++
title = 'Music On Andriod'
date = 2025-12-22T10:41:46-08:00
draft = false
+++

# Installing Music On Andriod (YT-DLP)
This method allows you to download music from yt-music using yt-dlp with all of the meta data embedded into an mp3 file like track number, artist, and album art. Then easily access it using Musicolet. Resulting in an extremely functional, pretty, and offline music listening experience.

## Application Installations

- Install [Musicolet](https://play.google.com/store/apps/details?id=in.krosbits.musicolet) from the Play Store
- Install [F-Droid](https://f-droid.org/) from your browser 
- Install [Termux](https://f-droid.org/packages/com.termux/) from F-Droid

## Termux Setup
- Launch Termux
- Run the command `termux-setup-storage` to initalize the file structure, follow the permissions prompts
- Run the command `mkdir .bin` to make a directory where you will place the script
- Run the command `pwd .bin` and save path that is output for later
- Run the command `pkg install curl git vim yt-dlp zsh -y`, to install the necessary packages
- Run the command `sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`, to install oh-my-zsh; say Yes to setting Zsh as default, *Zsh allows for the use of the tab button for ez autocomplete*
- Run the command `vim .zshrc`, [learn how to use vim](https://youtu.be/-txKSRn0qeA?si=WmhSCQRv3HkdOrOU) and change the theme to `ZSH_THEME=bira`, at the top of the file paste the following line `export PATH="$PATH:/path/to/script/directory"`, replace the path with the path to the scrip from earlier something like `export PATH="$PATH:/data/data/com.termux/files/home/.bin"`

## Install Script
- Go [here](https://github.com/nate0m/script-repo/blob/main/yt-dl-mus) and copy the this script to your clip board
- Run the command `vim .bin/yt-mus` and paste the script into there, and save and exit
- Run the command `chmod +x .bin/yt-mus`, to make the script executable
- Run the command `source .zshrc` to refresh your terminal

## Downlaoding Music
- Run the command `cd Music`, to move to the music directory
- Run the command `yt-mus https://yt-music-link` to download individual songs
- Run the command `yt-mus -p https://yt-music-album-lin;` to download an album or playlist

## Musicolet Setup
- Open Musicolet and set the source directory to the Music directory that you downloaded the music to
- Run a system scan from the three dot menu whenever you still more music and don't see it in your library

If you end up liking Musciolet consider supporting the creator by purchasing the premium upgrade.
