---
title: TV Servers
namespace: ''
original_url: https://warforkwiki.com/index.php?title=TV_Servers
aliases:
- TV_Servers
---

The TV Servers are servers that allow spectators to watch either a public game or private game without the ability of users to interfere with the main game keeping the lag to a minimum.

## Configure

Default config Warfork.app/Contents/Resources/basewf/tvserver_autoexec.cfg

    seta logconsole "tvconsole.log"
    seta logconsole_append "1"

    //set tv_password "password" // password for users to join this TV server
    set tv_udp "1" // Allow use of UDP port to connect
    set tv_tcp "1" // Allow use of TCP port to connect
    set tv_ip "" // set to bind to a specific interface IP address
    set tv_ipv6 "::"
    set tv_port 44440
    set tv_port6 44440
    //set tv_rcon_password "10203040" // remote administration password. Blank for disallowed
    seta tv_name "TV_Server"
    seta tv_maxclients "64"
    seta tv_chasemode "6" // default chas cam mode for spectators
    seta tv_autorecord "" // default to none

    set masterserver "master1.forbidden.gg master1.icy.gg:
    set masterservers_steam ""
    //Execute wftv_server and type in the console : connect IP:port of the
    //server you want to stream.
    //It is capable of streaming more than one server at once.
    //It can also be executed like: "wftv_server +connect ip:port" or "wftv_server +tcpconnect ip:port"

## Commands

| Commands | Paramaters | Description/Example |
|----|----|----|
| connect | \<ip/hostnane\>\[:port\] \[password\] \[name\] \[delay\] | Password is not in a string; Name is the one that displays on the display list of servers to spectate; Delay is the delay of seconds from the server; "connect 127.0.0.1:44400 Password LocalServer 10" |
| demo | \<pattern\|playlist\> \[name\] \[ordered\|random\] \[delay\] | Name is the one that displays on the display list of servers to spectate; Delay is the delay of seconds from the server; WIP |
| status | N/A | Displays current Upstream Connections and Downstream connections |

## Parameters

    Example command to run a TV server 
    ./wftv_server.Arch +connect 127.0.0.1:44400 Password LocalServer 10

| Commands | Paramaters | Description/Example |
|----|----|----|
| +connect | \<ip/hostnane\>\[:port\] \[password\] \[name\] \[delay\] | Password is not in a string; Name is the one that displays on the display list of servers to spectate; Delay is the delay of seconds from the server; "+connect 127.0.0.1:44400 Password LocalServer 10" |
| +exec | \[config name\] | Change which config file to load in /Resources/basewf "+exec tvserver_autoexec.cfg" |
