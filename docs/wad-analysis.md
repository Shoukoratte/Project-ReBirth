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