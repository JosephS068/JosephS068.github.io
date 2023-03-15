# Particle Systems
Created with another student

### Description:

All of the particles shown use Eulerian integration. 

### Bouncing Ball:
The particle in here is a ball which bounces in 2D. It moves to the right of the screen initially, and eventually come to rest on the right side of the screen.

### Water:
A particle System which is meant to represent water coming out of a bottle. The water arcs and then splashes when it hits the ground. Within this example the user is able to move a wall towards and away from the bottle. This represents the collision the water will have with the wall. Each water particle is textured with a water image. As time goes on the water particle changes colors from dark blue to light blue.  The water particles are translucent and after the initial impact of the splash become more translucent. Because the particles are 2D images, we have them rotate with the camera, which helps create a  3D effect. Water particles are randomly rotated to remove the square look.
Context: Magic potion with endless water.

### Fireworks:
When the screen loads, three different colored ray guns are shown. When the user presses f, a bullet is fired out of one of the guns (moves left to right, then back to left). The bullet will rise in the air for a few seconds then explode. When the explosion occurs the bullet disappears and three rounds of fireworks are seen. A blue firework, then an red, followed slightly after those with an orange one. The particles slowly fade as time go on and are effected by gravity (very mildly). The explosions come from a randomly sampled sphere.
Context: Gun which shoots fireworks.

### Code:
Code: [https://github.com/JosephS068/Processing-Particle-Systems](https://github.com/JosephS068/Processing-Particle-Systems)

Each particle system will run in its own file. 

### Video:
#### Ball:
##### Video One

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Videos/Ball-Screen.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

##### Video Two, Phone

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Videos/Ball-Phone.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Due to lag from recording on laptop, another video from phone is offered to better capture smoothness.

#### Water:

##### Video One

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Videos/Water-1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + 0:00 User controlled camera - translations
    + 0:15 User controlled camera - rotations
    + 0:25 Particles are textured
    + 0:30 Particles are shown to be translucent
    + 0:42 Arc of water is shown, the initial water particles are deeper blue than the later ones
    + 0:50 Zoom out to view splash, as the splash goes on, the particles fade until they fully disappear
    + 1:00 No additional features are shown after this point due to recording error

##### Second Video, Higher Quality

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Videos/Water-2.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + 0:00 User controlled camera - translations
    + 0:25 effects of lights on particles
    + 0:40 Zoom in on individual particle
    + 1:05 User interaction shown, press 'Y' or 'U' to move wall, 
    + 1:10 Water wall interaction

#### Firework:

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Videos/Fireworks.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + 0:00 User controlled camera - translations
    + 0:12 Particle firing from user pressing 'f' key 
    + 0:12 First stage of firework shown
    + 0:12 Shows the 3 layers of firework, with delayed final orange explosion
    + 0:21 Multiple fireworks going off at once
    + 0:21 Particles fade/change color as time goes on

### Benchmarks:
Hardware: Macbook Pro 2017, Intel Iris Plus Graphics (10)

Water: 8000 particles, 33 FPS

Fireworks: 6000 particles, 40 FPS

### Images:
#### Ball:

##### Ball In Air
![Ball in air](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Ball_Images/Ball-Air.png)

##### Ball Stopped
![Ball stopped](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Ball_Images/Ball-Stop.png)

#### Water:
##### Water Particles
![General picture of the particle setting](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-All.png)
##### Bottle Close Up
![Close up of the arc from the bottle](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Bottle.png)
##### Particle ground Interaction
![Up close picture of water particle after it has hit the ground](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Particle-Close.png)
##### Water Splash
![The splash of the water](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Splash.png)
##### Water Wall Collision
![The splash colliding with a wall](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Wall-Splash.png)
##### The splash colliding with a wall, far away
![The splash colliding with a wall, far away](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Wall-Splash-Away.png)
##### Water Wall Direct Contact
![The water flow colliding with a wall](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/Water-Wall-Flow.png)
##### Water Texture
![Texture used for water particles](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Water_Images/water.jpg)

#### Fireworks:
##### Scene
![Initial state of scene](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Firework-Initial.png)
##### Firework Phase 1
![Firework phase 1](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Firework-1.png)
##### Firework Phase 2
![Firework phase 2](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Firework-2.png)
##### Fireworks Multiple Bullets
![Firework with multiple bullets](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Fireworks-Bullets.png)
##### Fireworks Several Explosions
![Firework with several explosions](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Fireworks-Several2.png)
##### Fireworks Bullets And Explosions 
![Firework with several explosions with bullets](https://JosephS068.github.io/Game_Projects/Processing/Particle_Resources/Fireworks_Images/Fireworks-Several.png)
### Tools/Libraries Used:
Processing: [https://processing.org/reference/](https://processing.org/reference/)

Processing's Tutorials: [https://processing.org/tutorials/p3d/](https://processing.org/tutorials/p3d/)

Processing Documentation: [https://processing.org/reference/](https://processing.org/reference/)

Water Texture: [https://www.flickr.com/photos/freefoto/1239764571/in/photostream/](https://www.flickr.com/photos/freefoto/1239764571/in/photostream/)

Bullet: [http://www.aigei.com/s?q=%E5%AD%90%E5%BC%B9&type=3d&term=obj](http://www.aigei.com/s?q=%E5%AD%90%E5%BC%B9&type=3d&term=obj)