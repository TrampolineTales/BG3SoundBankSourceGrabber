# Baldur's Gate 3 Soundbank Source Grabber

This is a tool that forms search query strings of `CAkSound` entries in `XML` files. This is primarily for use with unpacked Baldur’s Gate 3 game files, but it may work with other games with similar file structures (this has not been tested). We've also made a YouTube tutorial showing how to use the tool [here](https://www.youtube.com/watch?v=zt9zGqRqJoo).

## Prerequisites

* Familiarity with [ShinyHobo's BG3 Modder's Multitool](https://github.com/ShinyHobo/BG3-Modders-Multitool) to unpack game files
* Familiarity with tepig327's instructions from [this pinned post](https://www.nexusmods.com/baldursgate3/mods/8240?tab=posts) on Nexus. 

## Necessary Programs

* [wwiser](https://github.com/bnnm/wwiser) to convert a `BNK` file to an `XML` file
* [Python](https://www.python.org/) to run wwiser.
* Your text editor of choice (I recommend [Notepad++](https://notepad-plus-plus.org/))
* To play the `WEM` files, [foobar2000](https://www.foobar2000.org/download) plus [this vgmstream component](https://www.foobar2000.org/components/view/foo_input_vgmstream).

## Baldur’s Gate 3 Usage

* Download the correct ZIP file for your operating system from the [releases](https://github.com/TrampolineTales/BG3SoundBankSourceGrabber/releases) page.
* Unzip and run the application.
* Open your converted `VOCALS.bnk.xml` (or any converted `BNK` → `XML` file, we’re using this one as an example) with your text editor. It’s a VERY large file, so I recommend selecting View > Fold Level > 7 if you’re using Notepad++ to make it a little more manageable.
* Choose a section of `obj na="CAkSound"` entries. I always do ONE section at a time, they all have either a `"CAkRanSeqCntr"` or `"CAkSwitchCntr"` above and below one section.
* Copy the whole group of `CAkSound` entries into the tool’s text box, and press “Get Source Query ID.” This will copy a string query of the source file entries for that section to your clipboard.
* You can then use that query to search via your file explorer in your unpacked `SharedSounds\Public\Shared\Assets\Sound` location.

Special thanks to the [Down by the river modding community](https://discord.gg/downbytheriver).
