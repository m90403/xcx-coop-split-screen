Xenoblade Chronicles X: Definitive Edition - two-player split-screen co-op
Release notes

0.1.2-alpha (public alpha 3)
----------------------------
For XCX Recomp 0.1.21 with game update 2.0.0. Gameplay baseline: development build V459.
An update for joining anywhere in the world and for how the host's AI companions and Skells look on the guest's
screen. Installing it over 0.1.0-alpha or 0.1.1-alpha builds the co-op program again and keeps both players' saves.

Fixed and confirmed in play (two players on one PC)
- Starting co-op while the host stands in the open world: the guest saw no enemies until the first fast travel.
  The enemies around the host are now shared from the start.
- Starting co-op while the host sits in its Skell: the guest was sent to the place where the host had boarded,
  which can be far away. The guest now arrives at the host.
- The guest could not unlock an FN Site (the hold-A gauge stayed at 0 %). Each player now plants probes in its own
  save.
- A Skell that took off right after a fast travel was shown walking in the air on the other screen. It now flies.
- After a fast travel the other player could be shown standing beside its own Skell while riding it. The pilot is
  now put aboard (this can take about two seconds after arriving).
- A companion of the host that fell and was put back on its feet by the game stayed in the falling pose on the
  guest's screen (seen in a new game, after the first scene outside). It now lands.

Included and checked by automated sessions; in play nothing was reported against them
- The Skells of the host's AI companions on the guest's screen: take-off and flight, drawing weapons, attacks,
  Arts and putting the weapons away. Before, a companion's Skell could stay in one pose for a whole fight.

Known limitations
- A Skell whose copy is built on the other screen while it has already been flying for a while may be shown on the
  ground until it changes its flight; a take-off right after arriving is handled.
- The host's AI companions fighting on foot were not examined in this update.
- Very rarely a game closes with an error two or three seconds after it starts, before the title screen. This is
  not caused by the co-op; start again.
- A destroyed Skell stays gone until it is repaired at the Barracks, as in the single-player game.
- Join out of combat.
- The guest's row in the host's Active Members screen must be left alone.
- A companion removed without a replacement stays visible to the guest.
- Two players on one PC only. Three or four players and online play are not part of this release.
- Tested on one machine (Windows 11, 2560x1600 display, two Xbox controllers).

0.1.1-alpha (public alpha 2)
----------------------------
For XCX Recomp 0.1.21 with game update 2.0.0. Gameplay baseline: development build V433.
A reliability update for the host's AI companions as the guest sees them. No new features. Installing it over
0.1.0-alpha builds the co-op program again and keeps both players' saves.

Fixed and confirmed in play (two players, several sessions, plus automated runs)
- The guest's game could close when the host changed a companion in Active Members. Changing companions,
  several times in a row, no longer does that.
- A companion the host had just changed in kept running in place on the guest's screen after it stopped. It now
  stops and stands. (Automated check: 0 of about 300 samples per session, 26 of 300 before.)
- Changing a companion and then fast travelling could lose the guest. The guest now follows the travel.
- After a fast travel, or right after joining, the other player on foot could be shown sliding with a stiff
  body until it boarded a Skell and got out again. It is now corrected by itself (at the join this can take about
  two seconds).
- After the host was defeated with the Skells destroyed and came back, the host and its companions moved with
  stiff bodies on the guest's screen. They now walk normally.
- A Skell boarded while the other game missed the boarding stayed kneeling and slid. It now stands up.

Corrections included but NOT verified
(neither situation came up again after the change, in play or in the automated runs, so these two have never
been seen working; they may or may not fix the problem)
- A companion's Skell that is shown ridden but stays in the kneeling pose on the other screen: the mod now tries
  to wake it after about two seconds. The problem was seen once before the change and has not occurred since.
- Very rarely the guest's game closed about half a second after "Begin Split-Screen Co-op": the mod now tries to
  carry on instead of closing the game. The problem has not occurred since the change.

Known limitations
- The guest sees only some of the attack animations of the host's AI companions' Skells.
- Very rarely a game closes with an error two or three seconds after it starts, before the title screen. This is
  not caused by the co-op; start again.
- Changing in a companion that owns a Skell was not tested on its own.
- A destroyed Skell stays gone until it is repaired at the Barracks, as in the single-player game.
- Join out of combat.
- The guest's row in the host's Active Members screen must be left alone.
- A companion removed without a replacement stays visible to the guest.
- Two players on one PC only. Three or four players and online play are not part of this release.
- Tested on one machine (Windows 11, 2560x1600 display, two Xbox controllers).

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
