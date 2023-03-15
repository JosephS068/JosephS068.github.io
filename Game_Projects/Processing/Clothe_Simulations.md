# Cloth Simulation
Created with another student.

### Description:
All of the systems shown use Eulerian integration except the comparison between midpoint and eulerian integrator. 

#### Thread:
The video shows several threads. Each thread contains a masses connected to one another with a spring. In the video you will see that the upper most spring is stretched the farthest. If a mass connects with the floor it will bounce backwards. We do not have collisions between masses. Collision only occurs between the floor and masses.

#### General Cloth:
First a cloth is shown interacting a ball which is controlled by the user. The simulation is then changed to have the cloth interact with a cube which is controlled by the user. Wind is added and the cloth falls onto the cube and eventually blows away. 

#### Drag Terms and Midpoint:
**Part One:**

First a cloth with drag is shown interacting with a ball. The drag is then removed from the cloth simulation and the results are shown with its interaction with the ball. 

**Part Two:**

The video then shows the cloth from the start, but now using the midpoint method instead of eulerian. The simulation becomes much slower when we switch to the midpoint method. The cloth is then set back to eulerian and put in an unstable state by changing parameters. Finally the cloth is put again in midpoint, which works, this shows midpoint being more stable than eulerian. 

#### Cloth Tear:
**First Video:** At the start camera controls are shown, 3D rendering of the context is shown. At the start the cloth is cut partially, because of the extra force on the uncut part of the cloth, it tears. The cloth is then cleanly cut. The sword is controlled by the user and the user is free to cut the cloth how they desire. 

**Second Video:** Camera controls are further demonstrated by traversing the setting. The cloth is then cut, but not as much as the first video to show that the cloth does not always tear.

#### Skip Nodes:
Initially a normal cloth is shown blowing in the wind until it falls from the force. The video then shows the same cloth, but now with additional springs which skip over nodes. This shows the stiffness in both when blowing in the wind and when it falls to the ground. 

#### 1D-Water:
 We see a water in 1D which is simulated between two pillars. When water is removed or added we can see that eventually the water will even out. The user is able to add and remove water at will to see its effects. There is a shark which floats on top of the water. There is a treasure hidden behind the water which is only seen by lowering the water(no in video).

### Code:
All of the code can be found here: [https://github.com/JosephS068/Processing-Cloth-Simulation](https://github.com/JosephS068/Processing-Cloth-Simulation)
### Video:
#### Threads

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Thread.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

Velocity is randomized for each mass at the beginning.

#### General Cloth

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Cloth-Cube-Sphere.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (0:00) 2D Mass-spring cloth simulation (Cloth interacts in 3D, including 2D)
    + (0:00) 3D Mass-spring cloth simulation
    + (0:05) One way cloth interaction (Sphere) Please note the disco ball rotating is purely cosmetic, the collision is treated as if it was a stationary sphere.
    + (0:35) One way cloth interaction (Square)
    + (0:00) Textured cloth

#### Drag Terms and Midpoint

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Comparison.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

 * Features:
    + (0:00) Drag terms, initially cloth has drag, (0:37) then no drag is applied
    + (0:00) Eulerian initially used by the cloth
    + (1:20) Midpoint
    + (Below) Integration method comparisons

 * **Comparison Between Integration Methods**
    + (0:00) Eulerian initial
    + (1:20) Midpoint initial
    + (1:40) Eulerian broken
    + (1:55) Midpoint not broken

First when we started the midpoint algorithm(1:20) we had a slower framerate than eulerian(0:00). When the time step was increased the eulerian was shown to be unstable(1:40) while the midpoint method worked(1:55).

#### Tear-able Cloth
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Cloth-Tear-1.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Cloth-Tear-2.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

* Features:
    + (1) (0:00) Realtime Rendering
    + (1) (0:11) Real-time user interaction with system
    + (1) (0:12) Tear-able cloth
    + (2) (0:00) 3D Rendering with user-controlled camera

**First Video:**

The cloth is cut in this video twice, once partially to show the rest of the cloth rip, then finally all the way through. The sword is controlled by the user.

If you are using the cloth tear file, you may have to restart it a few times as rocks may generate where the flag is.

**Second Video:**

Camera controls are shown off. The cloth is cut, but not enough is cut for it to pull apart.

#### Skip Nodes
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/Node-Skip.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

 * Features:
    + (0:03) Billowing/blowing effect
    + (0:35) skip nodes comparison

The first cloth shown does not have extra springs attached. Wind is added to create a blowing effect. This effect is used to show the difference between a regular cloth and a cloth with additional springs. The video then shows a cloth with additional skip springs and how it is stiffer. 

#### 1D Water
<video width="480" height="360" controls>
  <source src="https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Videos/1D-Water.mp4" type="video/mp4">
Your browser does not support the video tag.
</video>

 * Features:
    + (0:00) 1D Water surface, shallow water equation

Height is added and taken away from the water throughout the video, the user can add and remove water and this causes the waves. 

### Benchmarks:
15x15 cloth, 20 FPS

20x20 cloth 30 FPS

30x30 cloth 30 FPS

Processor: Intel i7-9750H

### Images:
#### Threads
##### Thread In Motion
![Thread In Motion](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Thread_Images/thread-motion.png)

##### Thread At Rest
![Thread At Rest](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Thread_Images/thread-rest.png)

#### Cloth
##### Cloth Scene Update Ball Interaction
![Cloth Scene Update Ball Interaction](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Cloth_Images/Ball-Interaction.png)
##### Cloth Scene Update No Interaction
![Cloth Scene Update Ball Interaction](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Cloth_Images/Ball-No-Interaction.png)
##### Cloth Normal
![Cloth Normal](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Cloth_Images/Cloth-Normal.png)
##### Cloth Cut
![Cloth Cut](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Cloth_Images/Cloth-Cut.png)
##### Cloth Clean Cut
![Cloth Clean Cut](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Cloth_Images/Cloth-Clean-Cut.png)

#### Water
##### Water High
![Water High](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Water_Images/Water-High.png)
##### Super Secret
![Super Secret](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Water_Images/Water-Secret.png)
##### Motion
![Motion](https://JosephS068.github.io/Game_Projects/Processing/Cloth_Resources/Water_Images/Water-Motion.png)
### Tools/Libraries Used:
Processing
Minim - for audio playing in processing

### Other Resources Used:
General information:[https://processing.org/reference/](https://processing.org/reference/)

How to play music:[https://stackoverflow.com/questions/11822144/processing-how-to-add-background-music ](https://stackoverflow.com/questions/11822144/processing-how-to-add-background-music )

How to texture cloth: [https://www.youtube.com/watch?v=FeXnJSCFj-Q](https://www.youtube.com/watch?v=FeXnJSCFj-Q)
