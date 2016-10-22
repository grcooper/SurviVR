# SurviVR

This repo is here for some practice in VR and procedural generation of worlds. Idealy we would like to create a survival game in VR for the cardboard (and in future iterations the oculus or vive).
This initially came from the repo: https://github.com/thadeaus/ProceduralGeneration however that was more of a sandbox and this is going to be more of an actual game

# Building and Playing

## For phone
* Set up your phone with developer mode and USB debugging enabled
* Attach phone to computer and click
	* File -> Build & Run
	* Build For android
	* Make sure the main scene (or scene you want to test) is selected
	* Click build and run
	* tap screen to move, turn head to change directions

## For Computer
* Open the scene you want
* Click the play button
* Click to move
* Hold ALT + Move mouse to look in the direction you want
* You can always switch to scene mode while playing to view the scene and move using regular unity controls
# Middle mouse click re-generates the world - this make take some time. 

# Contributing

* Please feel free to make PRs as needed. You will need to get unity from https://unity3d.com/
* When creating something for a scene, please create a new scene to test it out and add instructions on how to add it to the main game.

## Island Generator

There are a series of things in the Island Generator that allow you change how the island is viewed. All of these numbers can be updated in real time while playing the game. Values changed while in Play Mode WILL NOT SAVE.

`Land MF` - Leave this as is

`Render Distance` - Distance in game that new objects will be instantiated. Make this smaller if you want higher FPS

`Width` - Width of the island

`Height` - Height of the island

`World Scale` - Scale relative to the player. Making this smaller makes the island a lot smaller, but no longer has lots of open plains.

`Perlin Scale` - The size of the perlin map we are using,  higher makes the island more flat

`HScale` - also controls the scaling on the height component of the island

`Seed`/`Use random Seed` - Change this to have random seeds, for testing it is good to keep use random seed off, and using the same seed to see incremental changes.

`Smooth Iterations` - Number of times the smoothing algorithm is run. The higher this is, the fewer small patchs of biomes will be seen.

`Border Size` Currently I have a border around the island for the beach, this is the size of that beach border

`Type Percents` - This is still needed, but doesn't do as exactly as stated. It is a mapping to the Terrain type enum and allows you to change the amount of different types of terrain.

`Round Number` - To give the world more of a poly feield, and avoid constant curves in the terrain, this rounds heights to a multiple of this number.

`Environment Scale` - Scales the trees and rocks or other environmental objects placed in the future

`Tree Prefabs` - The different trees placed on the island randomly selected

`Stone Prefabs` - The different stones placed on the island randomly selected

`Player move render distance` - Every time the player moves this distance we check if objects are inside of the `Render Distance` and update if they can be seen

## Systems we would like to have implemented:
(in no particular order)

* Better world generation (more interesting)
* Crafting system
* Resource systems (health, hunger, energy etc)
* Inventory system
* AI's (enemies or friendlies to give the world a more lively feeling)
* Eventually multiplayer would be great...


## Playing around with procedural generation in Unity

![Alt text](/procgen1.png?raw=true "Most Recent Iteration - July 11th 2016")

![Alt text](/procgenisland.jpg?raw=true "First view of perlin noise being used - Feb. 2016")
