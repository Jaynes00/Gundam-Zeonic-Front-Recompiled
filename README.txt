GUNDAM ZEONIC FRONT RECOMPILED
Version RC6 Build 4 (1.0.1-rc6.4), release candidate for 1.0.1
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
  logs\, Bug Reports\       created when you play / report


LEGAL
-----
Mobile Suit Gundam: Zeonic Front is (c) Sotsu Agency, Sunrise and Bandai.
This port contains no game data from the original disc; it reads the data
from your own disc image. It is a non-commercial fan project and is not
affiliated with or endorsed by the rights holders.
