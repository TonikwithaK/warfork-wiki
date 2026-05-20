---
title: Server Install On Ubuntu
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Server_Install_On_Ubuntu
aliases:
- Server_Install_On_Ubuntu
---

*This guide contains a minimal amount of information needed to install the server correctly. Visit [[Console Commands]] for detailed configuration. Details on how to manage a server can be found [[Server Administration|here]].*

## Requirements

This guide assumes you are running **Ubuntu 20.04** (the latest Ubuntu LTS at the time of writing).

## Installing Dependencies

The following commands can be pasted into your terminal to ensure the minimum dependencies are installed:

    # Update package cache
    sudo apt update

    # Install dependencies (this is likely more than is necessary)
    sudo apt install -y --no-install-recommends 
        lib32gcc1 
        lib32stdc++6 
        wget 
        ca-certificates 
        rsync 
        unzip 
        tmux 
        jq 
        bc 
        binutils 
        ca-certificates 
        util-linux 
        python 
        curl 
        wget 
        file 
        tar 
        bzip2 
        gzip 
        unzip 
        bsdmainutils 
        libcurl4 
        libcurl3-gnutls 
        libcurl4-gnutls-dev

## Creating the installation directories

The following commands can be pasted into your terminal to create the directories/links that will be used to store SteamCMD and Warfork:

    # Make sure ~/.local/share/ exists
    mkdir -p ~/.local/share/

    # Symlink the eventual installation directory to ~/.local/share/warfork-2.1
    ln -s ~/server/Warfork.app/Contents/Resources ~/.local/share/warfork-2.1

    # Create directory for SteamCMD install
    mkdir ~/Steam

    # Create directory for Warfork install
    mkdir ~/server

## Installing SteamCMD

    # Change directory into the directory in which you'll install SteamCMD
    cd ~/Steam

    # Download SteamCMD installer
    wget -qO- https://steamcdn-a.akamaihd.net/client/installer/steamcmd_linux.tar.gz | tar zxf -

    # Install SteamCMD
    ~/Steam/steamcmd.sh +quit

## Installing Warfork

    # Install Warfork
    ~/Steam/steamcmd.sh +login anonymous +force_install_dir ~/server +app_update 1136510 validate +quit

## Configuring the server

At this point, you'll want to follow the **Configuration** section from the [[Hosting Game Servers#Configuration|Hosting Game Servers]] page. Visit [[Console Commands]] for detailed configuration.

Once configured, you can proceed with the next sections:

## Starting the server

    # Run Warfork
    ~/server/Warfork.app/Contents/Resources/wf_server.x86_64

## Updating the server

    # To update Warfork:
    ~/Steam/steamcmd.sh +login anonymous +force_install_dir ~/server +app_update 1136510 +quit

## Installation demo

<https://asciinema.org/a/u7PFRfIYNJow6jC2JrIoOoyWk>
