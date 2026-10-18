# HelloPortal (Portal Neighbor)

**The Portal gun in Hello Neighbor.** Shoot blue and orange portals, see through them, walk, fall and fling through
them, throw things through them, and watch the Neighbor chase you through them. GLaDOS comments on everything you
do, and she replaces the final boss.

<!-- screenshot here -->

> Unofficial fan project, not affiliated with Valve, tinyBuild or Dynamic Pixels. The download contains **no Portal
> files**: the installer takes the gun, GLaDOS and the sounds from **your own copy of Portal**.

## Features

- **Portals**: left mouse fires blue, right mouse fires orange. They stick to walls, floors and ceilings, and you see
  the other side through them.
- **Walk, fall and fling through them.** Your speed carries through, so jump into a floor portal from high up and fly
  out of the other one.
- **Thrown items** go through portals too.
- **The Neighbor uses them.** He follows you through, and if he sees you through a portal, he takes the shortcut.
- **GLaDOS** talks to you about your test: picking up the gun, your first portal, your first fling, getting caught,
  the Neighbor's "impossible" test...
- **GLaDOS as the final boss**: she hangs in place of the Thing in the finale.
- The real **portal gun** in your hand, with Portal's own shot, portal and fizzle sounds.

## Requirements

- **Hello Neighbor** (full game) on Steam, on Windows
- **Portal** (the 2007 game) on Steam. It can be in any Steam library; it only has to be installed.

## Install

1. Download `PortalNeighbor-1.0.0.zip` from [Releases](../../releases) and unzip it anywhere.
2. Close Hello Neighbor, then double-click **`Install.bat`**. It finds both games through Steam, builds the Portal
   content from your Portal files, and installs the mod (with [UE4SS](https://github.com/UE4SS-RE/RE-UE4SS)) into
   Hello Neighbor. This takes a few seconds.
   - Windows may warn about running a script from the internet. Choose "More info", then "Run anyway".
3. Start Hello Neighbor from Steam as usual and load a level. The portal gun lies in front of you: pick it up with **E**.

## Controls

| Key | With the gun in your hand |
|---|---|
| Left mouse | blue portal |
| Right mouse | orange portal |
| X | throw / put down the gun |
| F6 | close both portals |
| F7 | bring the gun back to you |
| F8 | the mod on / off |

## Uninstall

Double-click **`Uninstall.bat`**. It removes everything the installer added to Hello Neighbor. That includes UE4SS if
the installer put it there. A UE4SS you had before stays, and any file the installer replaced is put back. Portal
itself is never changed.

## What it changes

Only Hello Neighbor's folder:
- UE4SS: `dwmapi.dll` and the `ue4ss` folder in `HelloNeighbor\Binaries\Win64`
- the mod's two UE4SS mods (`Portal`, `PortalNative`)
- two content paks in `HelloNeighbor\Content\Paks\Portal`

Replaced files are kept as `*.before-portalneighbor`, and `installed.txt` lists everything that was added.

## Troubleshooting

- **"These Portal files are not the version this mod was made with"**: in Steam, open Portal > Properties >
  Installed Files > Verify integrity, then run `Install.bat` again.
- **Antivirus / SmartScreen warnings**: UE4SS loads as a `dwmapi.dll` next to the game. The installer also compiles
  its small Portal-file reader (`scripts\PortalRefill.cs`, plain C# you can read) with Windows' own .NET. Check that
  your download matches the SHA-256 on the release page (PowerShell: `Get-FileHash PortalNeighbor-1.0.0.zip`).
- **Bug reports**: please attach these logs from `<Hello Neighbor>\HelloNeighbor\Binaries\Win64`: `portal_lua.log`,
  `ue4ss\UE4SS.log` and `ue4ss\Mods\PortalNative\dlls\portal_native.log`.

Single-player only.

## Credits

- **Portal**, GLaDOS and Aperture Science: Valve. Their content is read from your own copy of Portal.
- **Hello Neighbor**: tinyBuild / Dynamic Pixels.
- **[UE4SS](https://github.com/UE4SS-RE/RE-UE4SS)** (MIT): the scripting system the mod runs on.
- Made with the help of AI coding tools.

Licence: MIT (see `LICENSE`). The game content it reads stays Valve's and tinyBuild's.
