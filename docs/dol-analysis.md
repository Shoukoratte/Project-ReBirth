# DOL Analysis

## Target Executable

- Filename: `main.dol`
- Size: `2,644,832 bytes`
- SHA-256: `0A5DDBBDFA4FA2235E4D6018ACB3F2EFD1599CD5DE2478E98A65346CF58EA1E9`

## Entry Point

- Entry point: `0x80004050`
- Identified symbol: `__start`

The executable does not begin directly at `main`.

The startup runtime initializes the execution environment before
eventually transferring control to the program's main logic.

## Main Function

- Address: `0x8014A8D0`
- Size: `0x50`

## Major Sections

| Section | Address | Size | File Offset |
|---|---:|---:|---:|
| `.init` | `0x80004000` | `0x26BC` | `0x100` |
| `.text` | `0x80006F20` | `0x2171E8` | `0x27C0` |
| `.rodata` | `0x8021E1E0` | `0xF968` | `0x21A2E0` |
| `.data` | `0x8022DB60` | `0x56A50` | `0x229C60` |
| `.bss` | `0x802845C0` | `0x8F1D0` | N/A |
| `.sdata` | `0x803137A0` | `0x2CB4` | `0x2806C0` |
| `.sbss` | `0x80316460` | `0xAFC` | N/A |
| `.sdata2` | `0x80316F60` | `0x27DC` | `0x283380` |

## Current Understanding

- File offsets describe where data exists inside the DOL file.
- Runtime addresses describe where sections are loaded in Wii memory.
- `.text` primarily contains executable PowerPC code.
- `.rodata` contains read-only data and constants.
- `.data` contains initialized writable data.
- `.bss` represents zero-initialized runtime memory and does not occupy
  normal file storage.