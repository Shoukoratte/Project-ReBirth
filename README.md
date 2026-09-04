# Castlevania: The Adventure ReBirth — Decompilation Project

Educational reverse-engineering and decompilation project for **Castlevania: The Adventure ReBirth (WiiWare)**.

## Goals

* Understand and document the original Wii executable.
* Learn the Wii WAD and DOL formats.
* Study the game's PowerPC code.
* Analyze the executable with Ghidra.
* Reconstruct game logic in readable C/C++.
* Use static recompilation as a temporary bridge for unknown functions.
* Build a portable runtime for PC.
* Keep platform-specific code separated from game logic.
* Experiment with true widescreen support.
* Experiment with higher rendering resolutions.
* Add modern controller support.
* Keep the architecture portable for possible future homebrew targets.

## Project Philosophy

This project uses a hybrid development strategy:

* **Decompilation and reconstruction** are the main goals.
* **Static recompilation** may temporarily execute functions that have not yet been understood or reconstructed.
* Recompiled functions should gradually be replaced by documented native C/C++ implementations.

## Legal Notice

This repository does **not** contain original game files.

Users must provide their own legally obtained copy of the game.

The following files are never intended to be distributed through this repository:

* WAD files
* Original DOL files
* Original APP contents
* Game assets
* Audio
* Textures
* Encryption keys

## Current Status

Early research and project setup.

### Progress

* Repository setup: 100%
* WAD analysis: 0%
* Executable analysis: 0%
* PowerPC mapping: 0%
* Functions identified: 0%
* Functions reconstructed: 0%
* Static recompilation: 0%
* PC runtime: 0%

## Repository Structure

```text
docs/       Technical documentation
notes/      Research notes
scripts/    Analysis and automation scripts
src/        Reconstructed source code and runtime
tools/      Project-specific tools
local/      Private game files — ignored by Git
```

## Development Status

This project is experimental and intended for educational and preservation research.
This project use AI for educational process and learning for someone who never did something like this before but have the basic knowledge from Engineering to make it real.
