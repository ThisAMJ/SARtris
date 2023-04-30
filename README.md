
# SARtris Classic

Run in your browser! **[DEMO](https://thisamj.github.io/sourcerun?example=sartris%20classic)** (switch left menu to SAR Hud)

(tl;dr - I made Tetris for NES in Portal 2)

Since its creation, the [SAR](https://sar.portal2.sr) speedrunning plugin has been able to
do much more than simply speedrun. In June of last year, this was
taken to the extreme with the advent of Config+, an esoteric
programming language that runs entirely within the config
files of Portal 2.

Config+ was intended to improve the automation that
speedrunners used during their sessions, and has effectively done
so in the community-driven [srconfigs](https://s.portal2.sr/srconfigs) project. At the same time,
it has been used in... less productive ways.

This repository signifies the current state of 'Config++' exploration.
I have recreated the popular game 'Tetris' for the NES entirely within
a config file that is normally used to change how your crosshair looks,
and I think that's pretty cool.

[Fellow community member RainbowwPhoenixx has made a version of SARtris
for 'modern' Tetris.](https://github.com/RainbowwPhoenixx/SARtris)
Keep in mind that it was made quite a while ago, and therefore doesn't
have the best performance.

I've also made Minesweeper in a similar way, which can be downloaded from [here](https://cdn.discordapp.com/attachments/730456805808799775/1068106578139549797/minesweeper.cfg).

## Installation

1. Download the source code for the repository.
2. Extract the `tetris` folder and place it in `.../steamapps/common/Portal 2/portal2/cfg`.
   You can also put it in your [common folder](https://www.youtube.com/watch?v=FmJ1OcKc7Ag), and
   it will work similarly in mods such as [Speedrun Mod](https://github.com/p2sr/Portal2SpeedrunMod/releases),
   Portal Stories: Mel, and Portal Reloaded.
3. Open `autoexec.cfg` (or `extra.cfg` if you have srconfigs)
   and write `exec tetris/tetris` on a new line.

## Usage

You can bind these actions to keys using `bind <key> <action>`.

|        Action           | Description
| ----------------------- | -----------
| `sartris_toggle`        | Toggles SARtris on/off.
| `sartris_newgame`       | Resets SARtris to a new game. You can optionally specify<br/>a number with which to seed the RNG for the next game.
| `sartris_get_seed`      | Get the RNG seed of the current game.
| `sartris_get_prev_seed` | Get the RNG seed of the previous game. Useful if you died<br/>
before you could get the seed.
| `+sartris_left`         | Move your tetromino left.
| `+sartris_right`        | Move your tetromino right.
| `+sartris_drop`         | Move your tetromino down.
| `+sartris_rotate_cw`    | Rotate your tetromino clockwise.
| `+sartris_rotate_ccw`   | Rotate your tetromino counter-clockwise.

You can customise the behaviour of SARtris Classic by changing
certain 'svars' using `svar_set <name> <value>`.

|         Name         | Default | Description
| -------------------- | :-----: | -----------
| `sartris_hud_offset` | `1000`  | Offset for the SAR HUD text element at which to draw the game.
| `sartris_region`     | `NTSC`  | Select ROM region. `NTSC` or `PAL`.
| `sartris_draw_next`  |   `1`   | Whether to draw the 'NEXT' piece.
| `sartris_nes_color`  |   `0`   | Whether to use the NES palette for colors.
