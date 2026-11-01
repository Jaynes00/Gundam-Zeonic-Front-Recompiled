GUNDAM ZEONIC FRONT RECOMPILED
Version RC6 Build 5 (1.0.1-rc6.5), release candidate for 1.0.1
=====================================================================

Gundam Zeonic Front Recompiled is a fan-made native Windows port of the PlayStation 2 game "Mobile Suit
Gundam: Zeonic Front" (US release, SLUS-20233). Please report anything that
looks, sounds or plays differently from the PS2 original.

Project page (updates, bug reports):
  https://github.com/Jaynes00/Gundam-Zeonic-Front-Recompiled

You need YOUR OWN copy of the US PS2 disc as a disc image (.iso). No game data
is included in this folder, and none may be shared with it.


WHAT YOU NEED
-------------
- Windows 10 or 11, 64-bit.
- A Direct3D 11 graphics card (practically any PC from the last 10 years).
- About 2.1 GB of free disk space for the game data copied from your disc.
- A disc image of "Mobile Suit Gundam: Zeonic Front" (USA, SLUS-20233).
  The Japanese releases and modified / patched images are not supported.
- Optional: an XInput gamepad (Xbox controller or compatible).


FIRST START
-----------
1. Keep this whole folder together (you may move or rename the folder).
2. Start ZeonicFrontLauncher.exe.
3. Click "Browse..." and choose your disc image.
   The launcher checks that it is the supported US disc, then copies the ten
   files the game needs (game data and the six movies) into your own user data folder
   (%LOCALAPPDATA%\ZeonicFrontPC\disc). This takes up to a minute and happens
   only once. Your disc image is never changed.
4. Click PLAY.

The launcher remembers your disc image. If you move the image, select it again.

Volume: the slider under the buttons sets the game's volume (0-100 %). It is
remembered and works while the game is running. It does not change the
Windows volume.

If Windows SmartScreen warns about an unknown publisher, choose
"More info" -> "Run anyway" (the files are not signed).


CONTROLS
--------
Any XInput gamepad works like the PS2 controller. The keyboard works at the
same time (only the first connected gamepad is used). PlayStation and other
non-XInput controllers need Steam Input or a similar tool.

Keyboard (= PS2 controller):
  W A S D ............ left stick (move)
  Arrow keys ......... right stick (camera)
  J or left mouse .... R1 (lock on / fire)
  Left Shift ......... L1 (run)
  Q / E .............. L2 / R2 (squad orders)
  Page Up / Page Down  D-pad up / down
  Home / End ......... D-pad left / right
  Z .................. Cross (confirm)
  X .................. Circle
  C .................. Square
  V .................. Triangle (back)
  Enter .............. START
  Backspace .......... SELECT (the full battlefield map; gamepad: View / Back)

PC-only keys:
  F6 ................. 60 / 30 frames per second
  I .................. frame interpolation on / off
  F7 / F8 ............ draw distance / fog (graphics extras, not original)
  F10 ................ graphics options (aspect ratio 4:3 / 16:9, resolution,
                       window / fullscreen, window size, draw distance...)
  Alt+Enter .......... fullscreen / window
  Esc ................ quit the game: asks first (KEEP PLAYING / QUIT TO
                       DESKTOP; progress since your last save is lost)


SAVES AND SETTINGS
------------------
- Saves are kept in the "saves" folder next to the launcher
  (ZFRONT_SYSTEM.zfsave = records, unlocks, simulator progress;
   ZFRONT_SLOTnn.zfsave = your campaign slots; .bak = the previous copy).
  Back up this folder if you like. Saves from earlier test builds can be
  copied into it.
- Display settings are kept in zf_view_settings.ini next to the launcher.
- The launcher's own setting (your disc image path) is kept in
  %LOCALAPPDATA%\ZeonicFrontPC\launcher.ini.


UPDATES
-------
- When it starts, the launcher checks the project's GitHub page for a newer
  build and shows the result below the volume slider ("New Update Available"
  or "You're running the latest version"). Without internet it simply says it
  could not check; you can always play the installed version.
- Download & Install downloads the new build, checks it against the checksum
  published with it, asks you to close the game if it is running, and then
  installs it and restarts the launcher. Your saves, display settings, logs
  and any files of your own in this folder are kept. The replaced files are
  kept in "update_backup"; if anything goes wrong during the install, the
  previous version is put back automatically.
