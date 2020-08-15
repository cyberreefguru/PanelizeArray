# PanelizeArray
ULP to create a panelized array of a PCB.

Changes in this version by CharlesVanDen:
- Issue: if the user's units are not MIL, the created panelized PCB will have the wrong size (way too big)
Solution: Add GRID MIL 50 2 in the beginning of the script

- Issue: If the library's name contains one or more spaces, the script will not work
Solution: Put the component's name between single quotes

- Issue: The command LINE is unknown in Eagle 7.2.0
Solution: replace LINE by WIRE

- Issue: the defaults for x/y array size are 0, which is not practicle
Solution: replace the defaults by 1,1

- Issue: If the user's units are not mil, but e.g. mm, the dialog box will show the word 'mm', but the actual values are still interpreted as mil
Solution: calculate back to mil from the user's units

- Issue: the approximate board size is only shown in mil, not in mm
Solution: also show the approximate board size in mm

<p>Based on original work by:<p>
<author>Author: Maurice SAAB (Lebanon) morisaab@yahoo.fr</author>
<p>
<author>Edited By: Todd Beyer (USA) tbeyer74@hotmail.com</author>
<p>
<author>Edited By: Thomas M. Sasala (USA) (cyberreefguru)</author>

<p>
<p><b>Usage:</b>
<p>Enter the variable values, confirm the settings, and click OK. A script will be created at the destination location. Once the script is generated, open a new board and run the script.  You can use the source board if you set the origin so it won't conflict with the original board.
<p><b>Variables:</b></p>
<p><b>Origin</b> - where to start the panel array.  Usually (0,0) or (0,0) plus the height of the current board.</p>
<p><b>Columns</b> - Number of boards to make in the X direction.</p>
<p><b>Rows</b> - Number of boards to make in the Y direction.</p>
<p><b>X Spacing</b> - Distance between boards in X direction.</p>
<p><b>Y Spacing</b> - Distance between boards in Y direction.</p>
