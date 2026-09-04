# WAD Analysis

## Source

This analysis is performed using a legally obtained personal copy of
**Castlevania: The Adventure ReBirth (WiiWare)**.

Original game files are not included in this repository.

## Original WAD

- Filename: `Castlevania Rebirth.wad`
- Size: `36,939,840 bytes`
- SHA-256: `3D819D3C8AB9FFEE37093D96774A530630CC4B1B92E520282EB6D442F44F5BFF`

## Purpose

The purpose of this document is to understand the structure of the WiiWare
WAD before analyzing the executable contained within it.

## Current understanding

A Wii WAD is an installable container that stores metadata and encrypted
title contents.

Important components include:

- WAD header
- Certificate chain
- Ticket
- TMD (Title Metadata)
- Content files

## Status

Step 1.0 completed:
- Original WAD located
- Filename recorded
- Size recorded
- SHA-256 recorded

Next:
- Study the conceptual internal structure of the WAD
- Choose an extraction tool
- Extract contents without modifying the original file

## WAD Extraction

The WAD was successfully verified and extracted using
decomp-toolkit (dtk) 1.8.3.

### Extracted metadata

- Ticket: `0001000157443945.tik`
- TMD: `0001000157443945.tmd`
- Certificate chain: `0001000157443945.cert`
- Trailer: `0001000157443945.trailer`

### Extracted contents

| Content | Size |
|---|---:|
| `00000000.app` | 398,272 bytes |
| `00000001.app` | 1,368,416 bytes |
| `00000002.app` | 32,301,393 bytes |
| `00000003.app` | 2,156,800 bytes |
| `00000004.app` | 312,576 bytes |

At this stage, the purpose of each content has not yet been confirmed.

### Observations

- Five title contents were extracted.
- Content `00000002.app` is significantly larger than the others.
- No assumptions have yet been made about which content contains the executable.
- Original extracted files remain inside `local/` and are not tracked by Git.

## Executable Identification

Content `00000001.app` was initially not recognized as a DOL.

Its first byte indicated Nintendo LZ-style compression, so the content was
decompressed using `dtk nlzss decompress`.

The decompressed result was successfully recognized by `dtk dol info` as a
valid Wii DOL executable.

Confirmed chain:

`WAD -> 00000001.app -> NLZSS-compressed data -> DOL executable`

The executable contains recognizable Wii / CodeWarrior runtime symbols,
including OS, GX, DVD, PAD, NAND, C++ runtime, and MetroTRK components.

DTK also reported:

`79 discovered functions from exception table`

## Main Executable

The compressed boot content was decompressed and saved locally as:

`local/work/main.dol`

This file is not tracked by Git.

- Source content: `00000001.app`
- Format: Wii DOL
- Compression layer: Nintendo LZ / NLZSS
- Size: `2,644,832 bytes`
- SHA-256: `0A5DDBBDFA4FA2235E4D6018ACB3F2EFD1599CD5DE2478E98A65346CF58EA1E9`