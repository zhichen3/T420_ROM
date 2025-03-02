This contains coreboot rom for T420

# Extract vga bios
We will use [git@github.com:LongSoft/UEFITool.git](UEFITool) to extract
vga bios.
First build UEFITool by following the guideline.
In short, go to the UEFITool within UEFITool  directory which contains
the file `uefitool.pro` and do:

`qmake uefitool.pro && make`

Now an exectuable `UEFITool` should appear, then run it:

`./UEFITool`

1. Select the rom file you wish to extract the bios from.
2. Select `search` (CTRL + f) and select `text` and unselect `unicode`
3. Now search `VGA Compatible BIOS`. A line should appear on the bottom
   double click should take you to the file that contains the vga bios
4. Right click that file and select `extract body` to get the binary file.