- Release notes opens the release's page on GitHub. Update options: check at
  start (on), download automatically (off; it is still installed only when
  you choose), notifications (on), and the channel: Preview (release
  candidates, the default for this build) or Stable (final releases only).
- Updating from RC6 Build 2 or older: those launchers have no updater. Copy
  your "saves" folder and zf_view_settings.ini into this folder once.


RANDOMIZER (OPTIONAL, OFF BY DEFAULT)
------------------------------------
Not in the PS2 game. Turn it on in GRAPHICS OPTIONS (F10) -> RANDOMIZER >.
The setting takes effect at the next mission's deployment menu. While it is
on, every main mission of ROUND 1 and ROUND 2 is randomized:
- YOUR PILOTS: when you reach the deployment menu of a mission, every pilot
  gets a random mobile suit (any of the 30), weapon (any of the 24 hand weapons;
  the GUNTANKs get one of their cannons, a GUNCANNON / GUNCANNON MP always its
  own cannon), melee weapon and shield (none with
  the two-handed M-LAUNCHER / GATLIN GUN).
- YOUR SUPPLIES: nothing is equipped for you. Every pilot
  gets a random choice of support items (a random number of item types,
  each at a random level) and a random amount of support space (6 to 20).
  Open SUPPORT in TEAM SETUP and pick what fits in the space. A GUNCANNON
  (and GUNCANNON MP) still starts with the level 1 shoulder cannons
  equipped, and any other suit that has cannons in the PS2 game (the
  MUDROCKs, the GUNDAM (G)) with its own level 1 cannon; you can take them
  off or swap them for a higher level if it is offered. A suit without
  cannons is never offered cannon supplies. On EASY every pilot starts
  with ARMOR 02 equipped. A
  GUNTANK never gets a shield (it cannot carry one; this build also takes one
  off at the sortie if you pick it by hand). TEAM SETUP shows the roll; it cannot be changed
  (see LOADOUTS ARE LOCKED). Retrying the same mission
  keeps your loadouts; the next mission rolls again.
