# XCX Co-op Split-Screen (public alpha)

Two-player local split-screen co-op for *Xenoblade Chronicles X: Definitive Edition* on PC, as a mod for
[XCX Recomp](https://github.com/jmars125/xcx-recomp).

Two players on one PC and one screen: the host on the top half, the guest on the bottom half, each with its own
controller, its own character and its own save, in the same open world.

> **Alpha.** It works and has been played from new games onward, but it has known glitches (listed below) and has
> only been tested on a small number of setups. Please report what you find.

## What this is, and what it is not

- This repository and its download contain **the mod only**: its source code and install scripts.
- It contains **no game code and no game data**. The co-op program is built **on your own PC, from your own game
  files**, during installation, with the tools your XCX Recomp setup already has.
- You need your own working installation of XCX Recomp, made from your own copy of the game.
- This is an unofficial fan project. It is not affiliated with or endorsed by Nintendo, Monolith Soft or the
  XCX Recomp project.

## Requirements

| | |
|---|---|
| Game | **XCX Recomp 0.1.21** ([release v0.1.21](https://github.com/jmars125/xcx-recomp/releases/tag/v0.1.21)) with **game update 2.0.0**, installed and working. Other versions are refused by the installer. |
| Folders | The game folder (with `xcx.exe`, `exefs`, `romfs`) and the setup folder that built it (with `python`, `llvm`, `bin`, `runtime`). |
| Controllers | Two Xbox-compatible controllers. Controller 1 is the host, controller 2 the guest. |
| System | Windows 10 or 11. About 3 GB of free disk space during installation, about 500 MB afterwards. |

## Download

Get **`XCX-Coop-Split-Screen-0.1.2-alpha.zip`** from the [Releases page](../../releases).

## Install

1. Unpack the zip anywhere.
2. Run **`Install Co-op Mod.cmd`**.
3. Choose your game folder. If the setup folder is not found by itself, choose it too.
4. Wait while the co-op program is built (a few minutes, once per version; nothing needs to be pressed).
5. Choose how the two players start:
   - **Yes** – each player starts from a copy of an existing save (pick one for the host and one for the guest, or
     the same for both). The saves you pick are only read.
   - **No** – both players start a new game.

Nothing in your game folder is changed. A folder `coop` and three shortcuts are added. Installing again keeps both
co-op saves.

## Play

1. Connect both controllers and start **`Play Co-op Split-Screen.cmd`** in the game folder.
2. Two games open and fill the top and bottom halves of your main display. Each is an ordinary single-player game
   at first: load the save, or start a new game, on each.
3. When both players stand in the world, the small window **XCX Co-op** enables **Begin Split-Screen Co-op**.
   Click it. The guest then joins the host: it travels to the host and takes a seat in the host's party.
4. Close both game windows to stop.

Each controller drives its own player whichever window has the focus.

## How it works

- **The host owns the world:** enemies, time and weather, and the party. Up to two of the host's AI companions are
  shared with the guest. The guest takes the fourth party slot when it is free, so the host's companions keep their
  places; with a full host party the guest takes the second slot and the host keeps two companions.
- **The host can change companions** in Active Members while connected.
- **Each player keeps its own progress:** character, equipment, Skell, inventory, missions and story, in its own
  save. Each player triggers, watches or skips its own cutscenes. The host leads the story: an encounter the guest
  triggers first appears when the host's scene has ended.
- **Fights are shared**, on foot and in Skells. A player joins a fight by attacking; rewards follow the game's own
  online rule (who took part gets them).
- **The guest follows the host's fast travel.**
- **Defeat:** when the host is defeated and not helped up, both players restart at the host's restart point. A
  defeated guest waits to be helped up while the host lives.

## Saves

- **`Open Co-op Saves.cmd`** opens `coop\saves` with one folder per player (`host`, `guest`). Each player saves
  with the game's own Save menu and autosave into its own folder.
- Back up by copying these folders. To start one player over, delete its folder and run the installer again.
- The single-player save of the game (`profile`) is never written by the co-op.

## Known limitations

- A Skell that has been flying for a while when the other screen builds its copy may be shown on the ground until
  it changes its flight.
- The host's AI companions fighting on foot were not examined in this version.
- Very rarely a game closes with an error two or three seconds after it starts; start it again.
- Join while both players are out of combat.
- In the host's Active Members screen, do not remove the guest's row and do not make it the controlled character.
- Removing a companion without putting another in its place is not shown to the guest.
- Two players on one PC only. Three or four players and online play are not part of this release.
- This is an alpha: a game can close with an error.

## Reporting a problem

Open an [issue](../../issues) and say what both players were doing. Attach the two newest files ending in
`-host.log` and `-guest.log` from `coop\logs` in your game folder (and `install-build.log` if the installation
failed).

## Uninstall

Run **`Uninstall Co-op Mod.cmd`** in the game folder. It asks whether the two co-op saves should be deleted too.
The game, its own save and its settings are not touched.

## Credits and licence

- Built on [XCX Recomp](https://github.com/jmars125/xcx-recomp) by jmars125 and its contributors. The mod's source
  is a modified copy of that project's source, under the same MIT licence ([LICENSE](LICENSE)); third-party
  components are listed in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md).
- The co-op mod reuses the game's own original multiplayer code inside the single-player world and adds only what
  that code needs to run between two copies of the game on one PC.
- The program built on your machine contains the game and is for your personal use: **do not share it.**
- *Xenoblade Chronicles X* is the property of Nintendo and Monolith Soft.
