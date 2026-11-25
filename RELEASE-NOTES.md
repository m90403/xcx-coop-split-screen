Xenoblade Chronicles X: Definitive Edition - two-player split-screen co-op
Release notes

0.1.0-alpha (public alpha 1)
----------------------------
For XCX Recomp 0.1.21 with game update 2.0.0. Gameplay baseline: development build V387.

What is in it
- Two players on one PC: host on the top half, guest on the bottom half of the main display, borderless and full
  width, sized from the detected display.
- One controller per player, independent of which window has the focus.
- One persistent save per player, separate from the single-player save.
- Start two new games together or continue from existing saves (also two different saves).
- Both games start single-player; "Begin Split-Screen Co-op" connects them when both players are in the world.
- The guest travels to the host by itself at the start and takes the fourth party slot when it is free.
- The host's party decides: up to two of the host's AI companions are shared with the guest, with their Arts,
  equipment and Skells; the host can change them in Active Members while connected.
- Shared enemies and fights on foot and in Skells; each player gets its own rewards by the game's own online rule.
- Each player's own missions, story progress, cutscenes and saves; the host leads shared story encounters.
- The guest follows the host's fast travel; time and weather come from the host.
- When the host is defeated and not helped up, both players restart together at the host's restart point.
- Installation builds the co-op program on your machine from your own game files; the package contains no game
  code or data. Reinstalling keeps the saves. An uninstaller is included.

Known limitations
- The guest can see a host companion running in place, or a companion's Skell kneeling or sliding, most often
  after the host changed companions; a fast travel corrects it.
- Join out of combat.
- The guest's row in the host's Active Members screen must be left alone.
- A companion removed without a replacement stays visible to the guest.
- Two players on one PC only. Three or four players and online play are not part of this release.
- Tested on one machine (Windows 11, 2560x1600 display, two Xbox controllers).

Reporting a problem
- Say what both players were doing, and attach the two newest files ending in -host.log and -guest.log from
  coop\logs in your game folder (and install-build.log if the installation failed).