- THE ENEMY: every enemy squad (mobile suits, tanks, aircraft and
  installations) becomes its own random mobile suit (Zeon or Federation) with
  a random weapon, so two squads of the same tanks can turn into two
  completely different suits. The three units of a squad stay alike. A
  squad that had no melee weapon (tanks, batteries, installations) gets a
  random one. Plain
  buildings, your allies and the squads a mission's ending depends on
  (e.g. Agar's squad in Mission 5, the Big Tray in Mission 7) are not changed,
  nor are the tanks and vehicles of Mission 8 (the Dobday rescue: as mobile
  suits they reached the Dobday at once and the mission failed). The swaps stay within
  the memory the mission normally uses (a swap that would not fit is passed
  over for one that does), so the big missions still load.
- SEED: everything comes from the seed in randomizer.ini (next to the game,
  created with a new seed the first time the game starts). The same seed always gives the
  same loadouts and enemies for a given round and mission; change the seed
  (any number) for a new run. randomizer.ini also turns each part on or off:
    enabled = 0             (1 = randomizer on)
    seed = 123456
    players = 1             (suits, weapons, melee weapons, shields)
    supplies = 1            supply_types = 8   (0..20: the most kinds of
                            supplies a pilot is offered; each pilot gets
                            from half of it up to it)
    enemies = 1             enemy_weapons = 1
  zf_view reads the file when it starts: restart the game after a change.
- IN-GAME SETTINGS: GRAPHICS OPTIONS (F10, or Back + Start, or OPTIONS in the
  briefing / deployment menus) -> RANDOMIZER >. The RANDOMIZER page has:
    RANDOMIZER          On / Off (Off = the normal game; TEAM SETUP opens again)
    SEED MODE           One seed for Round 1 and 2 / New seed every mission
    SEED                cross = a new random seed, left / right = -1 / +1
    DIFFICULTY          Easy   = every pilot gets the ARMOR x2 upgrade
                        Normal = no change
                        Hard   = enemy squads have 1.5x HP
                        Brutal = enemy squads have 2x HP
                        (Hard / Brutal: no ace-skill RX-78-2 or Char's
                        Zaku for your pilots either)
    YOUR LOADOUTS, YOUR SUPPLIES, SUPPLY CHOICES (0..20),
    ENEMY SQUADS, ENEMY WEAPONS
  Changes are saved to randomizer.ini at once and apply from the next
  mission's deployment (a mission already rolled keeps its rolls).
- SPOILERS: every roll is written to logs\randomizer_spoilers_seed_<seed>.txt.
- The Simulator and training programs are never randomized.
- Some missions get much easier or harder (a GUNDAM where a ZAKU was). Enemy
  name labels and radio lines may still name the original enemy.

QUALITY OF LIFE (OPTIONAL)
--------------------------
Not in the PS2 game. GRAPHICS OPTIONS (F10) -> QUALITY OF LIFE >. These
work with the randomizer on or off and are saved in randomizer.ini.
- MISSION SELECT: Off / Round 1 / Round 2, and START MISSION (1..13).
  When set, NEW GAME on the title screen starts at that round and mission
  instead of Mission 1. You play with the team a New Game has (the pilots
  and suits normally earned in earlier missions are not there unless the
  randomizer gives them). It is an ordinary campaign from there: it
  continues to the next missions and can be saved. CONTINUE and LOAD are
  not changed. Set it back to Off for a normal New Game.
- SKIP STORY SCENES: On = no training offer before Missions 1-3, no story
  (situation) scene before the briefing, no stage epilogue after a victory,
  and the movies are skipped (the logos at start-up stay). The mission
  briefings (MISSION / INFORMATION / ADVICE) are still in the briefing menu.
- MISSION STATS (Off by default): after every mission (cleared, retired or failed) the
  LAST MISSION page opens with:
    the result, the mission time, the score and grade (1 = best, 6 = worst;
    on a victory), and the randomizer seed;
    for each of your teams (BLUE / YELLOW / RED) its suit and weapon, its
    kills (split by whether the enemy was unaware of the team, alerted, or
    in combat with it; unaware kills score the most) and its losses;
    kills by allies, enemy units destroyed and still active;
    the totals of this session.
  Close it with cross / Enter or START. With MISSION STATS Off there is no
  pop-up; the page stays under QUALITY OF LIFE -> LAST MISSION, and every
  mission is also added to logs\mission_stats.txt.
  A RESTART from the pause menu updates the page without opening it.

MISSION EDITS (OPTIONAL, EXPERIMENTAL)
--------------------------------------
Not in the PS2 game. You can move enemy and allied squads and change their
suits and weapons with a text file named mission_edits.txt next to
ZeonicFrontLauncher.exe. Without that file nothing changes.

1. Find the squad numbers: set mission_info = 1 in randomizer.ini, start the
   mission once, and open logs\mission_info_r<round>m<mission>.txt (e.g.
   mission_info_r1m1.txt). Every GROUP is a squad: 0..2 are your teams,
   3..7 allies and support, 8 and up the enemy. Its "start" line is the cell
   (x, z) where it begins. The file shows the mission as loaded, edits
   included.
2. Write one edit per line in mission_edits.txt (# starts a comment):
     r1m1 group 11 start 64 34 heading 8   start cell (x, z); heading in
                                           steps of 22.5 degrees, 0 = north,
                                           4 = east, 8 = south, -4 = west
     r1m1 group 11 weapon 13               the weapon (id below)
     r1m1 group 11 suit 11                 the suit (id below)
     r1m1 group 12 hold                    the squad stays at its start
     r1m1 group 13 waypoint 2 70 90        one point of its patrol route
   "r1m1" = Round 1 Mission 1 ("r2m7" = Round 2 Mission 7). Only mobile
   suits change weapons (tanks, aircraft and guns keep theirs). Give a squad its
   weapon before you make it a mobile suit.
3. Play the mission. logs\mission_edits_log.txt lists every edit that was
   applied and every one that was refused, with the reason.

Suit ids:   00 ZAKU I (PROTO)   01 ZAKU I (G)   02 ZAKU I (S)   03 ZAKU II
            04 ZAKU II (G)   05 ZAKU II (S)   06 GOUF MP   07 GOUF
            08 GOUF CUSTOM   09 DOM   0A DOM FUNF   0B DOM TROPEN
            0C ZAKU I (SCHMITZER)   0D ZAKU II (CHAR)   0E GOUF (RAMBA)
            0F DOM (TRI-STAR)   10 ZAKU II (GARMA)   11 GM   12 GM (G)
            13 GM COMMAND   14 GM SNIPER II   15 GM S-ARMOR   16 GUNDAM (G)
            17 GUNDAM   18 MUDROCK (G)   19 MUDROCK   1A GUNCANNON
            1B GUNCANNON MP   (not usable: 0D, Char's ace Zaku, which could
            not be hit, and the GUNTANKs 1C / 1D; 17 GUNDAM uses the
            normal RX-78-2, not Amuro's ace record)
Weapon ids: 00 120mm MG   01 105mm MG   02 90mm MG   03 ZAKU BZ
            04 RAKETEN BZ   05 GIANT BZ   06 SHOTGUN   07 120mm AR
            08 90mm AR   09 M-LAUNCHER   0A GATLIN GUN   0B 75mm VULCAN
            0C BEAM RIFLE   0D 90mm MG   0E 100mm MG   0F R-LAUNCHER
            10 RIFLE   11 BEAM SG   12 BEAM GUN   13 / 14 / 15 BEAM RIFLE
            16 HYPER BZ   17 M-LAUNCHER   18 CANNON (Guncannon)

Refused (listed in the log): your own squads (TEAM SETUP / ROUTE SETUP set
them), the squads a mission's ending or story needs (marked PROTECTED in
the info file), cells off the map or on blocked ground, a route that other
squads share, the GUNTANKs, a mobile suit without a weapon, and switching a
squad's side ("team"): in this game the side comes from the squad number.
If the edits make a mission too big for the game's memory, it loads without
them (the log says so). Edits apply on top of the randomizer's rolls.

LOADOUTS ARE LOCKED (RANDOMIZER ON)
-----------------------------------
With the randomizer on you play with what the randomizer gives you. In TEAM SETUP the
MS (suit) list and the WEAPONS list do not open (you hear the "refused"
sound). You still choose which pilots go out, and their squad role and
formation settings. The SUPPORT screen opens and shows only the
supplies the randomizer offers that pilot, within the pilot's random space
(with YOUR SUPPLIES Off it stays locked).
With the randomizer off (the default) TEAM SETUP then works as on the PS2: each pilot's
own suits, the suit's own weapons and the suit's own support items.


REPORTING BUGS
--------------
- Please report bugs as an issue on the project's GitHub page:
    https://github.com/Jaynes00/Gundam-Zeonic-Front-Recompiled/issues
  The questions in BUG_REPORT_TEMPLATE.txt are a good outline; add a
  screenshot if you can.
- If the game closes unexpectedly, the launcher offers to create a report file
  (in the "Bug Reports" folder). Attach it to your GitHub issue: it contains
  the build version, your Windows version and graphics card, whether the disc
  check passed, the last mission or simulator program you were in, the crash
  log and the end of the last game session log. It does not contain any data
  from your disc or your saves.
- For a crash, the files zf_view_crash.log (game folder) and the newest file in
  the logs folder ("Logs" button in the launcher) help too.
- Please read KNOWN_ISSUES.txt first: those items are already known.


FILES IN THIS FOLDER
--------------------
  ZeonicFrontLauncher.exe   the launcher (start this)
  ZeonicFrontUpdater.exe    installs an update (started by the launcher)
  zf_view.exe               the game (started by the launcher)
  zf_view.pdb               debugging symbols (makes crash reports useful)
  msvcp140*.dll, vcruntime140*.dll
                            Microsoft Visual C++ runtime (redistributable)
  README.txt                this file
  KNOWN_ISSUES.txt          what is known to differ or is not finished
  VERSION.txt               build version and file checksums
  BUG_REPORT_TEMPLATE.txt   the bug report questions
  saves\                    your saves (created empty)
  randomizer.ini            the randomizer and QUALITY OF LIFE settings (created when
                            the game first starts)
  mission_edits.txt         your mission edits (optional, see MISSION EDITS)
  logs\, Bug Reports\       created when you play / report


LEGAL
-----
Mobile Suit Gundam: Zeonic Front is (c) Sotsu Agency, Sunrise and Bandai.
This port contains no game data from the original disc; it reads the data
from your own disc image. It is a non-commercial fan project and is not
affiliated with or endorsed by the rights holders.
