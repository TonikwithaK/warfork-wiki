---
title: Calling Votes
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Calling_Votes
aliases:
- Calling_Votes
---

Warfork has a voting system built-in that lets players change certain server settings, punish misbehaving players and modify game rules.

## Types of votes

Warfork has multiple votes by default. Some gametypes have their own votes.
Default Warfork votes:

<table>
<thead>
<tr>
<th>Vote</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>allow_falldamage</td>
<td>&lt;0/1&gt;</td>
<td>Toggles fall damage. 0 - disabled, 1 - enabled.</td>
</tr>
<tr>
<td>allow_selfdamage</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, players can hurt themselves with their own weapons. 0 - disabled, 1 - enabled.</td>
</tr>
<tr>
<td>allow_teamdamage</td>
<td>&lt;0/1&gt;</td>
<td>Toggles friendlyfire. 0 - disabled, 1 - enabled.</td>
</tr>
<tr>
<td>allow_uneven</td>
<td>&lt;0/1&gt;</td>
<td>Allows the teams to be uneven. If enabled, allows players to switch teams anytime. 0 - disabled, 1 - enabled.</td>
</tr>
<tr>
<td>allready</td>
<td></td>
<td>Makes all players ready, thus forcing a match to start. Only works during warmup.</td>
</tr>
<tr>
<td>extended_time</td>
<td><time></td>
<td>Changes the overtime's length to x minutes. 0 to disable.</td>
</tr>
<tr>
<td>gametype</td>
<td>&lt;gametype&gt;</td>
<td>Changes the gametype. Resets the match.</td>
</tr>
<tr>
<td>instajump</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, Instagun can be used for weapon jumping (Instagib only).</td>
</tr>
<tr>
<td>instashield</td>
<td>&lt;0/1&gt;</td>
<td>Enables Instashield (Instagib only).</td>
</tr>
<tr>
<td>kick</td>
<td>&lt;player&gt;</td>
<td>Kicks a player from the server.</td>
</tr>
<tr>
<td>kickban</td>
<td>&lt;player&gt;</td>
<td>Bans a player's IP address for 15 minutes.</td>
</tr>
<tr>
<td>lock</td>
<td></td>
<td>Locks the teams so that noone else can join during the game (doesn't affect warmup).</td>
</tr>
<tr>
<td>map</td>
<td>&lt;map&gt;</td>
<td>Changes the map.</td>
</tr>
<tr>
<td>maxteamplayers</td>
<td>&lt;value&gt;</td>
<td>Changes how many players can a single team have.</td>
</tr>
<tr>
<td>mute</td>
<td>&lt;player&gt;</td>
<td>Mutes a player. Prevents them from using text chat.</td>
</tr>
<tr>
<td>nextmap</td>
<td></td>
<td>Changes the current map to the next one from map rotation list.</td>
</tr>
<tr>
<td>numbots</td>
<td>&lt;value&gt;</td>
<td>Changes the amount of bots on the server. 0 to disable.</td>
</tr>
<tr>
<td>rebalance</td>
<td></td>
<td>Rebalances teams (based on the stats). Wipes player stats.</td>
</tr>
<tr>
<td>remove</td>
<td>&lt;player&gt;</td>
<td>Puts a player into Spectators team.</td>
</tr>
<tr>
<td>restart</td>
<td></td>
<td>Restarts the match.</td>
</tr>
<tr>
<td>scorelimit</td>
<td></td>
<td>Sets the amount of points required to obtain by a player / team to end the match.</td>
</tr>
<tr>
<td>shuffle</td>
<td></td>
<td>Shuffles teams. Wipes player stats.</td>
</tr>
<tr>
<td>timein</td>
<td></td>
<td>Resumes a match. Only works during timeouts.</td>
</tr>
<tr>
<td>timelimit</td>
<td>&lt;value&gt;</td>
<td>Sets the duration of matches (in minutes).</td>
</tr>
<tr>
<td>timeout</td>
<td></td>
<td>Pauses a match for 180 seconds.</td>
</tr>
<tr>
<td>unlock</td>
<td></td>
<td>Unlocks teams so other players can join during the game.</td>
</tr>
<tr>
<td>unmute</td>
<td>&lt;player&gt;</td>
<td>Unmutes a player. Allows them to use text chat.</td>
</tr>
<tr>
<td>vmute</td>
<td>&lt;player&gt;</td>
<td>Mutes player's voice commands.</td>
</tr>
<tr>
<td>vunmute</td>
<td>&lt;player&gt;</td>
<td>Unmutes player's voice commands.</td>
</tr>
<tr>
<td>warmup_timelimit</td>
<td>&lt;value&gt;</td>
<td>Sets how long do warmups take (in minutes). 0 to make warmups infinite.</td>
</tr>
</tbody>
</table>

## Calling votes

<img src="Votepanel.jpg" title="HUD Vote panel" width="128" alt="HUD Vote panel" />
There are two ways of calling a vote: using HUD and using the console.

Calling votes using the HUD is easy and straightforward. Some players prefer to use the console, which allows utilizing opcalls.

### HUD

To call a vote using HUD, click the Escape key once you're in-game and then Call a vote button.

A window with available callvotes will appear.

To call a vote, choose one of them, fill the argument if present and click Call a vote.

### Console

It's a bit tricker to call votes from the console because you need to type both the vote name and the optional argument, however it also lets you see the current value of a certain command unlike the HUD option and lets you utilize opcalls.

Click \` to open the console. Type *callvote* and hit Enter to access the list of votes.

To call a vote, type *callvote* followed by a name of the callvote and an optional argument: *callvote \<name\> \[argument\]*.

Examples:

- callvote map wfca1
- callvote mute Player
- callvote allow_uneven 1
- callvote gametype dm
- callvote numbots 5
- callvote nextmap
- callvote rebalance

#### Custom callvotes

Some gametypes have custom votes, which aren't stated in the Types of votes section. They appear at the top of the list when *callvote* is executed.
Same syntax applies to custom votes: *callvote \<name\> \[argument\]*.

#### Tips

The console method lets you view the current value of certain commands. If you type the name of the vote without additional arguments, it'll show you the current value it's set to. For example, *callvote allow_uneven* will display the current value, same with any other vote that has an argument.

You can view the list of maps you can vote on with *callvote map*, as long as you execute the command with no additional parameter.

Typing *vote yes* or *vote no* in the console lets you submit a vote without having to bind two separate keys for those actions.

#### Opcalls

Opcalls are special votes that can only be called by game operators. They have one major difference - they always pass immidiately. They're used by server operators to enforce server rules and punish rulebreakers instantly. To use opcalls, you first need to become an operator. The syntax is identical to callvote, examples:

- opcall map wfca1
- opcall mute Player
- opcall allow_uneven 1
- opcall gametype dm
- opcall numbots 5
- opcall nextmap
- opcall rebalance

##### Tips

Opcall has an ability to pass and cancel pending votes. To do so, type *opcall passvote* or *opcall cancelvote*.

## Default rules of voting system

- Voting system: Enabled
- Delay between votes: 5 seconds
- Callvotes last for: 20 seconds
- Maximum amount of yes/no changes: 3
- Percentage required for vote to pass: 55%
- All votes are allowed by default

## Additional information & bugs

- Server administrators can set their own rules of votes via *g_vote\_\** cvars and disable voting system, doing so also disables opcalls.
- Server operators cannot be kicked or kickbanned. However operators can still get muted by other players if they act fast enough.
- Server operators can kick or kickban themselves by starting a vote as a regular player against themselves, then becoming an operator and passing the vote with *opcall passvote*.
- Server administrators can disable specific votes one by one by setting *<a href="Console_Commands#g" class="wikilink" title="g_disable_vote_*">g_disable_vote_*</a> 1* where \* stands for the name of vote(s). Disabling votes this way doesn't affect opcalls.
- There are separate variables that can disable opcalls (*<a href="Console_Commands#g" class="wikilink" title="g_disable_opcall_*">g_disable_opcall_*</a> 1*).
