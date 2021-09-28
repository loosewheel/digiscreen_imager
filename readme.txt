This is a Windows program which does not need to be installed.
Just unzip it. It runs on Linux under wine.

Paste an image maximum size 256 x 256.

Set the resolution of a single screen display.

Click Table to copy the image as a lua table to the clipboard.

Click Binary to save the image as binary data to a file.

Table is formatted as a table of display table sections of the image of the given
resolution. The display tables are ordered left to right, top to bottom.
Each display table contains a table for each row, top to bottom.
Each row table has hex color strings for the given resolution for each pixel, left
to right.
The outer table has 2 name values, "width" and "height", for the display tables
that make up the width and height.
Note, each section table can be sent to a single digiscreen.

Binary is formatted with a header of a single byte for the width followed by a
single byte for the height. These values are one less than the actual value for a
maximum of 256. Then each pixel is three bytes as red, green, blue, left to right,
top to bottom of the image. Binary data has to converted to a table structure 
before sent to the displays, but uses far less disk space.

Click Copy binary to table conversion to copy the code to convert binary image
file to a table, for the given resolution.

Click Copy binary image blit to copy the code to blit a binary image file to a
group of displays.

Click Copy table image blit to copy the code to blit a table image file to a
group of displays.

The display channel names of a group must all begin with the same prefix and
each followed immediately by the display 1 based ordinal number left to right,
top to bottom. Even if there is only 1.
