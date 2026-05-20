---
title: Console Commands
namespace: ''
original_url: https://warforkwiki.com/index.php?title=Console_Commands
aliases:
- Console_Commands
---

## Variables

### Flags

Variables in Warfork can have flags. Flags provide additional information about a variable.

- **\*** - Static variable. Changes to those variables are saved in config.cfg.
- **U** - User-info variable. Those variables are uploaded to the server (for example to let the server know the player's nickname).
- **S** - Server-info variable. Those variables are uploaded to all clients (for example to sync bot difficulty).
- **-** - Read-only variable. Those variables cannot be edited while the game is running. They can only be changed by starting Warfork with a launch option (for example *+<a href="Console_Commands#g" class="wikilink" title="g_allow_bunny">g_allow_bunny</a> 0*).
- **L** - Variables with this flag require restart of a certain subsystem for the changes to apply.
- **C** - Cheat variable. Those variables can only be changed if <a href="Console_Commands#sv" class="wikilink" title="sv_cheats">sv_cheats</a> is enabled.

#### Notes

- Variables can have more than one flag. They can also have none.

### Additional information

- Some commands / variables are server/client-sided. This means if a command is server-sided, then it can only be executed by the server (via server console / rcon). Executing those commands on the client's side will throw a "Unknown command" error.

### bot\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>bot_dummy</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, bots will be completely stationary and not fire any weapons.
<u>Example Screenshot:</u> <a href=":File:Bot_dummy1.jpg" class="wikilink" title="bot_dummy &quot;1&quot;">bot_dummy "1"</a></td>
</tr>
<tr>
<td>bot_showcombat</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, combat messages for bots will be displayed.
Chasecam and botdebug must be enabled as well for this command to work.
<u>Example Screenshot:</u> <a href=":File:Bot_showcombat1.jpg" class="wikilink" title="bot_showcombat &quot;1&quot;">bot_showcombat "1"</a></td>
</tr>
<tr>
<td>bot_showlrgoal</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the long range goals for bots will be displayed.
Chasecam and botdebug must be enabled as well for this command to work.
<u>Example Screenshot:</u> <a href=":File:Bot_showlrgoal1.jpg" class="wikilink" title="bot_showlrgoal &quot;1&quot;">bot_showlrgoal "1"</a></td>
</tr>
<tr>
<td>bot_showpath</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, a path will be drawn that the bot is following.
Chasecam and botdebug must be enabled as well for this command to work.
<u>Example Screenshot:</u> <a href=":File:Bot_showpath1.jpg" class="wikilink" title="bot_showpath &quot;1&quot;">bot_showpath "1"</a></td>
</tr>
<tr>
<td>bot_showsrgoal</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the short range goals for bots will be displayed.
Chasecam and botdebug must be enabled as well for this command to work.
<u>Example Screenshot:</u> <a href=":File:Bot_showsrgoal1.jpg" class="wikilink" title="bot_showsrgoal &quot;1&quot;">bot_showsrgoal "1"</a></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### cg\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>cg_autoaction_demo</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables automatic demo recording of matches after warmup mode is finished.
The demo will be written to /demos/autorecord/gametype/ in your <a href="Game_data_folder" class="wikilink" title="data folder">data folder</a> with the following file format: gametype_yyyy-mm-dd-hh-mm_map_playername_id.wdz20</td>
</tr>
<tr>
<td>cg_autoaction_screenshot</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables automatic screenshot of final standings on the scoreboard when the match is finished.
The screenshot will be written to /screenshots/ in your <a href="Game_data_folder" class="wikilink" title="data folder">data folder</a> with the following file format: wf_yymmdd_id.extension</td>
</tr>
<tr>
<td>cg_autoaction_spectator</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Use autoaction when spectating games.</td>
</tr>
<tr>
<td>cg_autoaction_stats</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, your <a href="Cg_autoaction_stats" class="wikilink" title="statistics">statistics</a> will be written to /stats/gametype/ in your <a href="Game_data_folder" class="wikilink" title="data folder">data folder</a> when the match is finished in following file format: gametype_yyyy-mm-dd-hh-mm_map_playername_id.txt</td>
</tr>
<tr>
<td>cg_bloodTrail</td>
<td>*</td>
<td>10</td>
<td>&lt;value&gt;</td>
<td>Changes the density of damage rings rendered when a player is hit.
0 = Disabled
<u>Example Screenshot:</u> <a href=":File:Cg_bloodTrail10.jpg" class="wikilink" title="cg_bloodTrail &quot;10&quot;">cg_bloodTrail "10"</a></td>
</tr>
<tr>
<td>cg_bloodTrailAlpha</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0-1&gt;</td>
<td>Sets the transparency of damage rings rendered.
0 = 100% Transparent &amp; 1 = 100% Solid
<u>Example Screenshot</u> <a href=":File:Cg_bloodTrailAlpha.jpg" class="wikilink" title="cg_bloodTrailAlpha &quot;0.3&quot;">cg_bloodTrailAlpha "0.3"</a></td>
</tr>
<tr>
<td>cg_cartoonEffects</td>
<td>*</td>
<td>7</td>
<td>&lt;2/4/7&gt;</td>
<td>Enables cartoon effects.
<u>Example Screenshots:</u> 2 = <a href=":File:Dustfall.jpg" class="wikilink" title="Dust effect when falling">Dust effect when falling</a>, 4 = <a href=":File:Dasheffect.jpg" class="wikilink" title="Dash effect">Dash effect</a>, 7 = <a href=":File:Dustfall.jpg" class="wikilink" title="Dust effect when falling">Dust effect when falling</a>, <a href=":File:Dasheffect.jpg" class="wikilink" title="Dash effect">Dash effect</a>, <a href=":File:Dustwall.jpg" class="wikilink" title="Wall-jump effect">Wall-jump effect</a>.</td>
</tr>
<tr>
<td>cg_cartoonHitEffect</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, critical hit effects are displayed for high damage value attacks.
<u>Example Screenshot:</u> <a href=":File:Cg_cartoonHitEffect1.jpg" class="wikilink" title="cg_cartoonHitEffect &quot;1&quot;">cg_cartoonHitEffect "1"</a></td>
</tr>
<tr>
<td>cg_chatBeep</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables the chat beep sound when someone sends a message.</td>
</tr>
<tr>
<td>cg_chatFilter</td>
<td>*</td>
<td>0</td>
<td>&lt;0-2&gt;</td>
<td>Filters chat messages.
0 = Display all Messages, 1 = Filters global chat messages, 2 = Filters team chat messages</td>
</tr>
<tr>
<td>cg_chatFilterTV</td>
<td>*</td>
<td>2</td>
<td>&lt;0-4&gt;</td>
<td>Filters Warfork TV chat messages.
0 = Display all Messages, 1 = Filters global chat messages, 2 = Filters team chat messages, 4 = Filter TV spectator chat messages</td>
</tr>
<tr>
<td>cg_clientHUD</td>
<td>*</td>
<td></td>
<td>&lt;HUD name&gt;</td>
<td>Changes your <a href="HUD" class="wikilink" title="HUD">HUD</a>.</td>
</tr>
<tr>
<td>cg_colorCorrection</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables color correction.
Color Correction works only on maps which have tables for it with supported GPUs.
<u>Example Screenshots:</u> <a href=":File:Cg_colorCorrection0.jpg" class="wikilink" title="cg_colorCorrection &quot;0&quot;">cg_colorCorrection "0"</a> · <a href=":File:Cg_colorCorrection1.jpg" class="wikilink" title="cg_colorCorrection &quot;1&quot;">cg_colorCorrection "1"</a></td>
</tr>
<tr>
<td>cg_crosshair</td>
<td>*</td>
<td>1</td>
<td>&lt;0-13&gt;</td>
<td>Changes your crosshair style.
0 = No crosshair
![[Crosshairs_examples.png]]</td>
</tr>
<tr>
<td>cg_crosshair_color</td>
<td>*</td>
<td>255 255 255</td>
<td>&lt;R G B&gt;</td>
<td>Changes the color of your crosshair.</td>
</tr>
<tr>
<td>cg_crosshair_damage_color</td>
<td>*</td>
<td>255 0 0</td>
<td>&lt;R G B&gt;</td>
<td>Changes the color of your crosshair when you hit an enemy.</td>
</tr>
<tr>
<td>cg_crosshair_font</td>
<td>*</td>
<td>Warsow Crosshairs</td>
<td><font name></td>
<td>Changes the font of your crosshair.</td>
</tr>
<tr>
<td>cg_crosshair_size</td>
<td>*</td>
<td>24</td>
<td>&lt;size&gt;</td>
<td>Changes the size of your crosshair.</td>
</tr>
<tr>
<td>cg_crosshair_strong</td>
<td>*</td>
<td>0</td>
<td>&lt;0-13&gt;</td>
<td>Changes your crosshair style for strong ammo. 0 disables it.</td>
</tr>
<tr>
<td>cg_crosshair_strong_color</td>
<td>*</td>
<td>255 255 255</td>
<td>&lt;R G B&gt;</td>
<td>Changes the color of your crosshair for strong ammo.</td>
</tr>
<tr>
<td>cg_crosshair_strong_size</td>
<td>*</td>
<td>24</td>
<td>&lt;size&gt;</td>
<td>Changes the size of your crosshair for strong ammo.</td>
</tr>
<tr>
<td>cg_damage_blend</td>
<td></td>
<td>1</td>
<td>&lt;0-1&gt;</td>
<td>This command no longer works and is a placeholder.
It use to enable a red flash when you got hit if cg_damage_indicator = 1.</td>
</tr>
<tr>
<td>cg_damage_indicator</td>
<td>*</td>
<td>1</td>
<td>&lt;0-1&gt;</td>
<td>If enabled, a red damage indicator will appear in the direction(s) you were hit.</td>
</tr>
<tr>
<td>cg_damage_indicator_time</td>
<td>*</td>
<td>25</td>
<td>&lt;value&gt;</td>
<td>Sets how long the red damage indicator will be visible.</td>
</tr>
<tr>
<td>cg_damageNumbers</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables Damage Numbers that are displayed when attacking a player.</td>
</tr>
<tr>
<td>cg_damageNumbersColor</td>
<td>*</td>
<td>8</td>
<td>&lt;0-11&gt;</td>
<td>Changes the color of your Damage Numbers.
0 = White, 1 = Black, 2 = Red, 3 = Green, 4 = Blue, 5 = Yellow, 6 = Orange, 7 = Magenta, 8 = Cyan, 9 = Light Grey, 10 = Medium Grey, 11 = Dark Grey</td>
</tr>
<tr>
<td>cg_damageNumbersDistance</td>
<td>*</td>
<td>48</td>
<td>&lt;1-200&gt;</td>
<td>The vertical distance above the player model that Damage Numbers are displayed.</td>
</tr>
<tr>
<td>cg_damageNumbersOffset</td>
<td>*</td>
<td>1</td>
<td>&lt;1-5&gt;</td>
<td>The offset distance between the Damage Number and its shadow.</td>
</tr>
<tr>
<td>cg_damageNumbersSize</td>
<td>*</td>
<td>1</td>
<td>&lt;1-4&gt;</td>
<td>Changes the size of your Damage Numbers.
1 = Tiny, 2 = Small, 3 = Medium, 4 = Large</td>
</tr>
<tr>
<td>cg_debugHUD</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the HUD name that's being loaded will print to console.</td>
</tr>
<tr>
<td>cg_debugPlayerModels</td>
<td>*, C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, player model information will be displayed on each map load in console.</td>
</tr>
<tr>
<td>cg_debugWeaponModels</td>
<td>*, C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, weapon model information will be displayed on each map load in console.</td>
</tr>
<tr>
<td>cg_decals</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will see projectile impact effects on walls.</td>
</tr>
<tr>
<td>cg_draw2D</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will see the HUD (scores, ammunition, clock, etc.)</td>
</tr>
<tr>
<td>cg_ebbeam_alpha</td>
<td>*</td>
<td>0.4</td>
<td>&lt;0-1&gt;</td>
<td>Sets the transparency of the Electrobolt Beam. 0 = 100% Transparent &amp; 1 = 100% Solid</td>
</tr>
<tr>
<td>cg_ebbeam_old</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will see the old (simplistic) Electrobolt beam.</td>
</tr>
<tr>
<td>cg_ebbeam_time</td>
<td>*</td>
<td>0.6</td>
<td>&lt;value&gt;</td>
<td>Sets how long the Elecrobolt beam will be visible.</td>
</tr>
<tr>
<td>cg_ebbeam_width</td>
<td>*</td>
<td>64</td>
<td>&lt;value&gt;</td>
<td>Sets the width of the Elecrobolt beam.</td>
</tr>
<tr>
<td>cg_explosionsDust</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, an explosion dust will appear around Grenade Launcher and Rocket Launcher projectiles upon impact.</td>
</tr>
<tr>
<td>cg_explosionsRing</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, an explosion ring will appear around Grenade Launcher and Rocket Launcher projectiles upon impact.</td>
</tr>
<tr>
<td>cg_flashWindowCount</td>
<td>*</td>
<td>4</td>
<td>&lt;value&gt;</td>
<td>The amount of times Warfork flashes in your taskbar if warmup ends and a match starts.</td>
</tr>
<tr>
<td>cg_forceMyTeamAlpha</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, your HUD, teammates and enemies will appear as if you always were in the Alpha team.</td>
</tr>
<tr>
<td>cg_gamepad_accelMax</td>
<td>*</td>
<td>2</td>
<td>&lt;value&gt;</td>
<td>Maximum acceleration of the gamepad.</td>
</tr>
<tr>
<td>cg_gamepad_accelSpeed</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Speed of gamepad's acceleration.</td>
</tr>
<tr>
<td>cg_gamepad_accelThres</td>
<td>*</td>
<td>0.9</td>
<td>&lt;value&gt;</td>
<td>Threshold of gamepad's acceleration.</td>
</tr>
<tr>
<td>cg_gamepad_moveThres</td>
<td>*</td>
<td>0.239</td>
<td>&lt;value&gt;</td>
<td>Specifies the dead-zone for movement.</td>
</tr>
<tr>
<td>cg_gamepad_pitchInvert</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the gamepad will be inverted.</td>
</tr>
<tr>
<td>cg_gamepad_pitchSpeed</td>
<td>*</td>
<td>240</td>
<td>&lt;value&gt;</td>
<td>Specifies the sensitivity when looking up and down.</td>
</tr>
<tr>
<td>cg_gamepad_pitchThres</td>
<td>*</td>
<td>0.265</td>
<td>&lt;value&gt;</td>
<td>Specifies the dead-zone for looking up and down.</td>
</tr>
<tr>
<td>cg_gamepad_runThres</td>
<td>*</td>
<td>0.75</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_gamepad_strafeRunThres</td>
<td>*</td>
<td>0.45</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_gamepad_strafeThres</td>
<td>*</td>
<td>0.239</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_gamepad_swapSticks</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Swaps sticks on your gamepad.</td>
</tr>
<tr>
<td>cg_gamepad_yawSpeed</td>
<td>*</td>
<td>260</td>
<td>&lt;value&gt;</td>
<td>Specifies the sensitivity when looking left and right.</td>
</tr>
<tr>
<td>cg_gamepad_yawThres</td>
<td>*</td>
<td>0.265</td>
<td>&lt;value&gt;</td>
<td>Specifies the dead-zone for looking left and right.</td>
</tr>
<tr>
<td>cg_gibs</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>This command is a placeholder.
It use to define the total number of gibs that would be displayed when you fragged someone.</td>
</tr>
<tr>
<td>cg_gun</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Shows your weapon.</td>
</tr>
<tr>
<td>cg_gun_alpha</td>
<td>*</td>
<td>1</td>
<td>&lt;0-1&gt;</td>
<td>Transparency of your weapon model.</td>
</tr>
<tr>
<td>cg_gun_fov</td>
<td>*</td>
<td>90</td>
<td>&lt;1-160&gt;</td>
<td>Field-of-View of your weapon model.</td>
</tr>
<tr>
<td>cg_gunbob</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables bobbing of the weapon model.</td>
</tr>
<tr>
<td>cg_gunx</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Moves your weapon's model on the X axis.</td>
</tr>
<tr>
<td>cg_guny</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Moves your weapon's model on the Y axis.</td>
</tr>
<tr>
<td>cg_gunz</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Moves your weapon's model on the Z axis.</td>
</tr>
<tr>
<td>cg_handOffset</td>
<td>*</td>
<td>5</td>
<td>&lt;value&gt;</td>
<td>The offset of your hand's position. 0 means middle.</td>
</tr>
<tr>
<td>cg_instabeam_alpha</td>
<td>*</td>
<td>0.4</td>
<td>&lt;0-1&gt;</td>
<td>Transparency of the instabeam.</td>
</tr>
<tr>
<td>cg_instabeam_time</td>
<td>*</td>
<td>0.4</td>
<td>&lt;value&gt;</td>
<td>The time an instagun beam will be displayed before disappearing.</td>
</tr>
<tr>
<td>cg_instabeam_width</td>
<td>*</td>
<td>7</td>
<td>&lt;value&gt;</td>
<td>The width of an instagun beam.</td>
</tr>
<tr>
<td>cg_laserBeamSubdivisions</td>
<td>*</td>
<td>10</td>
<td>&lt;value&gt;</td>
<td>The higher the number the smoother the laser beam looks.</td>
</tr>
<tr>
<td>cg_movementStyle</td>
<td>*, U</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Old movement = 0 and New movement = 1</td>
</tr>
<tr>
<td>cg_noAutoHop</td>
<td>*, U</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, disables autohop by holding spacebar.</td>
</tr>
<tr>
<td>cg_outlineModels</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Outlines models.</td>
</tr>
<tr>
<td>cg_outlinePlayers</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Outlines players.</td>
</tr>
<tr>
<td>cg_outlineWorld</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Outlines every object in maps.</td>
</tr>
<tr>
<td>cg_particles</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables particles.</td>
</tr>
<tr>
<td>cg_pickup_flash</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will see a flash when picking up an item or weapon.
For this command to work please set cg_showViewBlends 1</td>
</tr>
<tr>
<td>cg_placebo</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>An easteregg for comedic purpose that does nothing. It will be removed shortly.</td>
</tr>
<tr>
<td>cg_playerTrailsColor</td>
<td></td>
<td>0.0 1.0 0.0</td>
<td>&lt;R G B&gt;</td>
<td>This command has already been removed from the game and only exists in default.cfg. The next update will purge the remnants.</td>
</tr>
<tr>
<td>cg_playList</td>
<td>*</td>
<td>sounds/music/match.m3u</td>
<td>&lt;path&gt;</td>
<td>Path to a music playlist.</td>
</tr>
<tr>
<td>cg_playListShuffle</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Plays songs randomly from the music playlist.</td>
</tr>
<tr>
<td>cg_predict</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Predicts players' movement on multiplayer servers for smoothness.</td>
</tr>
<tr>
<td>cg_predict_optimize</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Optimizes cg_predict's behavior.</td>
</tr>
<tr>
<td>cg_predictLaserBeam</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, a perfectly straight line laserbeam will always be drawn regardless of server lag. If disabled, a laserbeam will be drawn based on server lag.</td>
</tr>
<tr>
<td>cg_projectileAntilagOffset</td>
<td>*</td>
<td>1.0</td>
<td>&lt;value&gt;</td>
<td>The defined value adds a time offset to counter anti-lag visualization.</td>
</tr>
<tr>
<td>cg_projectileFireTrail</td>
<td>*</td>
<td>90</td>
<td>&lt;value&gt;</td>
<td>Controls the amount of firetrail left behind when firing the Rocket Launcher or Grenade Launcher.
0 = Disabled</td>
</tr>
<tr>
<td>cg_projectileFireTrailAlpha</td>
<td>*</td>
<td>0.45</td>
<td>&lt;0-1&gt;</td>
<td>Controls the transparency level of the firetrail left behind when firing the Rocket Launcher or Grenade Launcher.
0 = 100% Transparent, 1 = Solid Color</td>
</tr>
<tr>
<td>cg_projectileTrail</td>
<td>*</td>
<td>60</td>
<td>&lt;value&gt;</td>
<td>Controls the amount of smoke left behind when firing the Rocket Launcher or Grenade Launcher.
0 = Disabled</td>
</tr>
<tr>
<td>cg_raceGhosts</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables ghosts while racing.</td>
</tr>
<tr>
<td>cg_raceGhostsAlpha</td>
<td>*</td>
<td>0.25</td>
<td>&lt;0-1&gt;</td>
<td>Transparency of race ghosts.</td>
</tr>
<tr>
<td>cg_reactionKills</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables Reaction Kills.</td>
</tr>
<tr>
<td>cg_reactionKillsTimeout</td>
<td>*</td>
<td>45</td>
<td>&lt;1-180&gt;</td>
<td>Frequency of Reaction Kills in seconds.</td>
</tr>
<tr>
<td>cg_reactionRoundStart</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables Round Start Reactions.</td>
</tr>
<tr>
<td>cg_reactionRoundStartOdds</td>
<td>*</td>
<td>5</td>
<td>&lt;1-100&gt;</td>
<td>Odds of Round Start Reactions.</td>
</tr>
<tr>
<td>cg_scoreboardFontFamily</td>
<td>*</td>
<td>Droid Sans Mono</td>
<td><font name></td>
<td>Name of font used in scoreboard.</td>
</tr>
<tr>
<td>cg_scoreboardFontSize</td>
<td>*</td>
<td>12</td>
<td>&lt;value&gt;</td>
<td>Size of scoreboard's font.</td>
</tr>
<tr>
<td>cg_scoreboardMonoFontFamily</td>
<td>*</td>
<td>Droid Sand Mono</td>
<td><font></td>
<td></td>
</tr>
<tr>
<td>cg_scoreboardStats</td>
<td>*</td>
<td>1</td>
<td>&lt;0-1&gt;</td>
<td>If enabled, Weapons Statistics will be shown on the Scoreboard.</td>
</tr>
<tr>
<td>cg_scoreboardTitleFontFamily</td>
<td>*</td>
<td>Hemi Head</td>
<td><font name></td>
<td>Name of font used in the scoreboard's title.</td>
</tr>
<tr>
<td>cg_scoreboardTitleFontSize</td>
<td>*</td>
<td>24</td>
<td>&lt;value&gt;</td>
<td>Size of the font used in scoreboard's title.</td>
</tr>
<tr>
<td>cg_scoreboardWidthScale</td>
<td>*</td>
<td>1.0</td>
<td>&lt;value&gt;</td>
<td>Width scale of the scoreboard.</td>
</tr>
<tr>
<td>cg_shadows</td>
<td>*</td>
<td>1</td>
<td>&lt;0-2&gt;</td>
<td>Enables shadows. Uses simple shadows if set to 1, shadowmaps if set to 2. 0 to disable.</td>
</tr>
<tr>
<td>cg_showAwards</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Shows awards upon certain events (On Fire! etc.).</td>
</tr>
<tr>
<td>cg_showBloodTrail</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, damage rings will be rendered when a player is hit.</td>
</tr>
<tr>
<td>cg_showCaptureAreas</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>A command that does nothing. It will be removed shortly.</td>
</tr>
<tr>
<td>cg_showChasers</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Displays chasers on the scoreboard (if there are any).</td>
</tr>
<tr>
<td>cg_showCrosshairDamage</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Changes the crosshair's color to the damage color if an enemy gets hit.</td>
</tr>
<tr>
<td>cg_showFPS</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables an FPS counter.</td>
</tr>
<tr>
<td>cg_showhelp</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Displays help text under the timer.</td>
</tr>
<tr>
<td>cg_showHUD</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables HUD.</td>
</tr>
<tr>
<td>cg_showItemTimers</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Displays when items will spawn on your HUD (only in spectator mode).</td>
</tr>
<tr>
<td>cg_showMiniMap</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Displays a minimap (if supported by gamemode).</td>
</tr>
<tr>
<td>cg_showMiss</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>For debugging server events. If enabled, will dump prediction misses to console in x:y format. x = time y = distance error.
Best to use with con_drawnotify 1 for easier viewing.</td>
</tr>
<tr>
<td>cg_showObituaries</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Displays who fragged who using which weapon on your HUD.</td>
</tr>
<tr>
<td>cg_showPickup</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Displays when you pickup an item on your HUD.</td>
</tr>
<tr>
<td>cg_showPlayerNames</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Displays player names above player models.</td>
</tr>
<tr>
<td>cg_showPlayerNames_alpha</td>
<td>*</td>
<td>0.4</td>
<td>&lt;0-1&gt;</td>
<td>Transparency of player names.</td>
</tr>
<tr>
<td>cg_showPlayerNames_barWidth</td>
<td>*</td>
<td>8</td>
<td>&lt;value&gt;</td>
<td>Bar width above your teammates player model, which contains information such as Health and Armor.</td>
</tr>
<tr>
<td>cg_showPlayerNames_xoffset</td>
<td></td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Move player names by this much on the X axis.</td>
</tr>
<tr>
<td>cg_showPlayerNames_yoffset</td>
<td></td>
<td>16</td>
<td>&lt;value&gt;</td>
<td>Move player names by this much on the Y axis.</td>
</tr>
<tr>
<td>cg_showPlayerNames_zfar</td>
<td>*</td>
<td>824</td>
<td>&lt;value&gt;</td>
<td>Defines the distance that player names are still drawn over models.</td>
</tr>
<tr>
<td>cg_showPlayerTrails</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>This command has already been removed from the game and only exists in default.cfg. The next update will purge the remnants.</td>
</tr>
<tr>
<td>cg_showPointedPlayer</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, when your mouse is pointed over a teammate or enemy their name will be drawn over the player model.</td>
</tr>
<tr>
<td>cg_showPressedKeys</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, will show the key presses of players.</td>
</tr>
<tr>
<td>cg_showSelfShadow</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables seeing your own shadow.</td>
</tr>
<tr>
<td>cg_showSpeed</td>
<td>*</td>
<td>1</td>
<td>&lt;0-3&gt;</td>
<td>Changes the position of the speed display of the player. 0 to disable. Values higher than 1 aren't supported on all HUDs.
<u>Example Screenshot:</u> <a href=":File:Cg_showSpeed1.jpg" class="wikilink" title="cg_showSpeed &quot;1&quot;">cg_showSpeed "1"</a></td>
</tr>
<tr>
<td>cg_showTeamLocations</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled and your HUD supports it, your teammates location will be shown.</td>
</tr>
<tr>
<td>cg_showTeamMates</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Show teammates indicators.</td>
</tr>
<tr>
<td>cg_showTimer</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Displays the match's timer.</td>
</tr>
<tr>
<td>cg_showViewBlends</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, fullscreen overlays for underwater and pain effects will be displayed.
<u>Example Screenshots:</u> <a href=":File:Cg_showViewBlends0.jpg" class="wikilink" title="cg_showViewBlends &quot;0&quot;">cg_showViewBlends "0"</a> · <a href=":File:Cg_showViewBlends1.jpg" class="wikilink" title="cg_showViewBlends &quot;1&quot;">cg_showViewBlends "1"</a></td>
</tr>
<tr>
<td>cg_showZoomEffect</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the zoom effect is shown.</td>
</tr>
<tr>
<td>cg_simpleItems</td>
<td>*</td>
<td>0</td>
<td>&lt;0-2&gt;</td>
<td>Replaces 3D models of pickupable items with simplistic 2D models.
0 = 3D item models, 1 = Animated 2D items (bobbing up and down), 2 = Static 2D items</td>
</tr>
<tr>
<td>cg_simpleItemsSize</td>
<td>*</td>
<td>16</td>
<td>&lt;value&gt;</td>
<td>Changes the size of simplistic item models.</td>
</tr>
<tr>
<td>cg_specHUD</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;HUD name&gt;</td>
<td>Changes the HUD while spectating.</td>
</tr>
<tr>
<td>cg_strafeHUD</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables strafe HUD.</td>
</tr>
<tr>
<td>cg_teamALPHAcolor</td>
<td>*</td>
<td>254 101 101</td>
<td>&lt;R G B&gt;</td>
<td>Color of team Alpha players.</td>
</tr>
<tr>
<td>cg_teamALPHAmodel</td>
<td>*</td>
<td>bigvic</td>
<td>&lt;model name&gt;</td>
<td>Default model of team Alpha players.</td>
</tr>
<tr>
<td>cg_teamALPHAmodelForce</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Changes models of all team Alpha players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamALPHAskin</td>
<td>*</td>
<td>default</td>
<td>&lt;default/fullbright&gt;</td>
<td>Changes models skin of all Team Forbidden players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamBETAcolor</td>
<td>*</td>
<td>153 204 255</td>
<td>&lt;R G B&gt;</td>
<td>Color of team Beta players.</td>
</tr>
<tr>
<td>cg_teamBETAmodel</td>
<td>*</td>
<td>padpork</td>
<td>&lt;model name&gt;</td>
<td>Default model of team Beta players.</td>
</tr>
<tr>
<td>cg_teamBETAmodelForce</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Changes models of all team Beta players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamBETAskin</td>
<td>*</td>
<td>default</td>
<td>&lt;default/fullbright&gt;</td>
<td>Changes models skin of all Team Icy players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamColoredBeams</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the LG beam color will be changed to the team color of the attacker.
<u>Example Screenshots:</u> <a href=":File:Cg_teamColoredBeams0.jpg" class="wikilink" title="cg_teamColoredBeams &quot;0&quot;">cg_teamColoredBeams "0"</a> · <a href=":File:Cg_teamColoredBeams1.jpg" class="wikilink" title="cg_teamColoredBeams &quot;1&quot;">cg_teamColoredBeams "1"</a></td>
</tr>
<tr>
<td>cg_teamColoredInstaBeams</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Changes the color of the InstaBeam to the team color of the attacker.
<u>Example Screenshots:</u> <a href=":File:Cg_teamColoredInstaBeams0.jpg" class="wikilink" title="cg_teamColoredInstaBeams &quot;0&quot;">cg_teamColoredInstaBeams "0"</a> · <a href=":File:Cg_teamColoredInstaBeams1.jpg" class="wikilink" title="cg_teamColoredInstaBeams &quot;1&quot;">cg_teamColoredInstaBeams "1"</a></td>
</tr>
<tr>
<td>cg_teamPLAYERScolor</td>
<td>*</td>
<td>0 255 70</td>
<td>&lt;R G B&gt;</td>
<td>Color of team Players players (non-team based gametypes).</td>
</tr>
<tr>
<td>cg_teamPLAYERScolorForce</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Changes color of all team Players players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamPLAYERSmodel</td>
<td>*</td>
<td>bigvic</td>
<td>&lt;model name&gt;</td>
<td>Default model of team Players players.</td>
</tr>
<tr>
<td>cg_teamPLAYERSmodelForce</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Changes models of all team Players players to a user-chosen one.</td>
</tr>
<tr>
<td>cg_teamPLAYERSskin</td>
<td>*</td>
<td>default</td>
<td>&lt;default/fullbright&gt;</td>
<td>Changes models skin of all team Players players to a user-chosen one.
<u>Example Screenshots:</u> <a href=":File:Cg_teamPLAYERSskin_default.jpg" class="wikilink" title="cg_teamPLAYERSskin &quot;default&quot;">cg_teamPLAYERSskin "default"</a> · <a href=":File:Cg_teamPLAYERSskin_fullbright.jpg" class="wikilink" title="cg_teamPLAYERSskin &quot;fullbright&quot;">cg_teamPLAYERSskin "fullbright"</a></td>
</tr>
<tr>
<td>cg_thirdPerson</td>
<td>C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables third person view.
<u>Example Screenshots:</u> <a href=":File:Cg_thirdPerson_0.jpg" class="wikilink" title="cg_thirdPerson &quot;0&quot;">cg_thirdPerson "0"</a> · <a href=":File:Cg_thirdPerson_1.jpg" class="wikilink" title="cg_thirdPerson &quot;1&quot;">cg_thirdPerson "1"</a></td>
</tr>
<tr>
<td>cg_thirdPersonAngle</td>
<td></td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Changes the angle of third person view.
<u>Example Screenshots:</u> <a href=":File:Cg_thirdPersonAngle0.jpg" class="wikilink" title="cg_thirdPersonAngle &quot;0&quot;">cg_thirdPersonAngle "0"</a> · <a href=":File:Cg_thirdPersonAngle180.jpg" class="wikilink" title="cg_thirdPersonAngle &quot;180&quot;">cg_thirdPersonAngle "180"</a></td>
</tr>
<tr>
<td>cg_thirdPersonRange</td>
<td></td>
<td>70</td>
<td>&lt;value&gt;</td>
<td>The distance that the player model appears from the camera when in third person view.
<u>Example Screenshots:</u> <a href=":File:Cg_thirdpersonrange70.jpg" class="wikilink" title="cg_thirdPersonRange &quot;70&quot;">cg_thirdPersonRange "70"</a> · <a href=":File:Cg_thirdpersonrange200.jpg" class="wikilink" title="cg_thirdPersonRange &quot;200&quot;">cg_thirdPersonRange "200"</a></td>
</tr>
<tr>
<td>cg_touch_flip</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_lookDecel</td>
<td>*</td>
<td>8.5</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_lookInvert</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_lookSens</td>
<td>*</td>
<td>9</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_lookThres</td>
<td>*</td>
<td>5</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_moveThres</td>
<td>*</td>
<td>24</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_scale</td>
<td>*</td>
<td>100</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_showMoveDir</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_strafeThres</td>
<td>*</td>
<td>32</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_zoomThres</td>
<td>*</td>
<td>24</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_touch_zoomTime</td>
<td>*</td>
<td>250</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cg_viewBob</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enabled head bobbing.</td>
</tr>
<tr>
<td>cg_viewSize</td>
<td>*</td>
<td>100</td>
<td>&lt;40-100&gt;</td>
<td>The percentage of the viewable area displayed on your screen.
If less than 100 is defined then black space will fill your screen.
If you set cl_demoavi_scissor 0 then images will always be exported as cg_viewSize 100.
If you set cl_demoavi_scissor 1 then images will always be exported as cg_viewSize 100.
<u>Example Screenshot:</u> <a href=":File:Cg_viewSize40.jpg" class="wikilink" title="cg_viewsize &quot;40&quot;">cg_viewsize "40"</a></td>
</tr>
<tr>
<td>cg_voiceChats</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables voice commands (also known as "VSAYS").</td>
</tr>
<tr>
<td>cg_volume_announcer</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0-2.0&gt;</td>
<td>Changes the volume of the announcer.</td>
</tr>
<tr>
<td>cg_volume_effects</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0-2.0&gt;</td>
<td>Changes the volume of the effects.</td>
</tr>
<tr>
<td>cg_volume_hitsound</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0-2.0&gt;</td>
<td>Changes the volume of the hitsound.</td>
</tr>
<tr>
<td>cg_volume_players</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0-2.0&gt;</td>
<td>Changes the volume of player sounds.</td>
</tr>
<tr>
<td>cg_volume_voicechats</td>
<td>*</td>
<td>1.0</td>
<td>&lt;0.0-2.0&gt;</td>
<td>Changes the volume of voice commands.</td>
</tr>
<tr>
<td>cg_weaponAutoswitch</td>
<td>*</td>
<td>2</td>
<td>&lt;0-2&gt;</td>
<td>Enables auto switching of weapons when you're out of ammo.
0 = Autoswitch Disabled, 1 = Autoswitch Enabled (one click), 2 = Autoswitch Enabled (two clicks)</td>
</tr>
<tr>
<td>cg_weaponFlashes</td>
<td>*</td>
<td>2</td>
<td>&lt;0-2&gt;</td>
<td>Enables weapon flashes.
0 = All Weapon Flashes Disabled, 1 = Wall + Floor Weapons Flash Enabled, 2 = Wall + Floor &amp; Weapon Muzzle Flashes Enabled (if cg_gun is set to 1).</td>
</tr>
<tr>
<td>cg_weaponlist</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the weapon list will be displayed on your HUD.</td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### cl\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>cl_anglespeedkey</td>
<td></td>
<td>1.5</td>
<td>&lt;value&gt;</td>
<td>Defines the multiplier for how fast you turn when running is toggled.</td>
</tr>
<tr>
<td>cl_checkForUpdate</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the client will be permitted to check for updates.</td>
</tr>
<tr>
<td>cl_compresspackets</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Compresses network packets.</td>
</tr>
<tr>
<td>cl_debug_serverCmd</td>
<td>*, C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, server debug information will printed to console.</td>
</tr>
<tr>
<td>cl_debug_timeDelta</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, server debug information (netcode) will printed to console.</td>
</tr>
<tr>
<td>cl_demoavi_audio</td>
<td>*</td>
<td>0</td>
<td></td>
<td>If set to 1 Warfork will create a .wav when using demoavi cl_demoavi_video should be set to 0 since it will lag the game when capturing resulting in audio that is not realtime.</td>
</tr>
<tr>
<td>cl_demoavi_fps</td>
<td>*</td>
<td>30.3</td>
<td></td>
<td>Determines how many frames per second get captured by demoavi</td>
</tr>
<tr>
<td>cl_demoavi_scissor</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cl_demoavi_video</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If set to 1 Warfork will output frames when using demoavi</td>
</tr>
<tr>
<td>cl_download_allow_modules</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Allows the downlaoding of modules.
This is needed for mods such as Racemod.</td>
</tr>
<tr>
<td>cl_download_name</td>
<td>-</td>
<td>&lt;value&gt;</td>
<td>*write protected*</td>
<td>The name of what's being downloaded.</td>
</tr>
<tr>
<td>cl_download_percent</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>The percentage of what's being downloaded.</td>
</tr>
<tr>
<td>cl_downloads</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, your client is allowed to download files (maps, textures, etc.) directly from the server you're connecting to.</td>
</tr>
<tr>
<td>cl_downloads_from_web</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td>If enabled, your client is allowed to download files (maps, textures, etc.) from a webserver.</td>
</tr>
<tr>
<td>cl_downloads_from_web_timeout</td>
<td>*</td>
<td>600</td>
<td>&lt;value&gt;</td>
<td>The time before a client timeout when attempting to download from a webserver.</td>
</tr>
<tr>
<td>cl_extrapolate</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cl_flip</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cl_maxfps</td>
<td>*</td>
<td>250</td>
<td>&lt;24-1000&gt;</td>
<td>Sets the FPS limit.</td>
</tr>
<tr>
<td>cl_mm_autologin</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, matchmaking will automatically be logged into.</td>
</tr>
<tr>
<td>cl_mm_session</td>
<td>U, -</td>
<td>0</td>
<td>*write protected*</td>
<td>Contains your matchmaking session information.</td>
</tr>
<tr>
<td>cl_mm_user</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>Contains your matchmaking username.</td>
</tr>
<tr>
<td>cl_mumble</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables positional audio support for Mumble</td>
</tr>
<tr>
<td>cl_mumble_scale</td>
<td>*</td>
<td>0.0254</td>
<td>&lt;value&gt;</td>
<td>Scales the positional audio distance for Mumble.</td>
</tr>
<tr>
<td>cl_pitchspeed</td>
<td></td>
<td>150</td>
<td>&lt;value&gt;</td>
<td>The speed the player's screen moves up and down when using keyboard keys.</td>
</tr>
<tr>
<td>cl_port</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>IPv4 client port</td>
</tr>
<tr>
<td>cl_port6</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>IPv6 client port</td>
</tr>
<tr>
<td>cl_pps</td>
<td>*</td>
<td>40</td>
<td>&lt;value&gt;</td>
<td>The amount packets per second that client is sending to the server.</td>
</tr>
<tr>
<td>cl_run</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, running will be toggle automatically.
This serves no purpose in disabling as Warfork has no footstep sounds.</td>
</tr>
<tr>
<td>cl_shownet</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, latency information for network packets will be printed in console.</td>
</tr>
<tr>
<td>cl_sleep</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will get lower CPU usage with the cost of higher mouse latency and less stable fps.</td>
</tr>
<tr>
<td>cl_stereo</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, stereoscopic rendering mode will be toggled.</td>
</tr>
<tr>
<td>cl_stereo_separation</td>
<td>*</td>
<td>0.4</td>
<td>&lt;0-1.0&gt;</td>
<td>Camera offset with cl_stereo</td>
</tr>
<tr>
<td>cl_timeout</td>
<td></td>
<td>120</td>
<td>&lt;value&gt;</td>
<td>Kicks the player if connection is lost for more than x seconds.</td>
</tr>
<tr>
<td>cl_ucmdMaxResend</td>
<td>*</td>
<td>3</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cl_yawspeed</td>
<td></td>
<td>140</td>
<td></td>
<td></td>
</tr>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### cm\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>cm_mapHeader</td>
<td></td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>Stores map header information in the cvar.</td>
</tr>
<tr>
<td>cm_mapVersion</td>
<td></td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>Stores map format description (IBSP, FBSP, etc.) in the cvar.</td>
</tr>
<tr>
<td>cm_noAreas</td>
<td>C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Disables area culling.</td>
</tr>
<tr>
<td>cm_noCurves</td>
<td>C</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you can clip through curved surfaces.
<u>Example Screenshots:</u> <a href=":File:Cm_noCurves_1_1.jpg" class="wikilink" title="cm_noCurves &quot;1&quot; Perspective 1">cm_noCurves "1" Perspective 1</a> · <a href=":File:Cm_noCurves_1_2.jpg" class="wikilink" title="cm_noCurves &quot;1&quot; Perspective 2">cm_noCurves "1" Perspective 2</a></td>
</tr>
</tbody>
</table>

### com\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>com_introPlayed3</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>com_showtrace</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the number of traces that has to be made will be displayed in console.
You must change the map with devmap &lt;mapname&gt; and then com_showtrace 1 to utilize this command.</td>
</tr>
</tbody>
</table>

### con\_

| Command | Flags | Default | Parameters | Description |
|----|----|----|----|----|
| con_chatmode | \* | 3 |  |  |
| con_drawNotify | \* | 0 |  |  |
| con_fontSystemBigSize | \* | 24 | \<value\> |  |
| con_fontSystemConsoleSize | \* | 14 | \<value\> |  |
| con_fontSystemFallbackFamily | \*, L | Droid Sans Fallback | <font name> |  |
| con_fontSystemFamily | \* | Droid Sans | <font name> |  |
| con_fontSystemMediumSize | \* | 16 | \<value\> |  |
| con_fontSystemMonoFamily | \* | Droid Sans Mono | <font name> |  |
| con_fontSystemSmallSize | \* | 14 | \<value\> |  |
| con_fontSystemTinySize | \* | 8 | \<value\> |  |
| con_messageMode |  | 0 |  |  |
| con_notifytime | \* | 3 |  |  |
| con_printText | \* | 1 |  |  |

### fs\_

| Command            | Flags | Default | Parameters          | Description |
|--------------------|-------|---------|---------------------|-------------|
| fs_basegame        | \-    | basewf  | \*write protected\* |             |
| fs_basepath        | \-    | .       | \*write protected\* |             |
| fs_cdpath          | \-    |         | \*write protected\* |             |
| fs_game            | S, L  | basewf  |                     |             |
| fs_usedownloadsdir | \-    | 1       | \*write protected\* |             |
| fs_usehomedir      | \-    | 1       | \*write protected\* |             |

### g\_

| Command | Flags | Default | Parameters | Description |
|----|----|----|----|----|
| g_allow_bunny | \*, - | 1 | \*write protected\* |  |
| g_allow_falldamage | \* | 1 | \<0/1\> | Enables fall damage. |
| g_allow_selfdamage | \* | 1 | \<0/1\> | If enabled, players can hurt themselves with own weapons. |
| g_allow_spectator_voting | \* | 1 | \<0/1\> | Allows spectators to vote. Affects callvotes. |
| g_allow_stun | \* | 1 | \<0/1\> | If enabled, players can get stunned. |
| g_allow_teamdamage | \* | 1 | \<0/1\> | Enables friendlyfire. |
| g_ammo_respawn | \* | 0 | \<value\> | Changes the ammo respawn time. |
| g_antilag | \*, S, L | 1 | \<0/1\> | Enables antilag. |
| g_antilag_maxtimedelta | \* | 200 | \<value\> |  |
| g_antilag_timenudge | \* | 0 |  |  |
| g_asGC_interval | \* | 10 |  |  |
| g_asGC_stats | \* | 0 |  |  |
| g_autorecord | \* | 0 | \<0/1\> | Automatically records all demos. |
| g_autorecord_maxdemos | \* | 0 | \<value\> | Maximum amount of automatically recorded demos to keep (deletes old ones once limit is exceeded). |
| g_bomb_armtime | \* | 4 | \<value\> | (Bomb-exclusive) Changes the amount of time needed to arm a bomb.. |
| g_bomb_bombtimer | \* | 25 | \<value\> | (Bomb-exclusive) Time before the bomb explodes after arming. |
| g_bomb_carriers | \* | 1 | \<value\> | (Bomb-exclusive) |
| g_bomb_defusetime | \* | 7 | \<value\> | (Bomb-exclusive) Changes the amount of time needed to defuse an armed bomb. |
| g_bomb_roundtime | \* | 60 | \<value\> | (Bomb-exclusive) Sets the round time (in seconds). |
| g_bomb_spawnprotection | \* | 3 | \<value\> | (Bomb-exclusive) |
| g_challengers_queue |  | 1 | \<0/1\> | Enables the challengers queue. |
| g_countdown_time | \* | 5 | \<value\> |  |
| g_disable_opcall_allow_falldamage | \* | 0 | \<0/1\> | Disables "allow_falldamage" opcall. |
| g_disable_opcall_allow_selfdamage | \* | 0 | \<0/1\> | Disables "allow_selfdamage" opcall. |
| g_disable_opcall_allow_teamdamage | \* | 0 | \<0/1\> | Disables "allow_teamdamage" opcall. |
| g_disable_opcall_allow_uneven | \* | 0 | \<0/1\> | Disables "allow_uneven" opcall. |
| g_disable_opcall_allready | \* | 0 | \<0/1\> | Disables "allready" opcall. |
| g_disable_opcall_extended_time | \* | 0 | \<0/1\> | Disables "extended_time" opcall. |
| g_disable_opcall_gametype | \* | 0 | \<0/1\> | Disables "gametype" opcall. |
| g_disable_opcall_instajump | \* | 0 | \<0/1\> | Disables "instajump" opcall. |
| g_disable_opcall_instashield | \* | 0 | \<0/1\> | Disables "instashield" opcall. |
| g_disable_opcall_kick | \* | 0 | \<0/1\> | Disables "kick" opcall. |
| g_disable_opcall_kickban | \* | 0 | \<0/1\> | Disables "kickban" opcall. |
| g_disable_opcall_lock | \* | 0 | \<0/1\> | Disables "lock" opcall. |
| g_disable_opcall_map | \* | 0 | \<0/1\> | Disables "map" opcall. |
| g_disable_opcall_maxteamplayers | \* | 0 | \<0/1\> | Disables "maxteamplayers" opcall. |
| g_disable_opcall_mute | \* | 0 | \<0/1\> | Disables "mute" opcall. |
| g_disable_opcall_nextmap | \* | 0 | \<0/1\> | Disables "nextmap" opcall. |
| g_disable_opcall_numbots | \* | 0 | \<0/1\> | Disables "numbots" opcall. |
| g_disable_opcall_rebalance | \* | 0 | \<0/1\> | Disables "rebalance" opcall. |
| g_disable_opcall_remove | \* | 0 | \<0/1\> | Disables "remove" opcall. |
| g_disable_opcall_restart | \* | 0 | \<0/1\> | Disables "restart" opcall. |
| g_disable_opcall_scorelimit | \* | 0 | \<0/1\> | Disables "scorelimit" opcall. |
| g_disable_opcall_shuffle | \* | 0 | \<0/1\> | Disables "shuffle" opcall. |
| g_disable_opcall_timein | \* | 0 | \<0/1\> | Disables "timein" opcall. |
| g_disable_opcall_timelimit | \* | 0 | \<0/1\> | Disables "timelimit" opcall. |
| g_disable_opcall_timeout | \* | 0 | \<0/1\> | Disables "timeout" opcall. |
| g_disable_opcall_unlock | \* | 0 | \<0/1\> | Disables "unlock" opcall. |
| g_disable_opcall_unmute | \* | 0 | \<0/1\> | Disables "unmute" opcall. |
| g_disable_opcall_vmute | \* | 0 | \<0/1\> | Disables "vmute" opcall. |
| g_disable_opcall_vunmute | \* | 0 | \<0/1\> | Disables "vunmute" opcall. |
| g_disable_opcall_warmup_timelimit | \* | 0 | \<0/1\> | Disables "warmup_timelimit" opcall. |
| g_disable_vote_allow_falldamage | \* | 0 | \<0/1\> | Disables "allow_falldamage" callvote. Doesn't affect opcalls. |
| g_disable_vote_allow_selfdamage | \* | 0 | \<0/1\> | Disables "allow_selfdamage" callvote. Doesn't affect opcalls. |
| g_disable_vote_allow_teamdamage | \* | 0 | \<0/1\> | Disables "allow_teamdamage" callvote. Doesn't affect opcalls. |
| g_disable_vote_allow_uneven | \* | 0 | \<0/1\> | Disables "allow_uneven" callvote. Doesn't affect opcalls. |
| g_disable_vote_allready | \* | 0 | \<0/1\> | Disables "allready" callvote. Doesn't affect opcalls. |
| g_disable_vote_extended_time | \* | 0 | \<0/1\> | Disables "extended_time" callvote. Doesn't affect opcalls. |
| g_disable_vote_gametype | \* | 0 | \<0/1\> | Disables "gametype" callvote. Doesn't affect opcalls. |
| g_disable_vote_instajump | \* | 0 | \<0/1\> | Disables "instajump" callvote. Doesn't affect opcalls. |
| g_disable_vote_instashield | \* | 0 | \<0/1\> | Disables "instashield" callvote. Doesn't affect opcalls. |
| g_disable_vote_kick | \* | 0 | \<0/1\> | Disables "kick" callvote. Doesn't affect opcalls. |
| g_disable_vote_kickban | \* | 0 | \<0/1\> | Disables "kickban" callvote. Doesn't affect opcalls. |
| g_disable_vote_lock | \* | 0 | \<0/1\> | Disables "lock" callvote. Doesn't affect opcalls. |
| g_disable_vote_map | \* | 0 | \<0/1\> | Disables "map" callvote. Doesn't affect opcalls. |
| g_disable_vote_maxteamplayers | \* | 0 | \<0/1\> | Disables "maxteamplayers" callvote. Doesn't affect opcalls. |
| g_disable_vote_mute | \* | 0 | \<0/1\> | Disables "mute" callvote. Doesn't affect opcalls. |
| g_disable_vote_nextmap | \* | 0 | \<0/1\> | Disables "nextmap" callvote. Doesn't affect opcalls. |
| g_disable_vote_numbots | \* | 0 | \<0/1\> | Disables "numbots" callvote. Doesn't affect opcalls. |
| g_disable_vote_rebalance | \* | 0 | \<0/1\> | Disables "rebalance" callvote. Doesn't affect opcalls. |
| g_disable_vote_remove | \* | 0 | \<0/1\> | Disables "remove" callvote. Doesn't affect opcalls. |
| g_disable_vote_restart | \* | 0 | \<0/1\> | Disables "restart" callvote. Doesn't affect opcalls. |
| g_disable_vote_scorelimit | \* | 0 | \<0/1\> | Disables "scorelimit" callvote. Doesn't affect opcalls. |
| g_disable_vote_shuffle | \* | 0 | \<0/1\> | Disables "shuffle" callvote. Doesn't affect opcalls. |
| g_disable_vote_timein | \* | 0 | \<0/1\> | Disables "timein" callvote. Doesn't affect opcalls. |
| g_disable_vote_timelimit | \* | 0 | \<0/1\> | Disables "timelimit" callvote. Doesn't affect opcalls. |
| g_disable_vote_timeout | \* | 0 | \<0/1\> | Disables "timeout" callvote. Doesn't affect opcalls. |
| g_disable_vote_unlock | \* | 0 | \<0/1\> | Disables "unlock" callvote. Doesn't affect opcalls. |
| g_disable_vote_unmute | \* | 0 | \<0/1\> | Disables "unmute" callvote. Doesn't affect opcalls. |
| g_disable_vote_vmute | \* | 0 | \<0/1\> | Disables "vmute" callvote. Doesn't affect opcalls. |
| g_disable_vote_vunmute | \* | 0 | \<0/1\> | Disables "vunmute" callvote. Doesn't affect opcalls. |
| g_disable_vote_warmup_timelimit | \* | 0 | \<0/1\> | Disables "warmup_timelimit" callvote. Doesn't affect opcalls. |
| g_enforce_map_pool | \* | 0 | \<0/1\> | Enables enforcing the map pool for "map" callvote. |
| g_floodprotection_delay |  | 10 | \<value\> | Blocks the chat for x seconds to player who triggered the flood protection. |
| g_floodprotection_messages |  | 4 | \<value\> | How many messages can a player send in y seconds before triggering the flood protection. |
| g_floodprotection_seconds |  | 4 | \<value\> | Triggers flood protection if a player sends more than x messages in y seconds. |
| g_floodprotection_team |  | 0 | \<value\> | Triggers flood protection if a player sends more than x team messages in y seconds. |
| g_gametype | \*, S, L | dm | \<gametype\> | Changes the gametype. Requires server restart / map reload. |
| g_gametypes_available | S, - |  | \*write protected\* |  |
| g_gametypes_list | \*, - |  | \*write protected\* |  |
| g_gravity |  | 850 | \<value\> | Obsolete ConVar. |
| g_health_respawn | \* | 0 |  |  |
| g_inactivity_maxtime |  | 90.0 | \<value\> | A player will get moved to spectators team if inactive for longer than x seconds (doesn't affect warmup). |
| g_instagib | \*, S, L | 0 | \<0/1\> | Enables InstaGib. Requires server restart. |
| g_instajump | \* | 1 | \<0/1\> | Enables InstaJump. |
| g_instashield | \* | 1 | \<0/1\> | Enables InstaShield. |
| g_knockback_scale | \* | 1.0 | \<value\> | Changes the knockback scale of weapons. Affects normal weapons AND Instagun. |
| g_map_pool | \* |  | \<maplist\> | Only allows these maps to appear in "map" callvote. Needs g_enforce_map_pool set to 1. |
| g_maplist | \* |  | \<maplist\> | Sets the server's map list. |
| g_maprotation | \* | 1 | \<0-2\> | Sets map rotation mode. 0 - same map, 1 - in order, 2 - random. |
| g_match_extendedtime | \* | 2 | \<value\> | Changes the overtime's length to x minutes. 0 to disable. |
| g_match_score | S, - |  | \*write protected\* |  |
| g_match_time | S, - |  | \*write protected\* |  |
| g_maxtimeouts | \* | 2 | \<value\> | How many timeouts can be called per match. |
| g_maxvelocity |  | 16000 | \<value\> | Obsolete ConVar. |
| g_needpass | S, - | 1 | \*write protected\* |  |
| g_numbots | \* | 0 | \<value\> | Amount of bots on the server. |
| g_operator_password | \* |  | \<password\> | Sets the operator password. Operator is disabled if empty. |
| g_postmatch_timelimit | \* | 4 | \<value\> |  |
| g_race_gametype | S, - | 0 | \*write protected\* |  |
| g_scorelimit | \* | 0 | \<value\> | Amount of points required to obtain by a player / team to end the match. |
| g_spawnsystem_wave_maxcount | \* | 16 | \<value\> |  |
| g_spawnsystem_wave_time | \* | 15 | \<value\> |  |
| g_teams_allow_uneven | \* | 1 | \<0/1\> | Allow the teams to be uneven. If enabled, allows players to switch teams anytime. |
| g_teams_maxplayers | \* | 0 | \<value\> | How many players can a single team have. |
| g_timelimit | \* | 10 | \<value\> | Sets the duration of matches (in minutes). |
| g_uploads_demos |  | 1 | \<0/1\> | Allows players to download demos from the server. |
| g_votable_gametypes | \* |  | \<gametypes\> | A list of gametypes allowed to be used in "gametype" callvote. |
| g_vote_allowed | \* | 1 | \<0/1\> | Allows / disallows calling ALL votes (including opcalls). |
| g_vote_cooldowntime | \* | 5 | \<value\> | A player needs to wait x seconds after calling a vote to call another one. |
| g_vote_electtime | \* | 20 | \<value\> | Specifies how long do callvotes last (in seconds). |
| g_vote_maxchanges | \* | 3 | \<value\> | Specifies how many times can a player change their vote. |
| g_vote_percent | \* | 55 | \<0-100\> | How much % of players need to vote yes for the vote to pass. |
| g_warmup_timelimit | \* | 5 | \<value\> | Sets how long do warmups take (in minutes). |
| g_weapon_respawn | \* | 0 |  |  |

### gl\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>gl_cull</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enable OpenGL Culling.</td>
</tr>
<tr>
<td>gl_drawbuffer</td>
<td></td>
<td>GL_BACK</td>
<td>&lt;value&gt;</td>
<td>Specifies the buffer which display information will be written to.</td>
</tr>
<tr>
<td>gl_driver_win</td>
<td>*, L</td>
<td>opengl32.dll</td>
<td>&lt;value&gt;</td>
<td>Specifies the OpenGL driver dll file.</td>
</tr>
<tr>
<td>gl_ext_bgra</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td>If enabled, the BGRA openGL extension will be used if supported.</td>
</tr>
<tr>
<td>gl_ext_blend_func_separate</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_compressed_ETC1_RGB8_texture</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_depth24</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_depth_nonlinear</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_depth_texture</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_draw_instanced</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_draw_range_elements</td>
<td>*, L</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, DrawRangeElements (an opengl extension) will be used if it's supported.</td>
</tr>
<tr>
<td>gl_ext_ES3_compatibility</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_fragment_precision_high</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_fragment_shader</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_framebuffer_blit</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_framebuffer_object</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_gamma_control</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_get_program_binary</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_GLSL</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_GLSL130</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_GLSL_core</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_gpu_memory_info</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_gpu_shader5</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_half_float_vertex</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_instanced_arrays</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_meminfo</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_multitexture</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_packed_depth_stencil</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_rgb8_rgba8</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_shader_objects</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_shading_language_100</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_shading_language_130</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_shadow</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_shadow_samplers</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_swap_control</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture3D</td>
<td>*, L</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the Texture3D (an opengl extension) will be used if it's supported.</td>
</tr>
<tr>
<td>gl_ext_texture_array</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_compression</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_cube_map</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td>If enabled, Texture Cube Mapping (an opengl extension) will be used if it's supported.</td>
</tr>
<tr>
<td>gl_ext_texture_edge_clamp</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_filter_anisotropic</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_lod</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_non_power_of_two</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_texture_npot</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_vertex_buffer_object</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td>If enabled, opengl vertex buffer objects will be utilized if supported.
Vertex buffer objects are often slower than range elements.</td>
</tr>
<tr>
<td>gl_ext_vertex_buffer_object_hack</td>
<td>*, -</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_ext_vertex_half_float</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gl_ext_vertex_shader</td>
<td>*, -</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>gl_finish</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the CPU will wait for the GPU at the end of each rendered frame.
This can help resolve some video lag and input issues.</td>
</tr>
<tr>
<td>gl_max_texture_size</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
</tbody>
</table>

### http\_

| Command           | Flags | Default | Parameters | Description |
|-------------------|-------|---------|------------|-------------|
| http_proxy        | \*    |         |            |             |
| http_proxyuserpwd | \*    |         |            |             |

### in\_

| Command          | Flags | Default | Parameters          | Description         |
|------------------|-------|---------|---------------------|---------------------|
| in_debug         |       | 0       |                     |                     |
| in_dinput        |       | 1       |                     |                     |
| in_grabinconsole | \*    | 0       |                     |                     |
| in_initmouse     | \-    | 1       | \*write protected\* |                     |
| in_mouse         | \*    | 1       | \<0/1\>             | Enables mouse input |

### irc\_

| Command | Flags | Default | Parameters | Description |
|----|----|----|----|----|
| irc_nick | \* | WarforkPlayer | \<value\> | Sets your nickname. |
| irc_password | \* | \<undefined\> | \<value\> | Specifies a password for IRC Servers which require one to connect. |
| irc_port | \* | 6667 | \<value\> | Specifies a port for the IRC Server you're connecting to. |
| irc_server | \* | irc.quakenet.org | \<value\> | Specifies a ip\hostname for the IRC Server you're connecting to. |
| irc_user | \* | WarforkUser | \<value\> | Specifies a username for IRC Servers which require one to connect. |

### logconsole\_

| Command              | Flags | Default | Parameters | Description |
|----------------------|-------|---------|------------|-------------|
| logconsole           | \*    |         |            |             |
| logconsole_append    | \*    | 1       |            |             |
| logconsole_flush     | \*    | 0       |            |             |
| logconsole_timestamp | \*    | 0       |            |             |

### m\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>m_accel</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Mouse acceleration multiplier.</td>
</tr>
<tr>
<td>m_accelOffset</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Enables different mouse acceleration styles.
0 = Disabled, 1 = Weakens amplification effect if you move your mouse slower, 2 = Minimum distance for mouse movement to be registered.</td>
</tr>
<tr>
<td>m_accelPow</td>
<td>*</td>
<td>2</td>
<td>&lt;value&gt;</td>
<td>Determines the rate of acceleration for m_accelStyle = 2.
Must be greater than 2 to not decelerate.</td>
</tr>
<tr>
<td>m_accelStyle</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Style of mouse acceleration.
0 = Legacy style, 1 = Quake Live style, 2 = Extended legacy style with offset and variable pow mechanisms.</td>
</tr>
<tr>
<td>m_filter</td>
<td>*</td>
<td>0</td>
<td>&lt;0-2&gt;</td>
<td>If enabled the type of filtering applied to your mouse input will be changed.
0 = Off, 1 = Linear interpolation filtering, 2 = Extrapolation filtering.</td>
</tr>
<tr>
<td>m_filterStrength</td>
<td>*</td>
<td>0.5</td>
<td>&lt;value&gt;</td>
<td>Controls the strength of m_filter.</td>
</tr>
<tr>
<td>m_forward</td>
<td></td>
<td>1</td>
<td>&lt;value&gt;</td>
<td>Changes your mouse sensitivity when moving forward and back.</td>
</tr>
<tr>
<td>m_pitch</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>The sensitivity for looking up and down with the mouse.</td>
</tr>
<tr>
<td>m_raw</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables raw mouse data input.</td>
</tr>
<tr>
<td>m_sensCap</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Affects the maximum limit for m_accelStyle = 2.</td>
</tr>
<tr>
<td>m_side</td>
<td></td>
<td>1</td>
<td>&lt;value&gt;</td>
<td>Changes your mouse sensitivity when moving left and right.</td>
</tr>
<tr>
<td>m_yaw</td>
<td>*</td>
<td>0.022</td>
<td>&lt;value&gt;</td>
<td>Changes speed scale of X axis.</td>
</tr>
</tbody>
</table>

### r\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>r_brightness</td>
<td>*</td>
<td>0</td>
<td>&lt;0-1.0&gt;</td>
<td>Sets the brightness level on your screen.</td>
</tr>
<tr>
<td>r_coronascale</td>
<td></td>
<td>0.4</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_detailtextures</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, detailed textures will be shown.</td>
</tr>
<tr>
<td>r_drawelements</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables drawing elements.</td>
</tr>
<tr>
<td>r_drawentities</td>
<td>C</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables drawing entities.</td>
</tr>
<tr>
<td>r_drawflat</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, will draw the floor and walls as solid colors.</td>
</tr>
<tr>
<td>r_draworder</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_drawworld</td>
<td>C</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables drawing the world.</td>
</tr>
<tr>
<td>r_dynamiclight</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables dynamic light.</td>
</tr>
<tr>
<td>r_environment_color</td>
<td></td>
<td>0 0 0</td>
<td></td>
<td>Changes the background color if r_drawworld is 0</td>
</tr>
<tr>
<td>r_faceplanecull</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, only the polygons of the face will be rendered.
This command doesn't work and exists only in default.cfg. It will be purged and moved into the deprecated commands section soon.</td>
</tr>
<tr>
<td>r_fastsky</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, only a basic skybox will be drawn.</td>
</tr>
<tr>
<td>r_floorcolor</td>
<td>*</td>
<td>255 153 0</td>
<td>&lt;R G B&gt;</td>
<td>The color of floor if r_drawflat = 1.
Examples: <a href=":File:Drawflat_red.jpg" class="wikilink" title="Red">Red</a>, <a href=":File:Drawflat_green.jpg" class="wikilink" title="Green">Green</a>, <a href=":File:Drawflat_blue.jpg" class="wikilink" title="Blue">Blue</a></td>
</tr>
<tr>
<td>r_fullbright</td>
<td>L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Sets maximum brightness to all textures.</td>
</tr>
<tr>
<td>r_fxaa</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables FXAA antialiasing.</td>
</tr>
<tr>
<td>r_gamma</td>
<td>*</td>
<td>1.0</td>
<td>&lt;value&gt;</td>
<td>Changes the gamma.</td>
</tr>
<tr>
<td>r_ignorehwgamma</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_leafvis</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lerpmodels</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_ambientscale</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_deluxemapping</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_directedscale</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_glossexponent</td>
<td>*</td>
<td>24</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_glossintensity</td>
<td>*</td>
<td>1.5</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_grayscale</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables grayscale lighting.</td>
</tr>
<tr>
<td>r_lighting_maxglsldlights</td>
<td>*</td>
<td>16</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_maxlmblocksize</td>
<td>*, L</td>
<td>2048</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_packlightmaps</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_specular</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lighting_vertexlight</td>
<td>*, L</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lightmap</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, all textures will not be displayed and only static lights will be visible.</td>
</tr>
<tr>
<td>r_lockpvs</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lodbias</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_lodscale</td>
<td>*</td>
<td>5.0</td>
<td>&lt;value&gt;</td>
<td>This value adjusts the level of detail scale modifier.</td>
</tr>
<tr>
<td>r_mapoverbrightbits</td>
<td>*, L</td>
<td>2</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_maxfps</td>
<td>*</td>
<td>250</td>
<td>&lt;24-1000&gt;</td>
<td>Sets the FPS limit.</td>
</tr>
<tr>
<td>r_maxglslbones</td>
<td>L</td>
<td>100</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_multithreading</td>
<td>*, L</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables multithreading.</td>
</tr>
<tr>
<td>r_nobind</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_nocull</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_norefresh</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_novis</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_offsetmapping</td>
<td>*</td>
<td>2</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_offsetmapping_reliefmapping</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_offsetmapping_scale</td>
<td>*</td>
<td>0.02</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_outlines_cutoff</td>
<td>*</td>
<td>712</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_outlines_scale</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_outlines_world</td>
<td>*</td>
<td>1.8</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_overbrightbits</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_packlightmaps</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_picmip</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0-16&gt;</td>
<td>Overall image and texture quality. The highest the number the lower the quality level.</td>
</tr>
<tr>
<td>r_polyblend</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_portalmaps</td>
<td>*, L</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_portalmaps_maxtexsize</td>
<td>*</td>
<td>1024</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_portalonly</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_screenshot_fmtstr</td>
<td>*</td>
<td>wf_y%m%d_HM%S</td>
<td>&lt;date format&gt;</td>
<td>File name format of screenshots.</td>
</tr>
<tr>
<td>r_screenshot_jpeg</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables .jpeg screenshots.</td>
</tr>
<tr>
<td>r_screenshot_jpeg_quality</td>
<td>*</td>
<td>90</td>
<td>&lt;0-100&gt;</td>
<td>Sets the quality of jpeg screenshots, in percentages.</td>
</tr>
<tr>
<td>r_shadows</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_alpha</td>
<td>*</td>
<td>0.7</td>
<td>&lt;0-1&gt;</td>
<td>Alpha of shadows.</td>
</tr>
<tr>
<td>r_shadows_dither</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_maxtexsize</td>
<td>*</td>
<td>64</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_nudge</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_pcf</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_projection_distance</td>
<td>C</td>
<td>64</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shadows_self_shadow</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_shownormals</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_showtris</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_skymip</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0-16&gt;</td>
<td>Overall image and texture quality of the skybox. The highest the number the lower the quality level.</td>
</tr>
<tr>
<td>r_soft_particles</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables soft particles.</td>
</tr>
<tr>
<td>r_soft_particles_available</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>r_soft_particles_scale</td>
<td>*</td>
<td>0.02</td>
<td></td>
<td>Scale of soft particles.</td>
</tr>
<tr>
<td>r_speeds</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_stencilbits</td>
<td>*, L</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_subdivisions</td>
<td>*, L</td>
<td>5</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_swapinterval</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_swapinterval_min</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>r_temp1</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_texturebits</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, vsync will be activated.
Set vid_displayfrequency to your preferred value.</td>
</tr>
<tr>
<td>r_texturecompression</td>
<td>*, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables texture compression.</td>
</tr>
<tr>
<td>r_texturefilter</td>
<td>*</td>
<td>4</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_texturefilter_max</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>r_texturemode</td>
<td>*</td>
<td>GL_LINEAR_MIPMAP_LINEAR</td>
<td></td>
<td></td>
</tr>
<tr>
<td>r_usenotexture</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Disables textures.</td>
</tr>
<tr>
<td>r_wallcolor</td>
<td>*</td>
<td>255 255 255</td>
<td>&lt;R G B&gt;</td>
<td>The color of walls if r_drawflat = 1.
Examples: <a href=":File:Drawflat_red.jpg" class="wikilink" title="Red">Red</a>, <a href=":File:Drawflat_green.jpg" class="wikilink" title="Green">Green</a>, <a href=":File:Drawflat_blue.jpg" class="wikilink" title="Blue">Blue</a></td>
</tr>
</tbody>
</table>

### rcon\_

| Command | Flags | Default | Parameters | Description |
|----|----|----|----|----|
| rcon_address |  | \<undefined\> | \<ip address\> | Sets the IP address for rcon connection. |
| rcon_password |  | \<undefined\> | \<password\> | Sets the password for rcon connection. |

### s\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>s_doppler</td>
<td>*</td>
<td>1.0</td>
<td>&lt;value&gt;</td>
<td>If enabled, Doppler effect will be used for sounds</td>
</tr>
<tr>
<td>s_globalfocus</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Mutes the game when alt-tabbed.
0 = Disabled, 1 = Enabled</td>
</tr>
<tr>
<td>s_khz</td>
<td>*</td>
<td>44</td>
<td>&lt;value&gt;</td>
<td>The sampling rate of the sounds in kilohertz.</td>
</tr>
<tr>
<td>s_mixahead</td>
<td>*</td>
<td>0.14</td>
<td>&lt;value&gt;</td>
<td>The specified time waited before mixing sound samples.</td>
</tr>
<tr>
<td>s_module</td>
<td>*, L</td>
<td>1</td>
<td>&lt;0-2&gt;</td>
<td>Specifies the default sound module.
0 = No Sound, 1 = Qfusion, 2 = OpenAL</td>
</tr>
<tr>
<td>s_module_fallback</td>
<td>L</td>
<td>2</td>
<td>&lt;0-2&gt;</td>
<td>Specifies a fallback sound module incase s_module cannot be loaded.</td>
</tr>
<tr>
<td>s_musicvolume</td>
<td>*</td>
<td>0.15</td>
<td>&lt;0-1&gt;</td>
<td>Global music volume.</td>
</tr>
<tr>
<td>s_openAL_device</td>
<td>*, L</td>
<td>Generic Software</td>
<td>&lt;value&gt;</td>
<td>Specifies the OpenAL device.
Example: s_openAL_device "Rapture3D"</td>
</tr>
<tr>
<td>s_pseudoAcoustics</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>High quality spatialisation for the Qfusion Sound Module.</td>
</tr>
<tr>
<td>s_separationDelay</td>
<td>*</td>
<td>1.0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>s_stereo2mono</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables mono sound.</td>
</tr>
<tr>
<td>s_swapstereo</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Swap the left and right sound channel.</td>
</tr>
<tr>
<td>s_volume</td>
<td>*</td>
<td>0.8</td>
<td>&lt;0-1&gt;</td>
<td>Global volume of the game.</td>
</tr>
<tr>
<td>s_wavonly</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, only .wav sound files will be played.</td>
</tr>
</tbody>
</table>

### scr\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>scr_consize</td>
<td>*</td>
<td>0.4</td>
<td>&lt;0.1-1.0&gt;</td>
<td>size of the console "0.1-1.0"
0.1 = Smallest size, 0.5 = 50% of the screen, 1.0 = 100% of the screen.</td>
</tr>
<tr>
<td>scr_conspeed</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Controls the console drop-down speed.
0 = Instant, 1 = Slowest, and anything higher than 1 increases the speed.</td>
</tr>
</tbody>
</table>

### sv\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>sv_autoUpdate</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_botpersonality</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_cheats</td>
<td>S, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables cheats on the server.</td>
</tr>
<tr>
<td>sv_debug_serverCmd</td>
<td>*</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_defaultmap</td>
<td>*</td>
<td>wfdm1</td>
<td>&lt;map&gt;</td>
<td>Changes the default map of the server.</td>
</tr>
<tr>
<td>sv_demodir</td>
<td>-</td>
<td></td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_enforcetime</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_fps</td>
<td>-</td>
<td>62</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_highchars</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_hostname</td>
<td>*, S</td>
<td></td>
<td>&lt;name&gt;</td>
<td>Name of the server. Appears in the server list.</td>
</tr>
<tr>
<td>sv_http</td>
<td>*, S, L</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>Enables an HTTP server that lets connecting players download missing files.</td>
</tr>
<tr>
<td>sv_http_ip</td>
<td>*, L</td>
<td></td>
<td>&lt;ip address&gt;</td>
<td>If set, binds the HTTP server to a specific IPv4 address.</td>
</tr>
<tr>
<td>sv_http_ipv6</td>
<td>*, L</td>
<td></td>
<td>&lt;ip address&gt;</td>
<td>If set, binds the HTTP server to a specific IPv6 address.</td>
</tr>
<tr>
<td>sv_http_port</td>
<td>*, L</td>
<td>44444</td>
<td>&lt;port&gt;</td>
<td>Changes the port of the HTTP server.</td>
</tr>
<tr>
<td>sv_http_upstream_baseurl</td>
<td>*, L</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_http_upstream_ip</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_http_upstream_realip_header</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_ip</td>
<td>*, L</td>
<td></td>
<td>&lt;ip address&gt;</td>
<td>If set, binds the Warfork server to a specific IPv4 address.</td>
</tr>
<tr>
<td>sv_ip6</td>
<td>*, L</td>
<td><dl>
<dt></dt>
<dd>
<dl>
<dt></dt>
<dd>
&#10;</dd>
</dl>
</dd>
</dl></td>
<td>&lt;ip address&gt;</td>
<td>If set, binds the Warfork server to a specific IPv6 address.</td>
</tr>
<tr>
<td>sv_iplimit</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Maximum amount of connections from a single IP address.</td>
</tr>
<tr>
<td>sv_lastAutoUpdate</td>
<td>*, -</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_maxclients</td>
<td>*, S, L</td>
<td></td>
<td>&lt;value&gt;</td>
<td>Maximum amount of players allowed on the server.</td>
</tr>
<tr>
<td>sv_maxentities</td>
<td>*, L</td>
<td>1024</td>
<td>&lt;value&gt;</td>
<td>Maximum amount of entities on the map.</td>
</tr>
<tr>
<td>sv_maxmvclients</td>
<td>*, S</td>
<td>4</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_mm_authkey</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_mm_debug_reportbots</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_mm_enable</td>
<td>*, S, -</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_mm_loginonly</td>
<td>*, S</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_modmanifest</td>
<td>-</td>
<td></td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_MOTD</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Enables Message Of The Day on the server.</td>
</tr>
<tr>
<td>sv_MOTDFile</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;path&gt;</td>
<td>Path to Message Of The Day file.</td>
</tr>
<tr>
<td>sv_MOTDString</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>A definable MOTD String that takes precedence over sv_MOTDFile.
MOTD String only updates after a map change.</td>
</tr>
<tr>
<td>sv_port</td>
<td>*, L</td>
<td>44400</td>
<td>&lt;port&gt;</td>
<td>Changes the IPv4 port of the Warfork server.</td>
</tr>
<tr>
<td>sv_port6</td>
<td>*, L</td>
<td>44400</td>
<td>&lt;port&gt;</td>
<td>Changes the IPv6 port of the Warfork server.</td>
</tr>
<tr>
<td>sv_pps</td>
<td>S</td>
<td>20</td>
<td>&lt;value&gt;</td>
<td>Packets per second a server sends to the client.</td>
</tr>
<tr>
<td>sv_public</td>
<td>*</td>
<td></td>
<td>&lt;0/1&gt;</td>
<td>If set to 1, the server will appear on the public server list.</td>
</tr>
<tr>
<td>sv_pure</td>
<td>*, S, L</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If set to 1, the server will check the validity of client files with server. Kicks if invalid.</td>
</tr>
<tr>
<td>sv_pure_forcemodulepk3</td>
<td>L</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_reconnectlimit</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Seconds a client must wait until they can reconnect with a server.</td>
</tr>
<tr>
<td>sv_showChallenge</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_showclamp</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_showInfoQueries</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_showRcon</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_skilllevel</td>
<td>*, S, L</td>
<td>2</td>
<td>&lt;0-2&gt;</td>
<td>Defines the skill level of your server, which affects bots.
0 = Easy, 1 = Medium, 2 = Hard.</td>
</tr>
<tr>
<td>sv_skillRating</td>
<td>S, -</td>
<td>0</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_timeout</td>
<td></td>
<td>125</td>
<td>&lt;value&gt;</td>
<td>Kicks players from server if connection is lost for more than x seconds. Takes priority over cl_timeout.</td>
</tr>
<tr>
<td>sv_uploads</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_uploads_baseurl</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_uploads_demos</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_uploads_demos_baseurl</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>sv_uploads_from_server</td>
<td></td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, uploading is allowed directly from the server.</td>
</tr>
<tr>
<td>sv_uploads_http</td>
<td>-</td>
<td>1</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>sv_zombietime</td>
<td></td>
<td>2</td>
<td>&lt;value&gt;</td>
<td>Determines how long a connected client remains open after it has either timed out with sv_timeout or disconnected.</td>
</tr>
</tbody>
</table>

### ui\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>ui_autobrowse_manual</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, servers will be suggested when you click "Play" and query the masterservers.</td>
</tr>
<tr>
<td>ui_basepath</td>
<td>*</td>
<td>ui/porkui</td>
<td>&lt;value&gt;</td>
<td>Defines the basepath of the user interface.</td>
</tr>
<tr>
<td>ui_cachepurgedate</td>
<td>*</td>
<td>&lt;undefined&gt;</td>
<td>&lt;yyyy-mm-dd&gt;</td>
<td>Purges the folder "cache/ui" on a specific date, which contains cache from asyncrhonous HTTP requests.
Example: 2020-02-13</td>
</tr>
<tr>
<td>ui_lighting</td>
<td></td>
<td>2</td>
<td></td>
<td></td>
</tr>
<tr>
<td>ui_preload</td>
<td>*</td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>ui_serverbrowser_tab</td>
<td>*</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>ui_tutorial_taken</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, you will be prompted (once per game load) to complete the tutorial upon clicking "Play".</td>
</tr>
<tr>
<td>ui_video_profile</td>
<td>*</td>
<td>medium</td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

### vid\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>vid_displayfrequency</td>
<td>*, L</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Defines the refresh rate of your screen in Hz.
0 = Desktop Default</td>
</tr>
<tr>
<td>vid_fullscreen</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, Warfork will run in full screen mode.</td>
</tr>
<tr>
<td>vid_height</td>
<td>*, L</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Defines a custom screen resolution height.
0 = Desktop Default</td>
</tr>
<tr>
<td>vid_multiscreen_head</td>
<td>*</td>
<td>-1</td>
<td>&lt;value&gt;</td>
<td>Changes the default monitor used.</td>
</tr>
<tr>
<td>vid_parentwid</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>Defines the parent window identifier.</td>
</tr>
<tr>
<td>vid_ref</td>
<td>*, L</td>
<td>ref_gl</td>
<td>&lt;value&gt;</td>
<td>Defines the video renderer driver.</td>
</tr>
<tr>
<td>vid_width</td>
<td>*, L</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Defines a custom screen resolution width.
0 = Desktop Default</td>
</tr>
<tr>
<td>vid_xpos</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Defines the X position of the game running in window mode.</td>
</tr>
<tr>
<td>vid_ypos</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Defines the Y position of the game running in window mode.</td>
</tr>
</tbody>
</table>

### win\_

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>win_noalttab</td>
<td>*</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, ALT+TAB will work.
0 = Disabled - 1 Enabled</td>
</tr>
<tr>
<td>win_nowinkeys</td>
<td>*</td>
<td>1</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, Windows keys will work.
0 = Disabled - 1 Enabled</td>
</tr>
</tbody>
</table>

### Prefixless cvars & cvars with unique prefixes

<table>
<thead>
<tr>
<th>Command</th>
<th>Flags</th>
<th>Default</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>clan</td>
<td>*, U</td>
<td></td>
<td>&lt;name&gt;</td>
<td>Sets the name of your clan. Appears on the scoreboard.</td>
</tr>
<tr>
<td>color</td>
<td>*, U</td>
<td>255 255 255</td>
<td>&lt;R G B&gt;</td>
<td>Sets your Player color.</td>
</tr>
<tr>
<td>debuggraph</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the debug graph will be displayed.</td>
</tr>
<tr>
<td>dedicated</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>Tells the game if it's a dedicated server.</td>
</tr>
<tr>
<td>developer</td>
<td>C</td>
<td>0</td>
<td></td>
<td>Level of developer information printed to the console. The higher the number, the more information is printed.</td>
</tr>
<tr>
<td>developerMemory</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Prints memory allocation information to console if developer is enabled as well.</td>
</tr>
<tr>
<td>favorites</td>
<td>*</td>
<td>0</td>
<td></td>
<td>Amount of favorite servers.</td>
</tr>
<tr>
<td>filterban</td>
<td></td>
<td>1</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fixedtime</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fov</td>
<td>*</td>
<td>100</td>
<td>&lt;value&gt;</td>
<td>Changes your Field of view.</td>
</tr>
<tr>
<td>gamedate</td>
<td>S, L</td>
<td>Oct 8 2019</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gamename</td>
<td>S, -</td>
<td>Warfork</td>
<td>*write protected*</td>
<td>Name of the game.</td>
</tr>
<tr>
<td>graphheight</td>
<td></td>
<td>32</td>
<td></td>
<td>Changes the graph height for timegraph, netgraph, etc.</td>
</tr>
<tr>
<td>graphscale</td>
<td></td>
<td>1</td>
<td></td>
<td>Scales the graph (timegraph, netgraph, etc.) for resolutions with a width greather than 1024.</td>
</tr>
<tr>
<td>graphshift</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>hand</td>
<td>*, U</td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>Changes weapon handedness.
0 = right, 1 = left</td>
</tr>
<tr>
<td>handicap</td>
<td>*, U</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Decreases your damage output by x% usefull for dueling players below your skill level</td>
</tr>
<tr>
<td>host_speeds</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled timing information will be printed to console.
all (total time), sv (server time), gm (game time), cl (client time), and rf (renderer time).</td>
</tr>
<tr>
<td>lang</td>
<td>*, L</td>
<td></td>
<td>&lt;language&gt;</td>
<td>Sets the language of Warfork.</td>
</tr>
<tr>
<td>lookspring</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the screen will be automatically centered when using +mlook.</td>
</tr>
<tr>
<td>lookstrafe</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, automatic strafing will be toggled when using +mlook.</td>
</tr>
<tr>
<td>mapname</td>
<td>S, -</td>
<td></td>
<td>*write protected*</td>
<td>The name of current map played.</td>
</tr>
<tr>
<td>masterservers</td>
<td>L</td>
<td>master1.forbidden.gg master1.icy.gg</td>
<td>&lt;value&gt;</td>
<td>Specifies the master servers used to query a list of Warfork servers.</td>
</tr>
<tr>
<td>masterservers_steam</td>
<td>L</td>
<td>&lt;undefined&gt;</td>
<td>&lt;value&gt;</td>
<td>Specifies the Steam master servers used to query a list of Warfork servers.</td>
</tr>
<tr>
<td>mm_url</td>
<td>*, -</td>
<td><a href="https://mm.forbidden.gg:1338">https://mm.forbidden.gg:1338</a></td>
<td>*write protected*</td>
<td>Specifies the Warfork Matchmaking Servers</td>
</tr>
<tr>
<td>model</td>
<td>*, U</td>
<td>bigvic</td>
<td>&lt;model name&gt;</td>
<td>Changes your Player model.</td>
</tr>
<tr>
<td>name</td>
<td>*, U</td>
<td></td>
<td>&lt;name&gt;</td>
<td>Changes your nickname.</td>
</tr>
<tr>
<td>net_showfragments</td>
<td></td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>netgraph</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, information will be displayed on the bottom of the screen about all network packets.</td>
</tr>
<tr>
<td>nextmap</td>
<td></td>
<td>match "advance"</td>
<td>&lt;value&gt;</td>
<td>Proceeds to the next map.</td>
</tr>
<tr>
<td>password</td>
<td>*, U</td>
<td></td>
<td>&lt;password&gt;</td>
<td>If a server requires a password, the client automatically tries to join with x password.</td>
</tr>
<tr>
<td>protocol</td>
<td>S, -</td>
<td>22</td>
<td>*write protected*</td>
<td></td>
</tr>
<tr>
<td>revision</td>
<td>-</td>
<td>Oct 8 2019 00:08:07</td>
<td>*write protected*</td>
<td>Date when the game was compiled.</td>
</tr>
<tr>
<td>sensitivity</td>
<td>*</td>
<td>3</td>
<td>&lt;value&gt;</td>
<td>Changes sensitivity of your mouse.</td>
</tr>
<tr>
<td>showdrop</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, information will be displayed in the console about dropped network packets.</td>
</tr>
<tr>
<td>showpackets</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, information will be displayed in the console about all network packets.</td>
</tr>
<tr>
<td>skin</td>
<td>*, U</td>
<td>default</td>
<td></td>
<td></td>
</tr>
<tr>
<td>timedemo</td>
<td>C</td>
<td>0</td>
<td></td>
<td></td>
</tr>
<tr>
<td>timegraph</td>
<td></td>
<td>0</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, a graph will be displayed, which visualizes the compression and expansion of game time, which is necessary maintain the overall game time constant.</td>
</tr>
<tr>
<td>timescale</td>
<td>C</td>
<td>1.0</td>
<td>&lt;value&gt;</td>
<td>Changes the time scale of the game.</td>
</tr>
<tr>
<td>tv_server</td>
<td>-</td>
<td>0</td>
<td>*write protected*</td>
<td>Tells the game if the server is a TV server.</td>
</tr>
<tr>
<td>version</td>
<td>S, -</td>
<td>2.10 x64 Oct 8 2019 Win32 RELEASE</td>
<td>*write protected*</td>
<td>The version of the game.</td>
</tr>
<tr>
<td>zoomfov</td>
<td>*</td>
<td>30</td>
<td>&lt;value&gt;</td>
<td>Changes the field of view while zooming.</td>
</tr>
<tr>
<td>zoomsens</td>
<td>*</td>
<td>0</td>
<td>&lt;value&gt;</td>
<td>Changes your sensitivity while zooming.
0 = uses your normal sensitivity.</td>
</tr>
</tbody>
</table>

## Commands

<table>
<thead>
<tr>
<th>Command</th>
<th>Parameters</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>+attack</td>
<td></td>
<td>Primary attack.</td>
</tr>
<tr>
<td>+back</td>
<td></td>
<td>Moves backward.</td>
</tr>
<tr>
<td>+forward</td>
<td></td>
<td>Moves forward.</td>
</tr>
<tr>
<td>+klook</td>
<td></td>
<td>Keyboard look; +forward +back serve as +lookup +lookdown.</td>
</tr>
<tr>
<td>+left</td>
<td></td>
<td>Turns left.</td>
</tr>
<tr>
<td>+lookdown</td>
<td></td>
<td>Looks down.</td>
</tr>
<tr>
<td>+lookup</td>
<td></td>
<td>Looks up.</td>
</tr>
<tr>
<td>+movedown</td>
<td></td>
<td>Moves backwards.</td>
</tr>
<tr>
<td>+moveleft</td>
<td></td>
<td>Moves left.</td>
</tr>
<tr>
<td>+moveright</td>
<td></td>
<td>Moves right.</td>
</tr>
<tr>
<td>+moveup</td>
<td></td>
<td>Moves up; In water, lava, etc.</td>
</tr>
<tr>
<td>+quickmenu</td>
<td></td>
<td>An easily accessible menu with basic commands such as Voice Says.
By default it is bound to LSHIFT.</td>
</tr>
<tr>
<td>+right</td>
<td></td>
<td>Turns right.</td>
</tr>
<tr>
<td>+scores</td>
<td></td>
<td>Accesses the scoreboard.</td>
</tr>
<tr>
<td>+special</td>
<td></td>
<td></td>
</tr>
<tr>
<td>+speed</td>
<td></td>
<td>Changes your speed.
If run is enabled you will walk or vice versa when used. This serves no purpose as Warfork has no footstep sounds.</td>
</tr>
<tr>
<td>+strafe</td>
<td></td>
<td>When used +left and +right are changed with +moveleft and +moveright.</td>
</tr>
<tr>
<td>+use</td>
<td></td>
<td>Uses an item.</td>
</tr>
<tr>
<td>+zoom</td>
<td></td>
<td>Zooms.</td>
</tr>
<tr>
<td>-attack</td>
<td></td>
<td>Stops primary attack.</td>
</tr>
<tr>
<td>-back</td>
<td></td>
<td>Stops moving backward.</td>
</tr>
<tr>
<td>-forward</td>
<td></td>
<td>Stops moving forward.</td>
</tr>
<tr>
<td>-klook</td>
<td></td>
<td>Stops Keyboard look; +forward +back serve as +lookup +lookdown.</td>
</tr>
<tr>
<td>-left</td>
<td></td>
<td>Stops looking left.</td>
</tr>
<tr>
<td>-lookdown</td>
<td></td>
<td>Stops looking down.</td>
</tr>
<tr>
<td>-lookup</td>
<td></td>
<td>Stops looking up.</td>
</tr>
<tr>
<td>-movedown</td>
<td></td>
<td>Stops moving backwards.</td>
</tr>
<tr>
<td>-moveleft</td>
<td></td>
<td>Stops moving left.</td>
</tr>
<tr>
<td>-moveright</td>
<td></td>
<td>Stops moving right.</td>
</tr>
<tr>
<td>-moveup</td>
<td></td>
<td>Stops moving up; In water, lava, etc.</td>
</tr>
<tr>
<td>-quickmenu</td>
<td></td>
<td>Stops the quick menu, an easily accessible menu with basic commands such as Voice Says.</td>
</tr>
<tr>
<td>-right</td>
<td></td>
<td>Stops turning right.</td>
</tr>
<tr>
<td>-scores</td>
<td></td>
<td>Stops accessing the scoreboard.</td>
</tr>
<tr>
<td>-special</td>
<td></td>
<td></td>
</tr>
<tr>
<td>-speed</td>
<td></td>
<td>Stops changing your speed.
If run is enabled you will walk or vice versa when used. This serves no purpose as Warfork has no footstep sounds.</td>
</tr>
<tr>
<td>-strafe</td>
<td></td>
<td>Stops strafing, which When used +left and +right are changed with +moveleft and +moveright.</td>
</tr>
<tr>
<td>-use</td>
<td></td>
<td>Stops using an item.</td>
</tr>
<tr>
<td>-zoom</td>
<td></td>
<td>Stops zooming.</td>
</tr>
<tr>
<td>addbotroam</td>
<td></td>
<td></td>
</tr>
<tr>
<td>addcam</td>
<td>&lt;type name&gt;</td>
<td>Adds a camera to your democam path. Available camera types are: FirstPerson; ThirdPerson; Positional; Path_linear; Path_spline; orbital.</td>
</tr>
<tr>
<td>addip</td>
<td>&lt;ip address&gt;</td>
<td>Adds IP addresses to the filter list.</td>
</tr>
<tr>
<td>addnode</td>
<td></td>
<td></td>
</tr>
<tr>
<td>alias</td>
<td>&lt;alias name&gt; &lt;command&gt;</td>
<td>Creates an alias.</td>
</tr>
<tr>
<td>aliasa</td>
<td></td>
<td></td>
</tr>
<tr>
<td>aliaslist</td>
<td></td>
<td>Lists all aliases.</td>
</tr>
<tr>
<td>awards</td>
<td></td>
<td></td>
</tr>
<tr>
<td>bind</td>
<td>&lt;key&gt; &lt;command&gt;</td>
<td>Binds a key to a command.</td>
</tr>
<tr>
<td>bindlist</td>
<td></td>
<td>Lists all bound keys.</td>
</tr>
<tr>
<td>botdebug</td>
<td></td>
<td></td>
</tr>
<tr>
<td>botnotarget</td>
<td></td>
<td></td>
</tr>
<tr>
<td>callvote</td>
<td>&lt;vote&gt; [argument]</td>
<td>Calls a vote.</td>
</tr>
<tr>
<td>camswitch</td>
<td></td>
<td></td>
</tr>
<tr>
<td>centerview</td>
<td></td>
<td>Centers the players view.</td>
</tr>
<tr>
<td>chase</td>
<td></td>
<td></td>
</tr>
<tr>
<td>chasenext</td>
<td></td>
<td></td>
</tr>
<tr>
<td>chaseprev</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cinematic</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cinepause</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cinlist</td>
<td></td>
<td></td>
</tr>
<tr>
<td>clear</td>
<td></td>
<td>Clears the console.</td>
</tr>
<tr>
<td>clearcams</td>
<td></td>
<td>Clears all cameras in a camerapath.</td>
</tr>
<tr>
<td>cmd</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cmdlist</td>
<td></td>
<td>Lists all console commands.</td>
</tr>
<tr>
<td>coach</td>
<td></td>
<td>Allows you to be a coach in some team based gametypes.
Be on the team you wish to coach before typing the command in console.</td>
</tr>
<tr>
<td>cointoss</td>
<td>&lt;heads/tails&gt;</td>
<td>Flips a coin based on your choice and announces if you won or lost.</td>
</tr>
<tr>
<td>condump</td>
<td>&lt;filename&gt;</td>
<td>Dumps the console log to a file.</td>
</tr>
<tr>
<td>connect</td>
<td>&lt;ip address&gt;</td>
<td>Connects to a server.</td>
</tr>
<tr>
<td>cvarcheck</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cvarinfo</td>
<td></td>
<td></td>
</tr>
<tr>
<td>cvarlist</td>
<td></td>
<td>Lists all cvars.</td>
</tr>
<tr>
<td>deleteclosestnode</td>
<td></td>
<td></td>
</tr>
<tr>
<td>deletecam</td>
<td></td>
<td>Deletes the current camera; only works in demoEditMode</td>
</tr>
<tr>
<td>demo</td>
<td>&lt;filename&gt;</td>
<td>Loads a specific demo.</td>
</tr>
<tr>
<td>demoavi</td>
<td></td>
<td>Starts recording video as frames or audio as .wav file depending on cl_demoavi_audio and cl_demoavi_video. Framerate depends on cl_demoavi_fps.</td>
</tr>
<tr>
<td>demoEditMode</td>
<td></td>
<td>Lets you add and edit cameras for camera paths. Displays additional information on cameras (e.g.: timecode, current camera, next camera, type, position, roll, pitch, yaw ,fov).</td>
</tr>
<tr>
<td>demoFreeFly</td>
<td></td>
<td>Enables free flying camera regardless of set camera paths; entities like players may disappear on single POV demos when camera moves too far from the player.</td>
</tr>
<tr>
<td>demoget</td>
<td>&lt;ID&gt;</td>
<td>Use with demolist to download recorded demos from a server</td>
</tr>
<tr>
<td>demojump</td>
<td><time></td>
<td>Jumps to a specified time in a demo. Time format is [minutes:]seconds. Use + or - in front of the time to specify it in relation to current position in the demo.</td>
</tr>
<tr>
<td>demolist</td>
<td></td>
<td>Lists all demos on the Server and their ID. Can be downloaded via demoget &lt;ID&gt;</td>
</tr>
<tr>
<td>demopause</td>
<td></td>
<td>Pauses or resumes the currently playing demo.</td>
</tr>
<tr>
<td>devmap</td>
<td></td>
<td></td>
</tr>
<tr>
<td>disconnect</td>
<td></td>
<td>Disconnects from current server.</td>
</tr>
<tr>
<td>downloadcancel</td>
<td></td>
<td>Cancels an active download.</td>
</tr>
<tr>
<td>downloadstatus</td>
<td></td>
<td>Displays download status information.</td>
</tr>
<tr>
<td>driobide</td>
<td></td>
<td></td>
</tr>
<tr>
<td>dumpASapi</td>
<td></td>
<td></td>
</tr>
<tr>
<td>dumpuser</td>
<td></td>
<td></td>
</tr>
<tr>
<td>dynvarlist</td>
<td></td>
<td></td>
</tr>
<tr>
<td>echo</td>
<td>&lt;message&gt;</td>
<td>Prints a message to the console.</td>
</tr>
<tr>
<td>editcam</td>
<td>&lt;command&gt; &lt;variable&gt;</td>
<td>Edits the current camera, you can edit: type &lt;type name&gt; eg. path_spline; track &lt;entity number&gt; (tracks entity; 0 for no track); fov; timeOffset; origin; angles; pitch; yaw; roll.</td>
</tr>
<tr>
<td>editnodes</td>
<td></td>
<td></td>
</tr>
<tr>
<td>enterqueue</td>
<td></td>
<td></td>
</tr>
<tr>
<td>envshot</td>
<td></td>
<td></td>
</tr>
<tr>
<td>exec</td>
<td>&lt;filename&gt;</td>
<td>Executes a configuration file.</td>
</tr>
<tr>
<td>fontlist</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fs_checksum</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fs_mtime</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fs_pakfile</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fs_path</td>
<td></td>
<td></td>
</tr>
<tr>
<td>fs_search</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gamemap</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gamemenu</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gametype</td>
<td></td>
<td>Lists information about current game type.</td>
</tr>
<tr>
<td>getinfo</td>
<td></td>
<td></td>
</tr>
<tr>
<td>getstatus</td>
<td></td>
<td></td>
</tr>
<tr>
<td>gfxinfo</td>
<td></td>
<td></td>
</tr>
<tr>
<td>give</td>
<td>&lt;all/health/weapons/ammo/armor&gt;</td>
<td>Give items to a Player. Requires cheats to be enabled.</td>
</tr>
<tr>
<td>glslprogramlist</td>
<td></td>
<td></td>
</tr>
<tr>
<td>god</td>
<td></td>
<td>Toggles godmode.</td>
</tr>
<tr>
<td>heartbeat</td>
<td></td>
<td>Sends a manual heartbeat to the masterservers.
This makes your server visible to those that query the list of servers.</td>
</tr>
<tr>
<td>help_hud</td>
<td></td>
<td>Prints a list of HUD scripts commands, HUD scripts operators, HUD scripts CONSTANT names, and HUD scripts REFERENCE names to your console.</td>
</tr>
<tr>
<td>imagelist</td>
<td></td>
<td>Shows a list of all images loaded in your console.</td>
</tr>
<tr>
<td>importcams</td>
<td>&lt;filename&gt;</td>
<td>imports a .cam file. Filepath is relative to the demos directory. The cameras imported are merged with the previously existing, if any.</td>
</tr>
<tr>
<td>invite</td>
<td></td>
<td></td>
</tr>
<tr>
<td>irc_connect</td>
<td></td>
<td></td>
</tr>
<tr>
<td>irc_disconnect</td>
<td></td>
<td></td>
</tr>
<tr>
<td>join</td>
<td>[team name]</td>
<td>Joins the game. Joins a specific team if specified.</td>
</tr>
<tr>
<td>kick</td>
<td>&lt;player&gt;</td>
<td>Kicks a player from the server.</td>
</tr>
<tr>
<td>kill</td>
<td></td>
<td>Kills the player.</td>
</tr>
<tr>
<td>killserver</td>
<td></td>
<td>Kills the server process.</td>
</tr>
<tr>
<td>leavequeue</td>
<td></td>
<td>Leaves the challengers queue.</td>
</tr>
<tr>
<td>listip</td>
<td></td>
<td>The current list of filters will be printed to console.</td>
</tr>
<tr>
<td>listlocations</td>
<td></td>
<td>Prints a list of all map locations (if available) to console.</td>
</tr>
<tr>
<td>listraces</td>
<td></td>
<td></td>
</tr>
<tr>
<td>listratings</td>
<td></td>
<td></td>
</tr>
<tr>
<td>lockteam</td>
<td></td>
<td>Locks the teams.</td>
</tr>
<tr>
<td>makenodes</td>
<td></td>
<td></td>
</tr>
<tr>
<td>map</td>
<td>&lt;map name&gt;</td>
<td>Switches a map.</td>
</tr>
<tr>
<td>maplist</td>
<td></td>
<td>Lists all maps available.</td>
</tr>
<tr>
<td>match</td>
<td>&lt;restart\advance\status&gt;</td>
<td>Restarts, Advances, or gets the Status of your match.</td>
</tr>
<tr>
<td>memlist</td>
<td></td>
<td>Prints a memory pool list to your console.</td>
</tr>
<tr>
<td>memstats</td>
<td></td>
<td>Prints memory statistics to your console.</td>
</tr>
<tr>
<td>menu_close</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_force</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_modal</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_open</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_quick</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_tvchannel_add</td>
<td></td>
<td></td>
</tr>
<tr>
<td>menu_tvchannel_remove</td>
<td></td>
<td></td>
</tr>
<tr>
<td>messagemode</td>
<td></td>
<td>Prompts you to write a message, which will be sent to everyone on the server.</td>
</tr>
<tr>
<td>messagemode2</td>
<td></td>
<td>Prompts you to write a message, which will be sent to everyone on your team.</td>
</tr>
<tr>
<td>mm_login</td>
<td></td>
<td>Logs you out of matchmaking.</td>
</tr>
<tr>
<td>mm_logout</td>
<td></td>
<td>Logs you in Matchmaking.</td>
</tr>
<tr>
<td>modellist</td>
<td></td>
<td>Prints a list of all models loaded in your console.</td>
</tr>
<tr>
<td>music</td>
<td></td>
<td></td>
</tr>
<tr>
<td>next</td>
<td></td>
<td></td>
</tr>
<tr>
<td>nextmusic</td>
<td></td>
<td></td>
</tr>
<tr>
<td>noclip</td>
<td></td>
<td>Toggles noclip.</td>
</tr>
<tr>
<td>notready</td>
<td></td>
<td>Changes status to "Not ready".</td>
</tr>
<tr>
<td>op</td>
<td>&lt;password&gt;</td>
<td>Makes the player a game operator.</td>
</tr>
<tr>
<td>opcall</td>
<td>&lt;vote&gt; [argument]</td>
<td>Calls an <a href="Calling_Votes#Opcalls" class="wikilink" title="instant-passing">instant-passing</a> vote.</td>
</tr>
<tr>
<td>operator</td>
<td>&lt;password&gt;</td>
<td>Makes the player a game operator.</td>
</tr>
<tr>
<td>pausemusic</td>
<td></td>
<td></td>
</tr>
<tr>
<td>pingserver</td>
<td></td>
<td></td>
</tr>
<tr>
<td>players</td>
<td></td>
<td>Lists all players in-game.</td>
</tr>
<tr>
<td>position</td>
<td></td>
<td>Displays player's current position.</td>
</tr>
<tr>
<td>prevmusic</td>
<td></td>
<td></td>
</tr>
<tr>
<td>purelist</td>
<td></td>
<td>Displays a list of all Pure Files in your console.</td>
</tr>
<tr>
<td>putaway</td>
<td></td>
<td>Closes the scoreboard if open.</td>
</tr>
<tr>
<td>quit</td>
<td></td>
<td>Quits the game / server.</td>
</tr>
<tr>
<td>racerestart</td>
<td></td>
<td>Restarts the race.</td>
</tr>
<tr>
<td>rcon</td>
<td>&lt;command&gt;</td>
<td>Executes a server command as console.</td>
</tr>
<tr>
<td>ready</td>
<td></td>
<td>Makes the player ready.</td>
</tr>
<tr>
<td>reconnect</td>
<td></td>
<td>Reconnects the player to the current server.</td>
</tr>
<tr>
<td>record</td>
<td>&lt;name&gt;</td>
<td>Records a demo with the specified name(These are single POV demos, for multiPOV use serverrecord).</td>
</tr>
<tr>
<td>removeip</td>
<td>&lt;ip address&gt;</td>
<td>Removes IP addresses from the filter list.</td>
</tr>
<tr>
<td>requestservers</td>
<td></td>
<td></td>
</tr>
<tr>
<td>reset</td>
<td></td>
<td></td>
</tr>
<tr>
<td>s_devices</td>
<td></td>
<td>List of available OpenAL sound devices.</td>
</tr>
<tr>
<td>s_restart</td>
<td></td>
<td>Restarts the sound engine.</td>
</tr>
<tr>
<td>savenodes</td>
<td></td>
<td></td>
</tr>
<tr>
<td>saverecam</td>
<td>&lt;optional name&gt;</td>
<td>Saves the .cam script file with the camera path data. If no name is provided, the demo name is used.</td>
</tr>
<tr>
<td>say</td>
<td>&lt;message&gt;</td>
<td>Sends a global message.</td>
</tr>
<tr>
<td>say_team</td>
<td>&lt;message&gt;</td>
<td>Sends a team message.</td>
</tr>
<tr>
<td>score</td>
<td></td>
<td>Toggles the scoreboard.</td>
</tr>
<tr>
<td>screenshot</td>
<td></td>
<td>Takes a screenshot of what you're looking at.</td>
</tr>
<tr>
<td>serverinfo</td>
<td></td>
<td>Displays Server info settings in console.
Values displayed: version, fs_game, g_antilag, g_gametype, g_instagib, protocol, sv_cheats, sv_hostname, sv_http, sv_maxclients, sv_maxmvclients, sv_mm_enable, sv_mm_loginonly, sv_pps, sv_pure, sv_skilllevel, sv_skillRating.</td>
</tr>
<tr>
<td>serverrecord</td>
<td>&lt;name&gt;</td>
<td>Records a multiPOV demo on the Server (can be downloaded by clients via demolist and demoget).</td>
</tr>
<tr>
<td>serverrecordcancel</td>
<td></td>
<td></td>
</tr>
<tr>
<td>serverrecordpurge</td>
<td></td>
<td></td>
</tr>
<tr>
<td>serverrecordstop</td>
<td></td>
<td></td>
</tr>
<tr>
<td>set</td>
<td>&lt;cvar&gt; &lt;value&gt;</td>
<td>Changes the value of x cvar to y.</td>
</tr>
<tr>
<td>seta</td>
<td></td>
<td></td>
</tr>
<tr>
<td>setas</td>
<td></td>
<td></td>
</tr>
<tr>
<td>setau</td>
<td></td>
<td></td>
</tr>
<tr>
<td>setdyn</td>
<td></td>
<td></td>
</tr>
<tr>
<td>sets</td>
<td></td>
<td></td>
</tr>
<tr>
<td>setu</td>
<td></td>
<td></td>
</tr>
<tr>
<td>shaderdump</td>
<td></td>
<td></td>
</tr>
<tr>
<td>shaderlist</td>
<td></td>
<td>Prints a list of shaders currently loaded in your console.</td>
</tr>
<tr>
<td>showclosestnode</td>
<td></td>
<td></td>
</tr>
<tr>
<td>showip</td>
<td></td>
<td>Shows your local IP Address (reversed).</td>
</tr>
<tr>
<td>showserverip</td>
<td></td>
<td>Shows the server IP Address.</td>
</tr>
<tr>
<td>sizedown</td>
<td></td>
<td>Decreases the viewable area (affects cg_viewSize by -10) on your screen.</td>
</tr>
<tr>
<td>sizeup</td>
<td></td>
<td>Increases the viewable area (affects cg_viewSize by +10) on your screen.</td>
</tr>
<tr>
<td>soundlist</td>
<td></td>
<td>Prints a list of all sounds currently loaded in your console.</td>
</tr>
<tr>
<td>spec</td>
<td></td>
<td>Joins the SPECTATOR team.</td>
</tr>
<tr>
<td>spectators</td>
<td></td>
<td>Prints a list of spectators.</td>
</tr>
<tr>
<td>stats</td>
<td>&lt;id\playername&gt;</td>
<td>Prints your or a specified players stats.
Stats include hit/shot percent, damage given/received, ratio, health/armor, etc.</td>
</tr>
<tr>
<td>status</td>
<td></td>
<td>Displays the server status in console.
Map, Player ID, Score, Ping, Player Names, Last Message, Address, Port, Rate, etc.</td>
</tr>
<tr>
<td>stop</td>
<td></td>
<td>Stops your demo if it's currently recording.</td>
</tr>
<tr>
<td>stopmusic</td>
<td></td>
<td>Stops music that's currently playing.</td>
</tr>
<tr>
<td>svscore</td>
<td>&lt;0/1&gt;</td>
<td>If enabled, the scoreboard will be toggled.</td>
</tr>
<tr>
<td>timein</td>
<td></td>
<td>Resumes the match instantly.</td>
</tr>
<tr>
<td>timeout</td>
<td></td>
<td>Pauses the match for 180 seconds.</td>
</tr>
<tr>
<td>toggle</td>
<td>&lt;cvar&gt; &lt;argument 1&gt; [argument n]</td>
<td>Toggles a cvar's value between the arguments.</td>
</tr>
<tr>
<td>toggleconsole</td>
<td></td>
<td>Toggles the console.</td>
</tr>
<tr>
<td>toggleready</td>
<td></td>
<td>Toggles "ready" status.</td>
</tr>
<tr>
<td>tvconnect</td>
<td></td>
<td>Sends a command to connect to a TV server (with available slots) that has round robin balancing.</td>
</tr>
<tr>
<td>ui_dumpapi</td>
<td></td>
<td>Dumps API information to console.</td>
</tr>
<tr>
<td>ui_printdocs</td>
<td></td>
<td>Prints document cache to console.</td>
</tr>
<tr>
<td>ui_reload</td>
<td></td>
<td>Reloads the user interface.</td>
</tr>
<tr>
<td>unalias</td>
<td>&lt;name&gt;</td>
<td>Removes an alias.</td>
</tr>
<tr>
<td>unaliasall</td>
<td></td>
<td>Removes all aliases&gt;</td>
</tr>
<tr>
<td>unbind</td>
<td>&lt;key&gt;</td>
<td>Unbinds a key.</td>
</tr>
<tr>
<td>unbindall</td>
<td></td>
<td>Unbinds all keys.</td>
</tr>
<tr>
<td>unlockteam</td>
<td></td>
<td>Unlocks the teams.</td>
</tr>
<tr>
<td>unready</td>
<td></td>
<td>Makes the player unready.</td>
</tr>
<tr>
<td>upstate</td>
<td></td>
<td>Updates your client on the current state of things.</td>
</tr>
<tr>
<td>use</td>
<td></td>
<td>Uses an object in the world.</td>
</tr>
<tr>
<td>userinfo</td>
<td></td>
<td>Prints a list of User Info Settings to your console.
Examples: cg_movementStyle, cg_noAutohop, cl_mm_session, clan, color, hand, handicap, model, name, password, and skin.</td>
</tr>
<tr>
<td>vid_modelist</td>
<td></td>
<td>List of available video modes.</td>
</tr>
<tr>
<td>vid_restart</td>
<td></td>
<td>Restarts the video engine.</td>
</tr>
<tr>
<td>viewpos</td>
<td></td>
<td></td>
</tr>
<tr>
<td>vote</td>
<td>&lt;yes / no&gt;</td>
<td>Casts a vote.</td>
</tr>
<tr>
<td>vsay</td>
<td>&lt;name&gt;</td>
<td>Says a voice message globally. Shows list of all voice messages if executed without the argument.</td>
</tr>
<tr>
<td>vsay_team</td>
<td>&lt;name&gt;</td>
<td>Says a voice message to the team.</td>
</tr>
<tr>
<td>vstr</td>
<td>&lt;variable.</td>
<td>Execute a variable command.
Example: vstr nextmap</td>
</tr>
<tr>
<td>wait</td>
<td></td>
<td>Delays the execution of a remaining command buffer until the next frame.
Example: bind z "+attack ; wait ; kill"</td>
</tr>
<tr>
<td>weapcross</td>
<td>&lt;0-4&gt;</td>
<td>Shows weapon sets near your crosshair, which can be toggled between.
0 - View Only, 1 - Gunblade/Machine Gun, 2 - Riot Gun/Grenade Launcher, 3 - Rocket Launcher/Plasmagun, 4 - Lasergun/Electrobolt
Example: bind "p" weapcross 1</td>
</tr>
<tr>
<td>weaplast</td>
<td></td>
<td>Switches to last weapon.</td>
</tr>
<tr>
<td>weapnext</td>
<td></td>
<td>Switches to next weapon.</td>
</tr>
<tr>
<td>weapprev</td>
<td></td>
<td>Switches to previous weapon.</td>
</tr>
<tr>
<td>whois</td>
<td>&lt;player&gt;</td>
<td>Provides player information if they're logged into Matchmaking.</td>
</tr>
<tr>
<td>writeconfig</td>
<td>&lt;name&gt;</td>
<td>Writes the current configuration to a file.</td>
</tr>
<tr>
<td>writeip</td>
<td></td>
<td>Writes addip\removeip &lt;ip&gt; commands to listip.cfg for future execution. By default filter lists are not saved\restored.</td>
</tr>
</tbody>
</table>
