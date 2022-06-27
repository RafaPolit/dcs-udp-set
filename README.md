# DCS-UDP-SET

This is a very simple UDP listener to emit LoSetCommand into DCS.  

The motivation is to use it with [DCS-WEB-BIOS](https://github.com/RafaPolit/dcs-web-bios) in order to provide a GUI for switching MODES in FC3 without having to remember which "numbers" are available for each plane.

## Instalation Procedure

A release and source code is comming, but for now, simply:
- copy the contents of `src` into `<SavedGames>\DCS[.openbeta]\Scripts\`
- if you don't have an existing `Export.lua` file in there, create one and copy the following code in it with:

```
dofile(lfs.writedir()..[[Scripts\DCS-UDP-SET\UDP-SET.lua]]);
```

If you already have the file, just append the above line to the end of the file with a text editor like Notepad++.

## Reference

This code is mostly a copy-paste from the UDP listener Protocol and Protocol IO from [DCS-BIOS](https://github.com/DCSFlightpanels/dcs-bios).  All credit goes to them and the community for creating the socket listener and UDP parsing.  I merely replaced the actual command with a LoSetCommand instead of clickable items.
