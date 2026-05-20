---
title: Server Administration
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Server_Administration
aliases:
- Server_Administration
---

## RCON Commands

RCON (Remote Console) allows client console commands to be issued to the server remotely for administration purposes, without the need to directly connect to the machine.
Since Warfork uses the Qfusion engine, which is a fork of ID Tech 2 (known as the Quake 2 engine) you might notice the similarities.

To issue RCON commands you must open your client console and login (**see below**). If you're hosting a Local Game then you don't need to login or prefix each command with 'rcon'. Please only share your RCON password with those you trust.

<table>
<thead>
<tr>
<th>Command</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>rcon_password "&lt;rconpassword&gt;"</strong></td>
<td><strong>Logs you into RCON so you can execute the commands below.</strong></td>
</tr>
<tr>
<td>rcon status</td>
<td>Shows the Player ID and IP Address.</td>
</tr>
<tr>
<td>rcon kick &lt;playerid&gt;</td>
<td>Kicks the Player with the specified &lt;playerid&gt;.</td>
</tr>
<tr>
<td>rcon map &lt;mapname&gt;</td>
<td>Changes the map to the specified &lt;mapname&gt;.</td>
</tr>
<tr>
<td>1. rcon addip &lt;playerip&gt;
<code>2. rcon writeip </code><br />
<code>3. rcon kick &lt;playerid&gt;</code></td>
<td>Bans a Player after you perform a series of commands.
<code>1. Adds the IP to the banlist. </code><br />
<code>2. Writes the IP to the banlist. </code><br />
<code>3. Kicks the Player from the server. </code></td>
</tr>
</tbody>
</table>

## Scripts

There are a number of scripts to make your life easier:

| Name | Description | Author |
|----|----|----|
| [*Warfork Version Manager*](https://github.com/Warfork/wvm) | Simple way to install any version of Warfork FPS on your Linux machine. Use it to play any version of the game with different profiles, or to run multiple isolated servers with different configs! | stylemistake |
| [*Warfork Tool*](https://github.com/Warfork/wf_tool) | A tool for maintaining warfork servers. | psymin |
|  |  |  |
