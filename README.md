# Itches
--------------

Itches is essentially a Scratch-like language that can be used in the terminal.
Of course, this means commands rather than drag-and-drop, but hopefully 
tab-complete can be implemented.

## Command Ideas

Commands to be structured as `Category.Command(<Argument1> separator text <Argument2>)`.
Separator text can be replaced with a comma (`,`).

### Categories

*	Control	(Control Blocks)
*	Move	(Motion)
*	Look	(Appearance)
*	Variable	(Data - lists covered too)
*	Maths	(Mathematical/Bitwise logical operators)
*	Compare	(Comparison logical operators)
*	Pen	(Drawing)
*	Sense	(Sensing)
*	Sub	(Subroutine blocks)
*	Extended?	(Additional block types for extensions?)
*	etc...

## Tools

Need to create an ANSI/ASCII "image" editor!

## Graphics

"Graphics" will be done with ANSI/ASCII.  There will be multiple logical 
"layers" that will be "flattened" to produce the output.  From bottom to top:

*	Background (Scene)
*	Pen trail
*	Sprites (Z-order is controlled programmatically.)

Spaces with no extended attributes will be interpreted as transparent (outside 
of the background).

### Pen Trail

The first mark made by the pen when it goes down will be a full-stop/dot (`.`).
When the sprite moves with the pen down, the initial mark will be changed 
depending on the direction the sprite moves:

*	Vertical movement = `|`
*	Horizontal movement = `-`
*	Diagonal movement, depending on the direction = `/` or `\`

The new mark will initially be a `.`, which will again change based on any 
movement with the pen down.

