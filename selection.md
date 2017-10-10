## Test cases for the item selection

### SELECT-01
Select files (and only files) in the icon view and Miller column view

**Expected:** When the mouse is hovered over any of the selected files, an overlay is displayed at the bottom on the window with the selected file count and the sum of the file sizes

### SELECT-02
Select folders (and only folders ) in the icon view and Miller column view

**Expected:** When the mouse is hovered over any of the selected files, an overlay is displayed at the bottom on the window with the selected folder count

### SELECT-03
Select folders and files in the icon view and Miller column view

**Expected:** When the mouse is hovered over any of the selected files, an overlay is displayed at the bottom on the window with the selected folder count, the selected file count and the sum of the file sizes.

### SELECT-04
In Icon View and Column View, primary button down on white space and  drag diagonally.

**Expected:** A shaded rectangle appears and any icon touched by it is selected. Icons leaving the rectangle become deselected. Selection remains when button is released.

### SELECT-05
In List View, primary button down on white space in Filename column and  drag.

**Expected:** A shaded rectangle appears and any icon touched by it is selected. Icons leaving the rectangle become deselected. Selection remains when button is released.

### SELECT-06
In List View, primary button down on white space in Size, Type or Modified column and  drag.

**Expected:** No shaded rectangle appears. Only row initially clicked on is selected.

### SELECT-07
In any view, select some files.  Change to a different view.

**Expected:** The same files are selected in the new view.  If necessary the new view scrolls to show the selected file(s)

### SELECT-08
In Icon view, select a file.  Hold down the Shift key and use the Left and Right Arrow keys.

**Expected:** Further files are selected in a linear fashion, completing one row before continuing at the start of the next.

### SELECT-09
In Icon view, select two adjacent files in a row, while holding the Shift key down.  Continue to hold down the Shift key and use the Up and Down Arrow keys.

**Expected:** Further files are selected in a linear fashion, completing one row before continuing at the start of the next. (Not in a rectangular fashion cf rubberbanding).
