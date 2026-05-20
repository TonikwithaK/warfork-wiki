---
title: Frequently Asked Questions
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Frequently_Asked_Questions
aliases:
- Frequently_Asked_Questions
---

***Important links:***
***[[Help/Editing|Editing guidelines]]**''\***
[[Rules|Wiki rules]]**''

## Where can I download Warfork from?

For Desktop OSes: Warfork can be downloaded from [Steam](https://store.steampowered.com/app/671610/Warfork/).
For Linux servers: Warfork can be downloaded via [SteamCMD](https://developer.valvesoftware.com/wiki/SteamCMD) (AppID 671610 (requires logging in) / 1136510 (no login required)).

Note that appid 1136510 contains client binaries/resources and can be used to download Warfork without steam authentication, for windows and linux both.

Example steamcmd interactive session, once you launched `steamcmd`

``` sh
force_install_dir typeyourpathhere
login anonymous
app_update 1136510
```

You may want to specify an actual directory path instead of `typeyourpathhere`.

## Where can I report bugs / issues?

Any bugs, issues or problems related to Warfork can be reported on our [Discord](https://discord.gg/VY95TKZ).

## Where can I find my configuration file, demos, screenshots and other?

| Operating System | Path                                                    |
|------------------|---------------------------------------------------------|
| Windows          | %USERPROFILE%/My Documents/My Games/Warfork 2.1/basewf/ |
| Mac              | ~/Library/Application Support/Warfork-2.1/basewf/       |
| Linux            | ~/.local/share/warfork-2.1/basewf/                      |

## How can I host a server? / My server isn't appearing on the server browser! What do I do?

Follow [[Hosting Game Servers|this]] guide.

## How do I put colors in my player name?

![[Colors.jpg]]

Colors in-game

| Code | Color  |
|------|--------|
| ^0   | Black  |
| ^1   | Red    |
| ^2   | Green  |
| ^3   | Yellow |
| ^4   | Blue   |
| ^5   | Cyan   |
| ^6   | Purple |
| ^7   | White  |
| ^8   | Orange |
| ^9   | Gray   |

Color Codes
