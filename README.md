![Momentum Mod](https://i.imgur.com/iR7p55N.png)

> Momentum Mod is a free, standalone game built on the Source Engine centralizing the major movement gametypes found in games like Counter-Strike, Half-Life, Team Fortress, and Titanfall.

## What is this?

This is a WIP fork of momentum mod where KZ players can test different game mechanics and will hopefully help decide what will eventually be in the real Climb gamemode in Momentum Mod!

## How do I install this???

1. Download and install the 0.8.7 public build of Momentum Mod from here: https://github.com/momentum-mod/game/releases/tag/0.8.7-public-eval
2. Download the latest release of Momentum-KZ from here: https://github.com/GameChaos/momentum-kz/releases
3. Extract the Momentum-KZ .zip file into the root of your 0.8.7 installation folder (same folder where hl2.exe is).
4. Extract the Momentum-KZ-Maps folder into the maps/ folder.

If you want to fiddle with some commands like sv_airaccelerate, then add `-mapping` as a launch option to run_momentum.bat.

## Other Info

Maps that are included in Momentum-KZ-Maps-XXXX-XX-XX.zip:
- kz_100_metres - Similar to `100m` in Quake 1. Bhop in a straight line to get the best time.
- kz_bkz_goldbhop_bad_port - A quick and dirty port of bkz_goldbhop for gameplay testing.
- kz_checkmate_bad_port - A quick and dirty port of kz_checkmate for gameplay testing.
- kz_xc_nature - CSS map made by chichin: https://gamebanana.com/mods/123762

## Useful commands for players that are used to KZ.

- `mom_hud_menu_show savelocmenu` - A teleport menu similar to KZTimer's and GOKZ's, except you can set a checkpoint anywhere and it preserves your speed.

## KZ Commands that change KZ game mechanics:

### On-off commands:

| Command Name                      | Default Value | Min and Max Value | Description                                                                                                                                                                                                      |
|-----------------------------------|---------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sv_edge_friction                  | 1             | -                 | How much the player gets slowed down close to edges that are high. 1 = no effect, 2 = default CS 1.6 behaviour. This scales sv_friction when you're close to an edge.                                            |
| sv_kz_double_duck                 | 1             | 0 or 1            | Toggle double duck.                                                                                                                                                                                              |
| sv_kz_stamina_type                | 1             | 0 to 2            | Type of stamina. 0 = none, 1 = Mild version of CSGO's stamina, 2 = CSS/1.6 stamina                                                                                                                               |
| sv_kz_bhop_cap_type               | 1             | 0 or 1            | 0 = SimpleKZ, 1 = Forces you to not strafe a lot if you want to go as fast as possible. if landspeed >= sv_kz_bhop_cap_1_min, then newspeed = sv_kz_bhop_cap_1_max - (landspeed - sv_kz_bhop_cap_1_min)          |

### Advanced commands:

| Command Name                      | Default Value | Min and Max Value | Description                                                                                                                                                                                                      |
|-----------------------------------|---------------|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| sv_edge_friction_height           | 66            | -                 | How far from the ground an edge has to be for the player to be affected by edge friction.                                                                                                                        |
| sv_edge_friction_distance         | 16            | -                 | How close you have to be to an edge to get affected by edge friction.                                                                                                                                            |
|                                   |               |                  |                                                                                                                                                                                                                   |
| sv_kz_stamina_1_recovery_rate     | 0.4           | -                 | sv_kz_stamina_type 1: How many seconds it takes for stamina to be recovered.                                                                                                                                     |
| sv_kz_stamina_1_multiplier_height | 0.14          | -                 | sv_kz_stamina_type 1: How much height to remove with maximum stamina.                                                                                                                                            |
| sv_kz_stamina_1_multiplier_speed  | 0.06          | -                 | sv_kz_stamina_type 1: How much speed to remove per tick.                                                                                                                                                         |
| sv_kz_stamina_1_zspeed_amount     | 100.0         | -                 | sv_kz_stamina_type 1: At what z-speed do you get no stamina anymore relative to negative jump factor (jump factor is the vertical speed you get when you jump). Default jump factor is 301.993377.               |
| sv_kz_stamina_2_cost_jump         | 25.0          | -                 | sv_kz_stamina_type 2: How much stamina gets added when you jump.                                                                                                                                                 |
| sv_kz_stamina_2_recovery_rate     | 19.0          | -                 | sv_kz_stamina_type 2: How fast stamina recovers.                                                                                                                                                                 |
|                                   |               |                  |                                                                                                                                                                                                                   |
| sv_kz_double_duck_height          | 24.0          | -                 | The height you get from a double duck. If you hold duck in the air as well you can doubleduck onto 33 unit blocks                                                                                                |
|                                   |               |                  |                                                                                                                                                                                                                   |
| sv_kz_bhop_cap_0_multiplier       | 0.2           | -                 | if landspeed > sv_kz_bhop_cap_0_base, then newspeed = sv_kz_bhop_cap_0_base  + (landspeed - 250) * sv_kz_bhop_cap_0_multiplier.                                                                                  |
| sv_kz_bhop_cap_0_base             | 250           | -                 | -                                                                                                                                                                                                                |
| sv_kz_bhop_grace_ticks            | 4             | -                 | How many ticks after landing should the player be able to have the same bhop prespeed no matter what tick they jump on. To avoid confusion: if this is 3 here, then it's equivalent to 2 tick perfs in SimpleKZ. |
