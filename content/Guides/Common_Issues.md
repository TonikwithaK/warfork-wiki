---
title: Common Issues
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Common_Issues
aliases:
- Common_Issues
---

## My screen is blank when I open Warfork

This generally means your video card cannot run Warfork with its default configuration settings. The following solutions may fix this problem:
\# Add the following to game properties in Steam: `+exec profiles/ultralow`

1.  Update your video card drivers

## The game won't display on any of my screens

Try checking the config file in your documents folder, and search for this line `seta vid_multiscreen_head` . If it is set to "-1" then you will want to try changing it to 1 or 2 based on what is your main monitor.

If that doesn't help, search for lines `seta vid_xpos` and `seta vid_ypos` and set them to `"0"` as the game window may just be created off screen

## I'm seeing "pure check failed" when a server I connect to attempts to download a map.

There are multiple reasons why pure check could fail. This error message means the file on client's PC doesn't match with server's.
The following solutions may fix this problem:

1.  Add *`+set fs_usehomedir 0`* to Warfork's launch options on Steam.
2.  Remove all downloaded files. More information can be found [[Getting Started#Where do I find my configuration file.2C demos.2C screenshots and more.3F|here]].
3.  (Server admin only) Disable [[Console Commands#sv|sv_pure]] *(Not recommended on public servers)*

## How do I increase my FPS limit?

`cl_maxfps` and `r_maxfps` are responsible for the limit. They can be changed by using the [[Console]], or using the graphical menus (options-\>video-\>"Framerate (FPS) limit". The maximum FPS limit is 1000.

## I don't have Steam and\or don't want to use it. Where can I download Warfork?

See anonymous steamcmd download [[Frequently Asked Questions#Where can I download Warfork from.3F|Frequently Asked Questions#Where can I download Warfork from?]]

## Does a 32-bit version exist?

32-bit version of Warfork can be found in the game files.

## Is it possible to change weapon models?

It will be soon.

## Does Warfork have a max acceleration HUD like in defrag?

Defrag had such command like cgaz_hud
<https://i.ytimg.com/vi/uIFO4wB3bwo/maxresdefault.jpg>

not quite the same but cg_strafehud 1 is a strafe helper
ale's race hud can show accel and there are some other custom ones with it
i don't have links

## I created a game and I want to play with a friend, but how can he join me?

Warfork requires ports 44400 (UDP) and 44444 (TCP) to be forwarded. More information about server hosting can be found [[Hosting Game Servers|here]].

## How to remove the gray text while spectating?

Type *[[Console Commands#cg|cg_showhelp]] 0* in [[Console]].

## How do I make my own map?

You use a tool called NetRadiant. Most tutorials for Warsow, Quake 3, and GTKRadiant will be extremely similar. The Warfork files you need for NetRadiant can be found here - <https://cdn.discordapp.com/attachments/611741789237411850/659512520553267201/netradiant_warfork_gamepack.zip>
<https://en.wikibooks.org/wiki/NetRadiant>
<https://github.com/xonotic/xonotic/wiki/Netradiant>
<http://ingar.intranifty.net/gtkradiant/>
<https://slice.sh/warsow/oldwiki/IndexDocument.html> - In the Development section there are some relevant pages
<https://ws.q3df.org/level_design/> - Very detailed tutorial for quake 3 map-making

## Is there a way to set chat binds?

bind f say_team blablabla /bind f say blablabla / bind f vsay goodgame blablabla / bind f vsay_team goodgame blablabla / you can bind the voicemessages somewhere in the menu
might be that you need to put quotes around the actual command (like bind f "say_team blablabla")

## For some reason the players all turn the textures black around them when they are near me.

Here's an example: <https://i.imgur.com/OgOaWMu.png>
Hm, so turns out it's not just one server. So far the only servers I've had the issue on have been FFA ones. Here's another example: <https://i.imgur.com/8PirdXl.png>

you probably downloaded some pk3 that breaks it deleting or renaming that should work you'll have to redownload maps

undo that and only delete basewf/cache but not the basewf in downloads there is one above that

## warfork opengamepanel config?

if it has a q3 config that might work nevermind probably not

## where can I find the (script) files for official gamemodes?

pure pk3 file

## How do I make a custom gamemode?

## Should I modify pk3 files?

don't modify the pk3s

## How do I read or\extract PK3 files?

PK3 files are compressed using Zip compression. We recommend you use 7-Zip: <https://7-zip.org/download.html>

## How do I disable Steam Cloud synchronization for Warfork?

1.  Open your Steam game library.
2.  Search for Warfork.
3.  Right click on Warfork and select "Properties".
4.  Click the "Updates" tab.
5.  Uncheck "Enable Steam Cloud synchronization for Warfork".
6.  Click "Close".
