# Files needed for coreboot
This contains coreboot rom for T420

## Extract vga bios
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

## Bootsplash IMG
The bootsplash image needs to be in jpg format. Use GIMP to open up
image of desire, then export the image in jpg format, and uncheck
`progressive` option, and choose subsampling to `4:2:0 (chroma quartered)`.
Then make sure the resolution of the image in exactly `1024x768`.
