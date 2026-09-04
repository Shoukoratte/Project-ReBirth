# Work Log

## 2026-09-04 - Project setup and WAD identification

### Completed
- Initialized local Git repository
- Added `.gitignore`
- Added `README.md`
- Created first commit
- Connected project to GitHub
- Verified WAD location
- Recorded WAD filename, size, and SHA-256

### WAD Information
- Filename: `Castlevania Rebirth.wad`
- Size: `36,939,840 bytes`
- SHA-256: `3D819D3C8AB9FFEE37093D96774A530630CC4B1B92E520282EB6D442F44F5BFF`

### Notes
- Original files are kept inside `local/` and ignored by Git.
- Repository contains only documentation, scripts, and reconstructed work.
- The project will follow a hybrid strategy:
  - decompilation/reconstruction as the main goal
  - static recompilation as a temporary bridge

### Next Step
- Step 1.1: Understand the internal structure of a Wii WAD

### WAD extraction completed

- Verified WAD integrity successfully.
- Extracted Ticket, TMD, certificate chain, trailer, and five contents.
- No original game files were added to Git.
- Next task: identify the internal format and purpose of each `.app` content.

### Executable located

- Tested `00000001.app` as a DOL directly: failed.
- Inspected binary header.
- Identified Nintendo LZ-style compression.
- Decompressed `00000001.app`.
- Confirmed decompressed output is a valid DOL.
- DTK recognized Wii SDK / CodeWarrior runtime symbols.
- 79 functions were recovered from exception table metadata.

### Main executable prepared

- Decompressed `00000001.app`
- Renamed decompressed output to `main.dol`
- Confirmed valid Wii DOL structure with decomp-toolkit
- Recorded executable size: `2,644,832 bytes`
- Recorded executable SHA-256:
  `0A5DDBBDFA4FA2235E4D6018ACB3F2EFD1599CD5DE2478E98A65346CF58EA1E9`
- `main.dol` remains inside `local/` and is ignored by Git