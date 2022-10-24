<h1 align="center">Blockscaper Add-on</h1>

<h3 align="center">Professional building tools for Minecraft: Bedrock</h3>
<p align="center">One add-on. Any device. Multiplayer and singleplayer.<br>Production ready (with caution). Compatible with custom blocks.<br>And completely free.</p>

<p align="center"><img src="https://user-images.githubusercontent.com/37005439/197636783-97724f70-8f63-4c19-aefb-ce59d149a6b3.png" width="640" alt="Blockscaper Tinkrew Logo"></img></p>

<p align="center">Developed by Ian Senne for Tinkrew</p>

<p align="center">Report a bug on the <img src="https://user-images.githubusercontent.com/37005439/197584800-59e5483e-fcdf-4641-9e79-28549b469047.png" width="16" alt="Bug Tracker Icon"></img> <a href="https://github.com/Tinkrew/blockscaper/issues/new">Bug Tracker</a> or suggest a feature!</p><br>

<img src="https://user-images.githubusercontent.com/37005439/197627238-62ca0c7c-9fb6-4bef-b485-c4d25f022b01.png" width="50"></img>

<p align="center"><a href="https://github.com/Tinkrew/blockscaper/releases/latest/download/Blockscaper_Example_File.mcaddon"><img src="https://user-images.githubusercontent.com/37005439/197631531-049c96b3-2f76-44a2-a5d5-60e7548f2a19.png" width="320"></a></img></p>
<p align="center">Latest release Oct 24, 2022<br>Blockscaper v1.0.0 for Minecraft Bedrock v1.19.31</p4>

<img src="https://user-images.githubusercontent.com/37005439/197627238-62ca0c7c-9fb6-4bef-b485-c4d25f022b01.png" width="50"></img>

<h1 align="center">Quick Start Guide<br></h1>

<h3>1. Installation</h3>

