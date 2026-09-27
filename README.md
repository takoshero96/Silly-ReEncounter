[README.txt](https://github.com/user-attachments/files/32712861/README.txt)
SILLY REENCOUNTER
Unofficial fan project: play Serious Sam: Next Encounter (Nintendo GameCube, 2004) as a native PC program,
built on your own PC from your own copy of the game.

HOW IT WORKS
  This download contains NO game code and NO game data. You supply your own disc image, and the launcher turns it
  into a PC program on your computer:
  1. Select Disc: pick your disc image (.iso, .gcm, or Dolphin .rvz / .wia / .gcz / .ciso), or drop it on the window.
     The launcher checks that it is Serious Sam: Next Encounter (USA) and whether it matches a known good dump.
  2. Install Game:
       - copies the game's files out of your disc image into the game_data folder (about 1.3 GB),
       - downloads the free LLVM-MinGW compiler (about 170 MB, only the first time) from its official GitHub
         release into build-kit\toolchain,
       - translates the game's program (main.dol) from your disc into C++ and compiles it, then links it with the
         PC port in build-kit\lib. This makes SillyReEncounter-Game.exe. It takes a few minutes.
  3. Play.
  Everything made from your disc stays on your PC. Do not share game_data or SillyReEncounter-Game.exe: they are
  made from the game and are only for you.

REQUIREMENTS
  Windows 10 or 11, 64-bit; a GPU with OpenGL 3.3; about 3 GB of free disk space; an internet connection the first
  time you install (for the compiler download only).
  Your own legally obtained Serious Sam: Next Encounter for GameCube (USA, G3BE9G), dumped from a disc you own.
  Do not ask for, share or download disc images.

FILES
  SillyReEncounter.exe   the launcher
  gctool.exe               command-line disc tool: gctool info|verify|extract <image> [...]
  known_dumps.txt          SHA-1 checksums of known good dumps (checksums only)
  build-kit\               what the launcher needs to build the game on your PC:
      ssne-recomp.exe        translator from the GameCube program to C++
      G3BE9G_r1.sym          function names for the translator
      include\, lib\         the PC port and its runtime, prebuilt (no game code)
      kit.ini                build settings (compiler download address, compiler flags)
      work\logs\             build logs, if something goes wrong
  LICENSE.txt              public-domain dedication (The Unlicense) for this project's code
  THIRD-PARTY-NOTICES.txt  and the licenses folder: licenses of the libraries and fonts used
  source\                  complete source code (see source\README.md and source\docs\BUILDING.md)

  The launcher saves launcher.ini next to itself. It connects to the internet only to download the compiler from
  github.com, and only when you choose Install Game.

IN-GAME
  Settings are saved to settings.ini and memory card saves to saves\MemoryCardA.USA.raw, next to the game program.

HOTKEYS (work any time in the game window; also listed in F12 > Hotkeys)
  F12 / pad Back ..... settings menu (Esc closes it)
  F1 ................. log and statistics window
  Shift+F1 ........... show / hide the info bar at the top (fps, frame limit, key hints)
                       (also F12 > Graphics > "Show info bar at the top"; remembered in settings.ini)
  F2 ................. release the mouse (click the game window to capture it again)
  F3 ................. mute / unmute
  F4 / F5 ............ volume down / up (10% steps)
  F6 / F7 ............ internal resolution down / up (GPU renderer)
  F8 ................. aspect ratio: 16:9 / 21:9 / 4:3
  F9 ................. capture the next frame to the debug folder (GPU renderer, for bug reports)
  F10 ................ frame rate limit: 60 (original) / 120 / 144 / unlimited
  F11 or Alt+Enter ... fullscreen

LEGAL
  Silly ReEncounter is an unofficial, non-commercial fan project. It is not affiliated with, endorsed by or
  sponsored by Croteam, Devolver Digital, Climax Group, Global Star Software, Take-Two Interactive or Nintendo.
  "Serious Sam" and "Serious Sam: Next Encounter" are trademarks of their respective owners and are used here only
  to identify the game this software works with. Nintendo GameCube is a trademark of Nintendo.
  The project's own code is dedicated to the public domain (LICENSE.txt). It is provided "as is", without warranty
  of any kind.
