Jay's Magic Patch (.JMP) is a patch file format that allows the HEX code patching of any Xbox ".XBE" executable file via my online patching tool Jay's Magic Patcher: https://www.jayxbox.com/retail-game-modification/jays-magic-patcher

The patch file is human-readable via any text editor.

Every .JMP patch that I create is typically based on the work of others, and all patches subsequently credit those authors both in the file name and the "author=" line within.
All patches are provided as-is, many are untested as of writing this. If you are an author of a patch and want credit, let me know!

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

Patch records can theoretically go on forever, however my patcher can realistically only handle about 200. If your patch requires more than 100 records then it is probably a bad patch. Most clean patches require about 1 to 6 patch records.
If you were looking to create a .JMP file, download one from here and recycle the formatting I use.