-  Download the ![downloadicon](https://user-images.githubusercontent.com/37005439/197565238-ca154dac-2a71-4742-9e47-77b8a28d01b9.png) [Blockscaper Add-on](https://github.com/Tinkrew/blockscaper/releases/latest/download/Blockscaper_Example_File.mcaddon)
-  Install Blockscaper by opening the downloaded file using [Minecraft](https://minecraft.net/)

<h3>2. Adding Blockscaper to your world</h3>

-  Enable the `GameTest Framework` experimental feature <br>   <i>Note: this may make a copy of your world if you have not enabled experimental features before</i>
-  Activate the Blockscaper behavior pack
-  Opening the world should now greet you with a message letting you know Blockscaper is enabled

<h3>3. In-game</h3>

-  You can run `!items` in game to get all the Blockscaper items
-  All commands in Blockscaper start with just one exclamation mark `!forexample`
-  If you are familiar with Java World Edit, the commands should be similar otherwise you can learn more about them below

<img src="https://user-images.githubusercontent.com/37005439/197627238-62ca0c7c-9fb6-4bef-b485-c4d25f022b01.png" width="50"></img>

<h1 align="center">Index</h1>

<table align="center">
   <tr>
      <td>items</td>
      <td>undo</td>
      <td>pos1</td>
      <td>pos2</td>
      <td>set</td>
      <td>blockinfo</td>
      <td>replace</td>
      <td>wand</td>
      <td>mask</td>
      <td>gmask</td>
   </tr>
   <tr>
      <td>br</td>
      <td>queue</td>
      <td>history</td>
      <td>copy</td>
      <td>paste</td>
      <td>help</td>
      <td>sphere</td>
      <td>cyl</td>
      <td>pyramid</td>
      <td>cut</td>
   </tr>
   <tr>     
      <td>stack</td>
      <td>asc</td>
      <td>desc</td>
      <td>up</td>
      <td>move</td>
      <td>rotate</td>
      <td>fill</td>
      <td>drain</td>
      <td>fillr</td>
      <td>cancel</td>
   </tr>
   <tr>
      <td>tr</td>
      <td>expand</td>
      <td>walls</td>
      <td>flip</td>
      <td>shift</td>
      <td>contract</td>
      <td>thru</td>
      <td></td>
      <td></td>
      <td></td>
   </tr>
</table>

<img src="https://user-images.githubusercontent.com/37005439/197627238-62ca0c7c-9fb6-4bef-b485-c4d25f022b01.png" width="50"></img>

<h1 align="center">Command Library</h1>
<p align="center">Documentation updated Oct 24, 2022</p>

## !items
Get all the Blockscaper items!

`items`

## !undo
Undoes your past actions.

`undo`, `undo <count: Number>`

## !pos1
<i>Aliases:</i> `p1`<br>Sets the corresponding corner of your selection box.

`pos1`, `pos1 <position: Position>`

## !pos2
<i>Aliases:</i> `p2`<br>Sets the corresponding corner of your selection box.

`pos2`, `pos2 <position: Position>`

## !set
Fills your selection with a given input.

`set <blocks: ExtendedBlock>`
#### Simplex Implementation:
💡 `set #simplex(dx,dy,dz) <to: Block>`<br>Simplex patterns are enabled in this command. Create 3D noise with custom scaling and weights.

`(dx,dy,dz)` → three dimensional scaling, there are no numerical limits but values typically range from 0 to 1<br><i>Example: (0.5,0.1,0.1)</i>

`<to: Block>` → the pattern used in the simplex, you can use percentages to weight values.<br><i>Examples: 5%dirt,10%glass,5%granite</i>
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.

## !blockinfo
<i>Aliases:</i> `block`, `bi`<br>Get information about a block, such as block states.
   
`blockinfo <block: String>`

## !replace
Replace blocks in your selection.
   
`replace <from: Block> <to: Block>`, `replace <to: Block>`
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.

## !wand
Get your very own wand!
   
`wand`

## !mask
Applies a mask to your currently equipped brush.
   
`mask clear`, `mask add <mask: Mask>`, `mask remove <id: Number>`
#### Mask Format:
`!`blocks → everything except the specified `blocks`<br>`=`blocks → only the specified `blocks`<br><i>x</i>`>`blocks → <i>x</i> blocks above the specified `blocks`<br><i>x</i>`<`blocks → <i>x</i> blocks below the specified `blocks`

## !gmask
Applies a mask to everything.
   
`gmask`, `gmask <mask: Mask>`
#### Mask Format:
`!`blocks → everything except the specified `blocks`<br>`=`blocks → only the specified `blocks`<br><i>x</i>`>`blocks → <i>x</i> blocks above the specified `blocks`<br><i>x</i>`<`blocks → <i>x</i> blocks below the specified `blocks`

## !br
Assign a brush to the currently selected item.
   
`br sphere <material: Block> <radius: Number>`, `br cube <material: Block> <size: Number>`, `br cyl <material: Block> <radius: Number> <height: Number>`, `br paste`
#### Flags:
`-a` Ignores air blocks.<br>`-h` Makes a shape hollow.<br>`-u` Marks this action as unsafe by not recording an undo.

## !queue
Shows the command queue.
   
`queue`

## !history
Prints your past command usage.
   
`history`

## !copy
Copies your selection to your clipboard.
   
`copy`
#### Flags:
`-c` Sets the origin of your clipboard to the center of the region, at the region's lowest y-level.

## !paste
Pastes the contents of your clipboard into the world.
   
`paste`
#### Flags:
`-a` Ignores air blocks.<br>`-s` Selects the region after pasting.<br>`-n` Similar to the "-s" flag, but does not paste the clipboard's contents.<br>`-o` Pastes at the origin of your clipboard.<br>`-u` Marks this action as unsafe by not recording an undo.

## !help
Get help with commands.
   
`help`, `help <page: Number>`, `help <command: String>`

## !sphere
Makes a sphere in the world.
   
`sphere <block: Block> <radius: Number>`
#### Flags:
`-h` Makes a shape hollow.<br>`-u` Marks this action as unsafe by not recording an undo.

## !cyl
Makes a cylinder in the world.
   
`cyl <block: Block> <radius: Number>`, `cyl <block: Block> <radius: Number> <height: Number>`
#### Flags:
`-h` Makes a shape hollow.<br>`-u` Marks this action as unsafe by not recording an undo.

## !pyramid
Makes a pyramid in the world.
   
`pyramid <block: Block> <width: Number>`
#### Flags:
`-h` Makes a shape hollow.<br>`-u` Marks this action as unsafe by not recording an undo.

## !cut
Cuts your selection to your clipboard, filling the selected region with air.
   
`cut`
#### Flags:
`-c` Sets the origin of your clipboard to the center of the region, at the region's lowest y-level.<br>`-u` Marks this action as unsafe by not recording an undo.

## !stack
Repeats your selection a number of times.
   
`stack <count: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z->`
#### Flags:
`-s` Shifts the selection to the last stacked copy.<br>`-a` Ignores air blocks.<br>`-u` Marks this action as unsafe by not recording an undo.

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
Move the contents of your selection.
   
`move <distance: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z-> <replace: Block>`, `move <distance: Number> <direction: north, south, east, west, up, down, x+, x-, y+, y-, z+, z->`, `move <offset: Position> <replace: Block>`, `move <offset: Position>`
#### Flags:
`-s` Shifts your selection to the target location.<br>`-a` Ignores air blocks.<br>`-u` Marks this action as unsafe by not recording an undo.

## !rotate
Rotates the contents of your clipboard.
   
`rotate <degrees: Number>`

## !fill
Fill a hole.
   
`fill <block: Block> <radius: Number> <depth: Number>`, `fill <block: Block> <radius: Number>`
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.

## !drain
Clear out a volume of water and lava.
   
`drain <radius: Number>`
#### Flags:
`-p` Removes water plants.<br>`-u` Marks this action as unsafe by not recording an undo.

## !fillr
Fills a hole, recursively.
   
`fillr <block: Block> <radius: Number> <depth: Number>`, `fillr <block: Block> <radius: Number>` 
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.

## !cancel
Cancels a number of your queued actions.
   
`cancel`, `cancel <count: Number>`

## !tr
Replaces blocks in your selection by type.
   
`tr list`, `tr list <type: String>`, `tr <from: Type> <to: Type>`
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.
   
## !expand
Increases the size of your selection box.
   
`expand <direction: up, down, north, south, east, west, all> <amount: Number>`

## !walls
Places a wall around your selection.
   
`walls <blocks: Block>`
#### Flags:
`-u` Marks this action as unsafe by not recording an undo.

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
   
