<h1 align="center">Blockscaper Add-on<br></h1>
<h3 align="center">Professional building tools for Minecraft: Bedrock<br></h3>

<p align="center"><img src="https://user-images.githubusercontent.com/37005439/197584478-619d3376-0bf4-466d-b891-dfe9783450c7.png" width="320" alt="Blockscaper Tinkrew Logo"></img></p>

<h4 align="center">Developed by Ian Senne + Tinkrew<br></h4>

<p align="center">Report a bug on the <img src="https://user-images.githubusercontent.com/37005439/197581354-74c4a4f4-5b89-4aec-8e13-3e2a22180000.png" width="16" alt="Bug Tracker Icon"></img> <a href="https://github.com/Tinkrew/blockscaper/issues/new">Bug Tracker</a></p>

<h1 align="center">Quick Start Guide<br></h1>

## 1. Installation

-  Download the ![downloadicon](https://user-images.githubusercontent.com/37005439/197565238-ca154dac-2a71-4742-9e47-77b8a28d01b9.png) [Blockscaper Add-on](https://github.com/Tinkrew/blockscaper/releases/latest/download/Blockscaper_Example_File.mcaddon)

-  Install Blockscaper by opening the downloaded file using Minecraft

## 2. Adding Blockscaper to your world

-  Enable the `GameTest Framework` experimental feature

   Note: this may make a copy of your world if you have not enabled experimental features before
   
-  Activate the Blockscaper behavior pack

-  Opening the world should now greet you with a message letting you know Blockscaper is enabled

## 3. In-game

-  You can run `!items` in game to get all the Blockscaper items

-  All commands in Blockscaper start with just one exclamation mark `!forexample`

-  If you are familiar with Java World Edit, the commands should be similar otherwise you can learn more about them below

<h1 align="center">Command Library<br></h1>

## !debug
No help information specified.

`debug blocks`

## !docs-gen
No help information specified.

`docs-gen`

## !items
Get all the Blockscaper items!

`items`

## !undo
Undoes your past actions.

`undo`,
`undo <count: Number>`

## !pos1
Aliases: `p1`

Sets the corresponding corner of your selection box.

`pos1`,
`pos1 <position: Position>`

## !pos2
Aliases: `p2`

Sets the corresponding corner of your selection box.

`pos2`,
`pos2 <position: Position>`

## !set
Fills your selection with a given input.

`set <blocks: ExtendedBlock>`

#### Argument Information:

#simplex(sx, sy, sz) <entries> - sx, sy, sz are numbers representing scales on thier respective axis.

-  Example: #simplex(0.1,0.1,0.1) 5%dirt,10%glass,5%granite
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !blockinfo
Aliases: `block`, `bi`
   
Get information about a block, such as block states.
   
`blockinfo <block: String>`

## !replace
Replace blocks in your selection.
   
`replace <from: Block> <to: Block>`,
`replace <to: Block>`
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !wand
Get your very own wand!
   
`wand`

## !mask
Applies a mask to your currently equipped brush.
   
`mask clear`,
`mask add <mask: Mask>`,
`mask remove <id: Number>`
   
#### Argument Information:
   
#### Mask Format:
   
-  !blocks   -> is not <blocks>  
-  =blocks  -> is <blocks>
-  N>blocks -> N blocks above <blocks>  
-  N<blocks -> N blocks below <blocks>

## !gmask
Applies a mask to everything.
   
`gmask`,
`gmask <mask: Mask>`
   
#### Argument Information:
   
#### Mask Format:
   
-  !blocks   -> is not <blocks>
-  =blocks  -> is <blocks>
-  N>blocks -> N blocks above <blocks>
-  N<blocks -> N blocks below <blocks>

## !br
Assign a brush to the currently selected item.
   
`br sphere <material: Block> <radius: Number>`,
`br cube <material: Block> <size: Number>`,
`br cyl <material: Block> <radius: Number> <height: Number>`,
`br paste`
   
#### Flags
   
 `-a` 
Ignores air blocks.
   
 `-h` 
Makes a shape hollow.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !queue
Shows the command queue.
   
`queue`

## !history
Prints your past command usage.
   
`history`

## !copy
Copies your selection to your clipboard.
   
`copy`
   
#### Flags
   
 `-c` 
Sets the origin of your clipboard to the center of the region, at the region's lowest y-level.

## !paste
Pastes the contents of your clipboard into the world.
   
`paste`
   
#### Flags
   
 `-a` 
Ignores air blocks.
   
 `-s` 
Selects the region after pasting.
   
 `-n` 
Similar to the "-s" flag, but does not paste the clipboard's contents.
   
 `-o` 
Pastes at the origin of your clipboard.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !help
Get help with commands.
   
`help`,
`help <page: Number>`,
`help <command: String>`

## !sphere
Makes a sphere in the world.
   
`sphere <block: Block> <radius: Number>`
   
#### Flags
   
 `-h` 
Makes a shape hollow.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !cyl
Makes a cylinder in the world.
   
`cyl <block: Block> <radius: Number>`,
`cyl <block: Block> <radius: Number> <height: Number>`
   
#### Flags
   
 `-h` 
Makes a shape hollow.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !pyramid
Makes a pyramid in the world.
   
`pyramid <block: Block> <width: Number>`
   
#### Flags
   
 `-h` 
Makes a shape hollow.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !cut
Cuts your selection to your clipboard, filling the selected region with air.
   
`cut`
   
#### Flags
   
 `-c` 
Sets the origin of your clipboard to the center of the region, at the region's lowest y-level.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !stack
Repeats your selection a number of times.
   
`stack <count: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z->`
   
#### Flags
   
 `-s` 
Shifts the selection to the last stacked copy.
   
 `-a` 
Ignores air blocks.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !asc
Move up to the next solid block.
   
`asc`

## !desc
Move down to the next solid block.
   
`desc`

## !up
Move vertically a certain number of blocks.
   
`up <distance: Number>`

## !move
move the contents of your selection
   
`move <distance: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z-> <replace: Block>`,

`move <distance: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z->`,

`move <offset: Position> <replace: Block>`,
`move <offset: Position>`
   
#### Flags

 `-s` 
Shifts your selection to the target location.
   
 `-a` 
Ignores air blocks.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !rotate
Rotates the contents of your clipboard.
   
`rotate <degrees: Number>`

## !fill
fill a hole.
   
`fill <block: Block> <radius: Number> <depth: Number>`,
`fill <block: Block> <radius: Number>`
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !drain
Clear out a volume of water and lava.
   
`drain <radius: Number>`
   
#### Flags
   
 `-p` 
Removes water plants.
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !fillr
Fills a hole, recursively.
   
`fillr <block: Block> <radius: Number> <depth: Number>`,
`fillr <block: Block> <radius: Number>`
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !cancel
Cancels a number of your queued actions.
   
`cancel`
`cancel <count: Number>`

## !tr
Replaces blocks in your selection by type.
   
`tr list`,
`tr list <type: String>`,
`tr <from: Type> <to: Type>`
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !expand
Increases the size of your selection box.
   
`expand <direction: up, down, north, south, east, west, all> <amount: Number>`

## !walls
Places a wall around your selection.
   
`walls <blocks: Block>`
   
#### Flags
   
 `-u` 
Marks this action as unsafe by not recording an undo.

## !flip
Flips the contents of your clipboard across an axis.
   
`flip <axis: north, south, east, west, up, down>`

## !shift
Moves your selection box without affecting its contents.
   
`shift <direction: up, down, north, south, east, west, all> <amount: Number>`

## !contract
Reduces the size of your selection box.
   
`contract <direction: up, down, north, south, east, west, all> <amount: Number>`

## !thru
Move forward to the next solid block.
   
`thru`
   
