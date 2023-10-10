# Description:
A simple first person shooter made in processing. 

# Final Report 
[Report Here](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/FPS-Report.pdf)

# Project Presentation:
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Game-Presentation-SHORT-VERSION.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

# Longer Presentation:
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Game-Presentation.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Originally, I thought the presentation had to be 3 minutes. Here is the longer version, it had additional slides and talks briefly about the particle effects.

# Controls:
wasd - movement<br />
arrow - looking<br />
/ - shoot<br />
space - jump<br />
l - quit<br />
m - change to mouse controls<br />
r - reload<br />

# Code:
The code for this project can be found here: [https://github.com/JosephS068/Processing-First-Person-Shooter](https://github.com/JosephS068/Processing-First-Person-Shooter)

Known ISSUES:

There are two minor problems with the game's presentation, firstly, the audio can lag, this only occurred on my machine while other applications were running, like a web browser. 

Secondly on the win/death screen the text can become cut off, cause unknown, likely clipping into obstacles. 

# Videos:
### Play Through
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Play-Through.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Video shows:
    + Entire play through of level
    + Obstacle collisions
    + epsilon A* boss fight
    + Collision with box obstacles
    + Boid enemy
    + Bullet detection by entities
    + Player interaction with Doors

### Target Collision Problems
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Target-Poor-Collision.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

 * Video shows:
    + The hit boxes in this game are all spheres, so you can shoot in front of targets and still hit them. 
    + Bullets move through obstacles/other entities, multiple targets can be hit with one bullet.

### Collisions
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Collision-Showcase.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Video shows:
    + Player interacting with pipe collision(Cylinder Obstacle).
    + Wall collision(Quad Obstacle).
    + Box Collision(Rectangle Obstacle)
    + Player escaping the map, as geometry allows it. 

### Boss Mapping Displayed

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/Boss-Path.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Video shows:
    + The random points the boss can move to and how the goal(player position), is changed when the boss creates a new plan. 

### Play Through With Audio (Phone Camera)

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/FPS-Audio-1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Videos/FPS-Audio-2.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Video shows:
    + I was unable to record audio with my software on my laptop. A phone video is taken to provide a general overview of the audio present in game. 

# Images
## Target Area
### Pipe With Collision
![Pipe With Collision](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/pip.png)

### Player Firing, Hitting Target
![Player Firing, Hitting Target](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/target-shot.png)

### All Targets Cleared
![All Targets Cleared](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/target-reload.png)

### No Targets Hit
![No Targets Hit](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/Target.png)

## Boss Fight
### Boss' Traps
![Boss' Traps](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/boss-traps.png)

### Boss' Shield Up
![](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/boss-shield.png)

### Boss Dead
![Boss Dead](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/boss-dead.png)

### Boss Following Player
![Boss Following Player](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/boss.png)

### Death Screen
![Death Screen](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/Death.png)

### Obstacle Course
![Obstacle Course](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/obstacle-1.png)

### Final Corridor
![Final Corridor](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/obstacle-2.png)

### Player Shooting Enemy, In Final Elevator
![Player Shooting Enemy, In Final Elevator](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/obstacle-3.png)

### Corridor Empty
![Corridor Empty](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/parasite-hallway.png)

### Win Screen Glitch
![Win Screen Glitch](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/win.png)

# Maps For Level Creation
Below are the maps I used while programming the level, it was used to help figure out each obstacle's coordinates, as well as provide the ground work of the level's layout. It's primary use was keeping track of how Z axis and X axis were positioned. I gave every wall an id, which allowed for quick map creation. Finally when coloring floors/ceilings the below maps are used

![Maps For Level Creation](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/map.jpg)
![Maps For Level Creation 2](https://JosephS068.github.io/Game_Projects/Processing/FPS_Resources/Images/map-3.jpg)
# Benchmarks:
Though FPS bench marks were not taken, an exported version of this game was played on a Mac Book running windows. Which was found to have a large decrease in performance compared to my Acer laptop. I made this note, because the Acer laptop used to develop this game was weaker than the Mac Book. To improve performance on all machines, parts of the level is removed from collision check after passing a certain section. Additionally, short audio clips are loaded in memory at the start up.

# Tools/Libraries Used:
Processing: [https://processing.org/](https://processing.org/)<br />
Minim: [http://code.compartmental.net/minim/](http://code.compartmental.net/minim/)<br />
Audacity: [https://www.audacityteam.org](https://www.audacityteam.org)

FPS Camera:<br />
While no code was directly used from the following source, it was helpful in understanding a working first person camera.
[https://forum.processing.org/one/topic/1st-person-perspective.html](https://forum.processing.org/one/topic/1st-person-perspective.html)

Mouse Controls:<br />
No code directly used, but information helped develop mouse controls. <br />
[https://processing.org/discourse/beta/num_1226167144.html#4](https://processing.org/discourse/beta/num_1226167144.html#4)<br />
[https://stackoverflow.com/questions/1439022/get-mouse-position](https://stackoverflow.com/questions/1439022/get-mouse-position)

Exporting Application:<br />
[https://stackoverflow.com/questions/11832342/processing-exported-applet-not-working](https://stackoverflow.com/questions/11832342/processing-exported-applet-not-working)

When using audio library, had lag issue and null pointers. Following post helped fix that issue.<br />
[https://github.com/ddf/Minim/issues/45](https://github.com/ddf/Minim/issues/45)

##### Music:
All music in this game was produced by a Friend.

##### Play Testing:
A Friend

##### Voices:
Hurt/Death sound effects by A Friend<br />
General/Sergeant U.S.A by a Friend<br />

Icons:<br />
Cross Hair:  [https://image.flaticon.com/icons/png/512/59/59325.png](https://image.flaticon.com/icons/png/512/59/59325.png)<br />
Ammo: [https://image.flaticon.com/icons/png/512/225/225814.png](https://image.flaticon.com/icons/png/512/225/225814.png)<br />
Heart: [https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fgetdrawings.com%2Ffree-icon-bw%2Fheart-icon-transparent-background-22.png&f=1&nofb=1](https://external-content.duckduckgo.com/iu/?u=http%3A%2F%2Fgetdrawings.com%2Ffree-icon-bw%2Fheart-icon-transparent-background-22.png&f=1&nofb=1)<br />

Sound Effects:<br />
GunShot: [http://soundbible.com/2120-9mm-Gunshot.html](http://soundbible.com/2120-9mm-Gunshot.html)<br />
Reload: [http://soundbible.com/1959-Shotgun-Reload-Pump.html](http://soundbible.com/1959-Shotgun-Reload-Pump.html)<br />
Footsteps: [http://www.orangefreesounds.com/walking-footsteps-on-metal-surface/](http://www.orangefreesounds.com/walking-footsteps-on-metal-surface/)<br />
Explosion: [http://www.orangefreesounds.com/explosion-sound-effect/](http://www.orangefreesounds.com/explosion-sound-effect/)<br />
Door Open: [http://www.orangefreesounds.com/metro-door-open-sound/](http://www.orangefreesounds.com/metro-door-open-sound/)<br />
Robot Hurt 1: [http://soundbible.com/906-Drop-Sword.html](http://soundbible.com/906-Drop-Sword.html)<br />
Robot Hurt 2: [http://www.orangefreesounds.com/crash-sound-effect/](http://www.orangefreesounds.com/crash-sound-effect/)<br />
Robot Hurt 3: [http://www.orangefreesounds.com/metal-door-closing-sound-effect/](http://www.orangefreesounds.com/metal-door-closing-sound-effect/)<br />
Trap Place: [http://www.orangefreesounds.com/footstep-single-ice/](http://www.orangefreesounds.com/footstep-single-ice/)<br />
Sword Spin: [http://www.orangefreesounds.com/fan-sound-effect/](http://www.orangefreesounds.com/fan-sound-effect/)<br />
Bullet Deflect: [http://soundbible.com/1464-Western-Ricochet.html](http://soundbible.com/1464-Western-Ricochet.html)<br />
Target Hit: [http://soundbible.com/1781-Metal-Clang.html](http://soundbible.com/1781-Metal-Clang.html)<br />
Teleport: [http://soundbible.com/1885-Martian-Death-Ray.html](http://soundbible.com/1885-Martian-Death-Ray.html)<br />
Trap Closed: [http://soundbible.com/1104-Metal-Clank-Wobble.html](http://soundbible.com/1104-Metal-Clank-Wobble.html)<br />

Textures:<br />
Metal Floor: [https://www.pinterest.com/pin/123075002294687146/](https://www.pinterest.com/pin/123075002294687146/)

