# TUNIC MSU

MSU JSON for the TUNIC soundtrack.

## You will need

* Latest release of [MSUPCM++](https://github.com/qwertymodo/msupcmplusplus/releases/latest). `msupcm.exe` is the goal.
* A copy of TUNIC. Any PC version should work; the macOS version will likely work too, but I couldn't tell you where the files are at
  * PC
    * [Epic Games](https://store.epicgames.com/en-US/p/tunic)
    * [Humble Bundle](https://www.humblebundle.com/store/tunic)
    * [Steam](https://store.steampowered.com/app/553420/TUNIC/)
* A copy of the TUNIC soundtrack
  * PC
    * [Steam](https://store.steampowered.com/app/1928140/TUNIC_Original_Game_Soundtrack/)
* Or a bundle
  * PC
    * [GOG](https://www.gog.com/en/game/tunic_bundle)
    * [Steam](https://store.steampowered.com/bundle/25280/Tunic_Game__Soundtrack/)

* Yes, you will need _both the game and the soundtrack_
* [foobar2000](https://www.foobar2000.org/)
* The [foobar2000 component](https://vgmstream.org/downloads) for vgmstream must be installed in foobar2000

## Steps

1. Run foobar2000
1. Install foobar2000 component
    * File `->` Preferences `->` Components `->` Install...
    * Navigate to foobar2000 component
    * Apply
1. Find TUNIC's folder
    * Steam: `steamapps/common/TUNIC/Tunic_Data/StreamingAssets`
    * XBOX: `Content/Secret Legend_Data/StreamingAssets`
1. For `music_main.bank` & `sfx_main.bank`
    * Open the file in foobar2000
    * Select all tracks with `CTRL+A`
    * Right-click one of the selected files `->` Convert `->` ...
        * Output format: FLAC level 5
        * Destination: File name pattern: `%title%`
        * Processing: None
        * Convert
1. Place a copy of the `.json` and `msupcm.exe` into the folder with the `.flac` files
1. Edit the .json to contain the full path to the song Early Birds .flac file in the soundtrack - or, alternatively, copy and paste Early Birds into the folder with the rest of the exported files. Either way, those lines need to be changed to point to the right location
1. Drag the `.json` file onto `msupcm.exe` to start the conversion
    * Alternatively, run `msupcm.exe` via the commandline and load the proper `.json` file

Hey, now you have MSU files to attach to your ROM!

## Notes

The music is super loud in the game. It's been normalized to -10. If that's still too loud, fiddle with line 8 in the JSON. Also bear in mind that a couple of tracks have been manually set to 0, since they're quiet.

## Contact

Me if something is wrong. If you have song placement recommendations, they will be ignored. `fantallis#3161` on Discord.
