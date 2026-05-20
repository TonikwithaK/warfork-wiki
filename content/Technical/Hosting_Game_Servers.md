---
title: Hosting Game Servers
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Hosting_Game_Servers
aliases:
- Hosting_Game_Servers
---

Ubuntu: [[Server Install On Ubuntu|click here!]]
Linux: [[Babitz guide|click here!]]
*This guide contains a minimal amount of information needed to configure and start the server correctly. Visit [[Console Commands]] for detailed configuration. Details on how to manage a server can be found [[Server Administration|here]]. An extended version of this guide can be found [here](https://steamcommunity.com/sharedfiles/filedetails/?id=1939995111).*

## Getting started

To host a Warfork server, you need to forward ports 44400 (UDP) and 44444 (TCP) and you need to have the base game [[Getting Started#Where can I download Warfork from.3F|downloaded]] (it contains a dedicated server).
The server executables are located in ***\steamapps\common\fvi\Warfork.app\Contents\Resources*** - ***wf_server_x64.exe**'' for a 64-bit version and***wf_server_x86.exe**'' for a 32-bit version.

## Configuration

**Windows:** *Configuration files can be found at **\steamapps\common\fvi\Warfork.app\Contents\Resources\basewf** for general server config, and **\Documents\My Games\Warfork 2.1\basewf\configs\server\gametypes** for gametype configs.*

The server configuration is stored in ***\basewf\dedicated_autoexec.cfg***. This file can be opened with any text editing software (Windows default notepad works too).
To modify the values of cvars, change the text between the quote marks. Do not remove any quotes from the file!
*Only the most important settings are listed below. For detailed configuration of your server and detailed descriptions of commands visit [[Console Commands]].*

    8 set sv_hostname "Warfork Server"
    9 set sv_ip ""              // set to bind to a specific interface IP address
    10 set sv_port "44400"
    11 set sv_port6 "44400"       // set a port for IPv6
    12 
    13 set sv_http "1"
    14 set sv_http_ip "" // set to bind to a specific interface IP address
    15 set sv_http_port "44444"

You need to fill *sv_ip* and *sv_http_ip* with your internal IP address (obtainable via ipconfig). You can change the ports here if you want to host multiple servers on a single machine. *sv_hostname* is the name of the server which is displayed on the server browser.

    138 set g_gametype "ca"

Changes the gametype of your server. Valid options are available [[Gametypes|here]] (click a gametype to obtain its short name).

    142 set g_instagib "0"

Toggles instagib setting. Cannot be changed with callvotes.

    160 set sv_defaultmap "wfdm1"

Changes the map the server loads upon startup.

## Starting the server

Save your custom configuration. To start a server, launch one of the server executables. If everything is configured right, the server will start successfully and send two heartbeats (if sv_public is set to 1).

### Connecting to your server

There are 3 ways you can connect to your own server:

1.  Execute *connect \<privateip\>* in console
2.  Execute *connect \<publicip\>* in console
3.  Join your server from server browser

Others can connect to the server either by finding it on a server browser or connecting directly to your public IP. *Note: Your server won't appear on the server browser if sv_public is disabled.*
