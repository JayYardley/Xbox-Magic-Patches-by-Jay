# Xbox Magic Patches
by Jay

### Here is my humble collection of every patch I could find, converted into my .JMP patch format.
It's a work in progress.

Jay's Magic Patch (.JMP) is a patch file format that allows the HEX code patching of any Xbox ".XBE" executable file via my online patching tool Jay's Magic Patcher: [https://www.jayxbox.com/retail-game-modification/jays-magic-patcher](https://www.jayxbox.com/Retail-Game-Modification/Magic-Patcher.php)
The patch file is human-readable via any text editor.

Every .JMP patch that I create is typically based on the work of others, and all patches subsequently credit those authors both in the file name and the "author=" line within.
All patches are provided as-is, many are untested as of writing this. If you are an author of a patch and want credit, let me know!

<Details>
  <summary>Details about the .JMP format:</summary>

#### Here is what the filename of a patch should be formatted like to make it easy for others:
+ >Game Title
+ >{Nature of patch}
+ >(Game region the patch applies to)
+ >[Patch author].JMP

>Example: 50 Cent - Bullet Proof {720p} (GLOBAL) [Silverrock].JMP

#### Here is what the contents of a .JMP file looks like, let's start with the headers which use up 7 lines:

+ >#Jay's Magic Patcher (www.jayxbox.com)
+ >system=Xbox
+ >game-title=Cool game
+ >region=NTSC
+ >version=56550041 (VU-065)
+ >author=Jay
+ >notes=This patch is awesome

Any relevant information MUST be added after the "=" sign for each header. Headers can be blank but must not be removed.
For the "version=" header on xbox titles, I like including both the Title ID in HEX format, and the converted Title ID in brackets.

#### Below the headers are "Patch Records" and must initially be commented with a "#" line. Notice there is no line break between patch records.

There are two types of patch records.
+ >Search and Replace
+ >Offset

##### Search and replace:
+ >#This patch record searches for the first resulting "AABBCCDD" and replaces it with "DDCCBBAA"
+ >AABBCCDD
+ >DDCCBBAA

The second line of a patch record (the one after the comment line), dictates the HEX value to "find". The third line is the HEX value that goes in it's place, effectively replacing the original data.

##### Offset:
+ >#This patch record jumps to the offset "0x120" and inserts AABBCCDD
0x120:AABBCCDD

The colon is a separator for the offset and data.
Offset patch records can have the following offset formats and all mean the samne thing:
"120"
"0x120"
"00000120"
"0x00000120"

Patch records can theoretically go on forever.
If you were looking to create a .JMP file, download one from here and recycle the formatting I use. Alternatively you can generate a templated .JMP using a stock .XBE and a patched .XBE here: [XBE2Magic](https://www.jayxbox.com/Retail-Game-Modification/XBE2Magic.php)
</details>

### 🔍 Search this repo
> I've organised patches by the author's handle, so if you're looking for something quickly use the search feature and start typing the game title.
> 
Find this entry field at the top of the page and search "Widescreen" or "720p":

![search](https://github.com/JayYardley/Magic-Patches-by-Jay/blob/main/search.PNG?raw=true)

> In the near future, I would like to create a patch bounty system, which would allow the average Joe to donate into a pool per game. All outstanding pool amounts will be provided to the patch creator when it is determined to sufficiently meet the needs of a typical patch.
