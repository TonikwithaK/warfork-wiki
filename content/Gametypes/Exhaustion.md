---
title: Exhaustion
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Exhaustion
---

Exhaustion is a gametype created by msc and Asbestos.
There are no pickups and you spawn with all weapons, but each time you die it takes longer for you to respawn. Once an entire team is waiting to respawn, the opposing team gets a point, this goes on until the maximum amount of points is reached and one team is declared the winner.

Exhaustion is a community-created game type made by msc and Asbestos.

## Tips

- When you are the last person alive, you're encouraged to run away until a teammate respawns.

## Default rules

<table>
<thead>
<tr>
<th>Rule</th>
<th>State</th>
</tr>
</thead>
<tbody>
<tr>
<td>Team-based</td>
<td><figure>
<img src="Yes.png" title="Yes.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Team damage</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Item pickups</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Points awarded for</td>
<td>Eliminating the enemy team</td>
</tr>
<tr>
<td>Fall damage</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Self damage</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Starting health</td>
<td>100</td>
</tr>
<tr>
<td>Starting armor</td>
<td>150 (0 for <a href="Instagib" class="wikilink" title="Instagib">Instagib</a>)</td>
</tr>
<tr>
<td>Respawning mid-game</td>
<td><img src="Yes.png" title="Yes.png" width="24" alt="Yes.png" />*</td>
</tr>
<tr>
<td>Time limit</td>
<td>0</td>
</tr>
<tr>
<td>Score limit</td>
<td>11</td>
</tr>
<tr>
<td>Overtime</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Starting weapons</td>
<td>![[Gunblade_blast.png]]![[Machinegun.png]]<img src="Riot.png" title="Riot.png" width="24" alt="Riot.png" />![[Grenade.png]]<img src="Rocket.png" title="Rocket.png" width="24" alt="Rocket.png" /><img src="Plasma.png" title="Plasma.png" width="24" alt="Plasma.png" />![[Laser.png]]![[Electro.png]]
![[Instagun.png]] (<a href="Instagib" class="wikilink" title="Instagib">Instagib</a> only)</td>
</tr>
<tr>
<td>Starting ammo / Max ammo</td>
<td>![[Bulletsammo.png]]75/75, <img src="Riotammo.png" title="Riotammo.png" width="24" alt="Riotammo.png" />15/15,
![[Grenadeammo.png]]20/20, <img src="Rocketammo.png" title="Rocketammo.png" width="24" alt="Rocketammo.png" />20/20
<img src="Plasmaammo.png" title="Plasmaammo.png" width="24" alt="Plasmaammo.png" />125/125, ![[Laserammo.png]]140/140
![[Electroammo.png]]10/10</td>
</tr>
<tr>
<td>Stunning</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Challengers Queue</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
</tbody>
</table>

### Notes

- Each person starts with a 5 second respawn delay. The formula for calculating the next respawn time is *(d+1)\*t* where *d* stands for the amount of deaths and *t* stands for standard respawn delay (5 by default).

### Item respawn times

<table>
<thead>
<tr>
<th>Item</th>
<th>Time</th>
</tr>
</thead>
<tbody>
<tr>
<td>Ammo respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Armor respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Weapon respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Health respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Powerup respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Mega Health respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
<tr>
<td>Ultra Health respawn time</td>
<td><figure>
<img src="No.png" title="No.png" width="24" />

</figure></td>
</tr>
</tbody>
</table>

## Game type-exclusive information

### Commands and cvars

| Command | Default | Parameters | Description |
|----|----|----|----|
| g_ca_timelimitlvl | 60 | \<value\> | Time (in seconds) how long do 1v1 fights last before ending up with a tie. |
| g_noclass_inventory | gb mg rg gl rl pg lg eb cells shells
grens rockets plasma lasers bullets | \<weapons, ammo\> | Starting weapons and ammo packs. |
| g_class_strong_ammo | 1 75 20 20 40 125 180 15 | \<amount\> | Amount of starting ammo for weapons. |
| g_wipeout_delay | 5 | \<value\> | Standard respawn delay (in seconds). |
| g_wipeout_teamdelay | 0 | \<0/1\> | If enabled, players' respawn timers will be replaced with team respawn timer. |

### Callvotes

| Vote      | Parameters | Description                                |
|-----------|------------|--------------------------------------------|
| teamdelay | \<0/1\>    | Modifies the value of g_wipeout_teamdelay. |
| delay     | \<value\>  | Modifies the value of g_wipeout_delay.     |
