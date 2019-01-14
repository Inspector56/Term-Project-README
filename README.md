# Term-Project-README
Explains how the project at works.

WHAT IS THIS PROJECT?

  This project is a small puzzle game; in particular, it is a First-Person (sort-of) 3D Platformer. The player's goal at any given moment is to ascend higher. To do so, they can move with wasd and can use space to jump on the blocks around them. If you fall off, you will be reset to the last checkpoint. Some of these blocks will appear transparent/as wireframes. This is where the player's gun comes into action. Use 'b' to change the fire mode. Click to fire. In the primary fire mode, you can shoot an existing block to toggle it between its solid and wireframe form. The number of transformed blocks you can have in the world is limited; you can untoggle a transformed block to restore charges.

  The second gun mode is a little more niche; you will see some yellow orbs floating in space. If you collect them, you will permanently gain a charge for your primary fire. To collect these orbs, put your gun in the secondary fire mode and select four cubes from the world such that the path created by visiting each cube in order intersects with the floating orb (as visual feedback, you should see your own yellow orb float through the path once four cubes have been selected).

  To assist you in your upwards journey, you can press 'c' to toggle control of the snake. The snake is the set of gray blocks. When in control of the snake, hold space and press w or s to zoom in or out, respectively. You can click and drag to rotate the view around the snake's head. The snake should show which direction it is facing; move the camera around and used wasd to manipulate the direction it is facing. Once it is facing a wireframe/passable block, press shift to move it forward. Boxes that are part of the snake may not be transformed, but they can be selected for the second fire mode. Similar to collecting the yellow orbs, some boxes may have gray orbs inside of them. When the snake passes into these boxes, it will permanently grow in length. If you get yourself stuck, press 'r' to reverse the snake.

  Finally, you will come across clusters of boxes surrounding red orbs. These have associated "controllers", which appear in the world as small, floating, transparent red cubes. It should change color ("light up") when you are near enough to use it. Press q to make it turn left, e to make it turn right, and f to make it rotate "forwards". Whichever way the box rotates, at least one associated cluster will rotate the same way. Use this to try to create paths. You may find it helpful to know that, if the snake occupies any of the boxes in such a cluster the cluster will be "locked".

  Note that it is fairly easy and straightforward to create your own levels or add to existing ones; all of the details needed to create a level are in the level_info object of the Game_Scene class, which you can modify in the class constructor. When you first load the page you will not be able to move or control the snake; press 'f' when you are ready to begin playing.

CONTRIBUTIONS:

Benjamin Spector:

- created and implemented object design tree/hierarchy
- implemented first-person camera movement, including:
  - vertical and lateral collision with boxes
  - gravity/vertical acceleration -bounded rotation angles
  - implemented snake camera movement and direction controls, and camera switching
- implemented ray-cast picking
- implemented Rubiks objects and their view-and-position-sensitive controllers
- implemented path following/animation and second gun mode
- created/instantiated the level layout for the demo/presentation 

Matthew Horner: 
- Created transparent texture effect for bottom of game environment.
  - Attempted to mimick volume rendering. 
- Designed custom arrow shape using tiny-graphics' surface of revolution tool. 

Matthew Paterno:

- Designed textured cube object with varying textures on each side.
- Designed and implemented infinite skybox object/class.
  - Skybox position based on player camera.
- Designed and implemented gun object/class.
  - Textures, display based on gun mode, varying values.
  - Timeout animations on button clicks.

Matei Lupu

- Created one of the versions of gravity/vertical acceleration that was tested for the project but was not used in the final product.
- Implemented camera movement and made it seem more natural by doing things such as limiting movement in the y-direction to appear more human-like. 
- Implemented sound effects for events such as character jumps, fire-mode switch and for the actual firing of the snake/gun
- Created and Implemented crosshairs shape to represent the current aim/selection of the snake/gun

HOW TO RUN:

While dependencies has been modified, we used an unmodified version of tiny_graphics. Once all you have all of these files in your directory, simply use host.bat or host.command and use Google Chrome to go to the indicated localhost address, just as you would for any of the previous assignments in this course.

SPECIAL NOTE:
If you're seeing that most of the commits are from Benjamin Spector, well, while I probably did have the most commits, this is mostly a reflection of the fact that for the duration of the project I was not pulling before pushing, and because Git remains a very flawed and needlessly confusing API, was unwitting, not only overwriting things and erasing files and changes in the repository, but actually erasing other people's previous commits from the commit history. Somehow. One might imagine that that's the sort of thing you'd want to warn the user before doing, or perhaps even just not allow the user to do at all. Nonetheless, take that bit of foolishness on my part into consideration.

