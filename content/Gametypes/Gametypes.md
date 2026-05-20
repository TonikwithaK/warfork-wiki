---
title: Gametypes
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Gametypes
---

A gametype is a set of game rules that makes for a unique gameplay. Warfork has 13 gametypes by default. The full list of gametypes can be seen on the [[Main Page]]. Gametypes can be changed by typing *[[Console Commands#g|g_gametype]] \<gametype\>* into the console.

## Custom gametype installation

Custom gametypes can be installed by putting the specific gametype files in *Warfork.app/Contents/Resources/basewf/progs/gametypes*. Gametype files come with 3 different file extensions: .as (scripts), .gt (list of script files to load) and optional .gtd (gametype description). All gametypes are coded in *AngelScript* language, which is a scripting language used in Warfork and is similar to C.

## Additional information

- Stock gametypes aren't available in *progs/gametypes* folder. They're located in *Warfork.app/Contents/Resources/basewf/data0_21pure.pk3* file, which is a zip archive and thus can be opened with most file archiving software.
- Stock gametypes take priority while the game is loading. This means if a player puts a gametype for example called *Duel* in *progs/gametypes*, the game will not load the custom gametype and will load the stock one located in *data0_21pure.pk3* instead.
- If a player wants to modify a stock gametype, they have to change the name of it to prevent the game from loading the stock one. Do not modify the *data0_21pure.pk3* file!
- Gametypes are commonly called gamemodes.
- Most stock gametypes use GPL v2 license.
