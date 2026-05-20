---
title: Health
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Health
---

Health is one of the most important player statistics in Warfork. It determines how much damage player can receive before death. The amount of health a player has is commonly referred as HP (Health Points). Current player's health is shown in the bottom left corner (default HUD).
The default amount of health players start with is 100, however it can vary depending on the game type. 100 HP is also the default HP limit, however it's possible to have up to 200 HP by using overhealing items (see: <a href="Health#Overhealing" class="wikilink" title="Overhealing">Overhealing</a>).

Players can lose health by taking various types of damage (like <a href="Weapons#Damage_Definitions" class="wikilink" title="weapon damage">weapon damage</a>), and can also gain health by collecting health items.

When health drops to (or below) 0, the player dies.

## Colors

![[Hp_bars.jpg|Colors of Health bars]]
The health bar changes color depending on the amount of health a player has. The colors are:

\<25 HP - red

25-49 HP - orange

50-74 HP - yellow

75-99 HP - white

100 HP - blue

\>100 HP - purple

## Health items

![[Hp5.jpg|Five 5HP health items next to each other on <a href="wfda4" class="wikilink" title="wfda4">wfda4</a>]]
![[Hp5s.jpg|Simple items enabled]]
Warfork features health items that restore your HP. There are 5 different health items.

<table>
<thead>
<tr>
<th>Item</th>
<th>In-game name</th>
<th>HP amount</th>
<th>Can overheal</th>
</tr>
</thead>
<tbody>
<tr>
<td>![[5.png]]</td>
<td>5 Health</td>
<td>5</td>
<td>Yes</td>
</tr>
<tr>
<td>![[25.png]]</td>
<td>25 Health</td>
<td>25</td>
<td>No</td>
</tr>
<tr>
<td>![[50.png]]</td>
<td>50 Health</td>
<td>50</td>
<td>No</td>
</tr>
<tr>
<td>![[100.png]]</td>
<td>Mega Health</td>
<td>100</td>
<td>Yes</td>
</tr>
<tr>
<td>![[100ultra.png]]</td>
<td>Ultra Health</td>
<td>100</td>
<td>Yes</td>
</tr>
</tbody>
</table>

## Simple items

Health items' appearance is affected by *Simple items (<a href="Console_Commands#cg" class="wikilink" title="cg_simpleitems">cg_simpleitems</a>)*. If simple items are enabled, the 3D models of health items will be replaced with simplistic 2D models. This has no effect on gameplay, it's purely visual. Some players might prefer to use simple items for better visibility. Simple items can be enabled either by typing *cg_simpleitems 1* into the console or by going to *Options -\> Player -\> Misc* and enabling *Simple items*.

## Default behavior of health items

- Health items have their own respawn times, however the 5, 25 and 50 Health items use the same timer
- Health items are automatically collected when a player walks into them
- Health items aren't collected if a player has maximum amount of HP
- Respawn times depend on the game type
- Mega health's respawn timer starts when the health of the player who picked it up last drops to 100 HP
- Ultra health's respawn timer starts immediately after picking it up
- Certain game types (like Clan Arena) have health items disabled

## Overhealing

Some healing items can overheal a player (check the table above). Overhealing items ignore the default 100 HP limit and can overheal the player up to 200 HP. Examples:

- 74 HP + Mega Health = 174 HP
- 98 HP + 5 Health = 103 HP
- 150 HP + Ultra Health = 200 HP

Overhealed health points aren't permanent unlike normal health points. They decay at a rate of 1 HP / second, until the player is back to 100 HP.

## Tips

- Keep an eye on the health bar. If your health is running low, make sure to replenish it before jumping into the battlefield.
- Don't let enemies collect health items during a battle against them, it drastically increases their chances of survival.
