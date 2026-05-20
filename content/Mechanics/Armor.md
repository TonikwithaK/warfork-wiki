---
title: Armor
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Armor
---

Armor is the second most important player statistic in Warfork. Armor absorbs most of the damage received, thus letting players survive longer during battles. Current player's Armor Points (AP) are shown in the bottom left corner above health (default HUD). Players can lose AP by taking various types of damage, and can also gain AP by collecting Armor items. It's possible to collect up to 200 AP. Armor bar is hidden if the player doesn't have any armor. The amount of armor players respawn with depends on the game type.

## Colors

![[Armor_bars.jpg|Colors of Armor bars]]
The armor bar changes color depending on the amount of armor a player has. The colors are:

\<100 AP - green

100-124 AP - yellow

\>124 AP - red

## Armor items

![[A7.jpg|Seven armor shards next to each other on <a href="Wfda1" class="wikilink" title="wfda1">wfda1</a>]]
![[A7s.jpg|Simple items enabled]]
Warfork features armor items that give AP upon collection. There are 4 different armor items.

<table>
<thead>
<tr>
<th>Item</th>
<th>In-game name</th>
<th>AP amount</th>
<th>Maximum armor</th>
</tr>
</thead>
<tbody>
<tr>
<td>![[Ga.png]]</td>
<td>Green Armor</td>
<td>50</td>
<td>100</td>
</tr>
<tr>
<td><figure>
<img src="Ya.png" title="Ya.png" width="60" />

</figure></td>
<td>Yellow Armor</td>
<td>75</td>
<td>125</td>
</tr>
<tr>
<td><figure>
<img src="Ra.png" title="Ra.png" width="60" />

</figure></td>
<td>Red Armor</td>
<td>100</td>
<td>150</td>
</tr>
<tr>
<td><figure>
<img src="Shard.png" title="Shard.png" width="60" />

</figure></td>
<td>Armor Shard</td>
<td>5</td>
<td>200</td>
</tr>
</tbody>
</table>

## Simple items

Armor items' appearance is affected by *Simple items (<a href="Console_Commands#cg" class="wikilink" title="cg_simpleitems">cg_simpleitems</a>)*. If simple items are enabled, the 3D models of armor items will be replaced with simplistic 2D models. This has no effect on gameplay, it's purely visual. Some players might prefer to use simple items for better visibility. Simple items can be enabled either by typing *cg_simpleitems 1* into the console or by going to *Options -\> Player -\> Misc* and enabling *Simple items*.

## Damage reduction

Armor reduces 2/3rd of the damage a player receives. For example if a player takes 1 damage, the armor takes 0.(6) damage and health takes 0.(3) damage. The armor and health values in <a href="HUD" class="wikilink" title="HUDs">HUDs</a> are rounded. Assuming a player has 100 AP and 100 HP: First damage point results in -1 AP from HUD (because 99.(3) AP rounded is 99 and 99.(6) HP rounded is 100). Second damage point results in -1 HP from HUD (because 98.(6) AP rounded is 99 and 99.(3) HP rounded is 99). Third damage point results in -1 AP from HUD (because 98.0 AP is 98 and 99.0 HP is 99).

## Default behavior of armor items

- All armor items use the same respawn timer
- Armor items are automatically collected when a player walks into them
- Armor items aren't collected if the player has more armor than the armor item's maximum
- Respawn times depend on the game type
- Certain game types (like Clan Arena) have armor items disabled

## Tips

- Unlike Health, Armor doesn't decay if a player has more than 100 AP. You can only lose armor by taking damage.
- Some HUDs show respawn timers for armor items. Those can be useful during battles.
- Make sure to grab some armor before joining a fight. It greatly increases your chances of survival.
- Armor color on the armor bar suggests what type of armor can be collected. If it's green, all types of armor can be collected. If it's yellow, only yellow and red armor can be collected. If it's red, only red armor can be collected. Armor shards can always be collected.
- You can collect up to 200 AP with armor shards. This combined with a lot of health makes a player very hard to kill.
