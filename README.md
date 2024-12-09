# Xbox Magic Patches
by Jay

### Here is my humble collection of every patch I could find, converted into my .JMP patch format.
It's a work in progress.

Every .JMP patch that I create is typically based on the work of others, and all patches subsequently credit those authors both in the file name and the "author=" line within.
All patches are provided as-is, many are untested as of writing this. If you are an author of a patch and want credit, let me know!

> I've organised patches by the author's handle, so if you're looking for something quickly use the search feature and start typing the game title:

![search](https://github.com/JayYardley/Magic-Patches-by-Jay/blob/main/search.PNG?raw=true)

> In the near future, I would like to create a patch bounty system, which would allow the average Joe to donate into a pool per game. All outstanding pool amounts will be provided to the patch creator when it is determined to sufficiently meet the needs of a typical patch.

<Details>
  <summary>Details about the .JMP format:</summary>
      Jay's Magic Patch (.JMP) is a patch file format that allows the HEX code patching of any Xbox ".XBE" executable file via my online patching tool Jay's Magic Patcher: https://www.jayxbox.com/retail-game-modification/jays-magic-patcher
The patch file is human-readable via any text editor.

#### Here is what the contents of a .JMP file looks like, let's start with the headers:

+ >#Jay's Magic Patcher (www.jayxbox.com)
+ >system=Xbox
+ >game-title=Cool game
+ >region=NTSC
+ >version=56550041 (VU-065)
+ >author=Jay
+ >notes=This patch is awesome

Any relevant information MUST be added after the "=" sign for each header. Headers can be blank but must not be removed.

#### Below the headers are "Patch Records" and must initially be commented with a "#". The comment line separates these 2 records.

+ >#This patch record does nothing
+ >AABBCCDD
+ >AABBCCDD
+ >#This next patch record definitely does something
+ >AABBCCCDD
+ >DDCCBBAA

The first line of a patch record (exluding the comment line), dictates the HEX value to "find". The second line is the HEX value that goes in it's place, effectively replacing the original data.

Patch records can theoretically go on forever, however my patcher can realistically only handle about 200. If your patch requires more than 100 records then it is probably a bad patch. Most clean patches require about 1 to 6 patch records.
If you were looking to create a .JMP file, download one from here and recycle the formatting I use.
</details>
