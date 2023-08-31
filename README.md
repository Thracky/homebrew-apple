This repo has some additions that allow the BG3 launcher to work properly, mainly an implementation of `ResolveLocaleName` that was added to standard wine some time ago.

With Game Porting Toolkit beta 4, this will now allow you to run BG3 from steam, with no fancy tricks. This means cloud and cross-platform saves will work.

Any other current method of running BG3 means you are either not actually using GPTK/D3DMetal (because you've used CXPatcher or Whisky + DXVA or something of that nature) or you have no cloud/cross platform saves because you have to launch bg3_dx11 directly.

# Apple Homebrew Tap

This repository contains formulae for use with Homebrew: https://brew.sh

## Special Instructions

### `game-porting-toolkit`

Using the `game-porting-toolkit` formula requires downloading the Game Porting Toolkit from [developer.apple.com](https://developer.apple.com/download/all/?q=game%20porting%20toolkit).

**To use this Formula instead of Apple's, instead of `brew -v install apple/apple/game-porting-toolkit` mentioned in the Game Porting Toolkit readme, grab this formula and run the following from the `Formula` subdirectory (It will take a LONG time to compile!):**

`HOMEBREW_NO_INSTALL_FROM_API=1 brew reinstall --build-from-source -v game-porting-toolkit-compiler.rb game-porting-toolkit.rb`

Follow the rest of the steps as outlined in the GPTK readme.

