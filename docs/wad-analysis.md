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