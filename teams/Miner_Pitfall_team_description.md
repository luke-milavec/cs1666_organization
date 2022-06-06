# Miner Pitfall

## Canonical game repo URL:

[Miner Pitfall Github URL](https://github.com/CS1666-Miner-Pitfall-2022)

## Team Members
* Advanced Topic Subteam 1: PROCEDURAL GENERATION

	* LANDIN O'NEILL
		* Pitt Username: lao42
		* Github Username: lao42
	* YINUO LI
		* Pitt Username: yil201
		* Github Username: yil201
	* MATT TREZZA
		* Pitt Username: mat271
		* Github Username: trezzamatt
	* LUCAS MILAVEC
		* Pitt Username: lrm88
		* Github Username: luke-milavec

* Advanced Topic Subteam 2: PHYSICS SIMULATION

	* JUSTIN DO
		* Pitt Username: jud44
		* Github Username: jud44
	* NARA HERNANDEZ
		* Pitt Username: nnh6
		* Github Username: nnh6
	* GRANT SMITH
		* Pitt Username: gas101
		* Github Username: GrantSmith0

## Game Description

**Story Overview:** There’s a system of mines. Each sector has an entrance and an exit way but all the maps have disappeared. You’re a miner hired to explore the different mines and find a path from the entrance to exit.

**Type:** Platform game (action subgenre) + Player versus Environment

**Player Goal:** Find the other exit without dying or getting trapped. You can also pick up gold and other goods that you find. 

**Concept Art:**

![Mock Scene](https://github.com/CS1666-Miner-Pitfall-2022/Images/blob/main/Miner%20Pitfall%20Scene%20Concept%2025.png)
![Axe](https://github.com/CS1666-Miner-Pitfall-2022/Images/blob/main/pickaxe.png)
![Bomb](https://github.com/CS1666-Miner-Pitfall-2022/Images/blob/main/dynamite.png)
![Bow](https://github.com/CS1666-Miner-Pitfall-2022/Images/blob/main/Crossbow-pulled.png)
![Arrow](https://github.com/CS1666-Miner-Pitfall-2022/Images/blob/main/Crossbow-pre.png)

**Gameplay Mechanics:** 
	Player: The player will be able to move left and right using 'A' and 'D', and will be able to jump with the space bar. Ladders will be ascended and descended using 'W' and 'S' respectively.

	Inventory Items: These will be accessed by tabbing through the different options of pickaxe (default), crossbow, and dynamite. The dynamite will be picked up later in the game for specific uses.

	Pickaxe: This will be used to break portions of the map and damage enemies and is activated by clicking the mouse. 

	Crossbow: Will be used to damage enemies at a range, and interact with map elements from a distance. The crossbow will be aimed by controlling the mouse location on screen and fired with a mouse click.

	Dynamite: This will be an item that can be picked up later in the game and added to your inventory. It is a throwable item and will have an arched path. The explosion will cause a larger amount of damage to the map.

	Mobs: Will be angry groundhogs that move side to side and can damage players.

	Health: The player will have a health bar that will be affected by mobs, possible damage from explosions, and staying underwater for too long.

	Water: Will be randomly generated in ceratin segments of the map and will include a player oxygen level when entered. Water will have a different movement style when traversed.

**Scope of the Game: Map Size** The game will contain 100x100 subrooms, each subroom contains 25 4x4 subroom grids. 

## Advanced Topic Description

### ADVTOPIC1: PROCEDURAL GENERATION

**General Topic:** Procedural Generation is programmatic random or pseudo random process to generate game content as opposed to handcrafting it. Procedural generation allows for more content and more replayability because the game is always generating new content. Since the content is being generated programmatically, more content can always be made by tweaking some seed parameters. 

**How we will implement:** We will construct a grid of rooms for the player to explore, each room being created procedurally. We will do this using cellular automata to create natural looking environments. Using rules such as the 4-5 method allows for production of structures that look natural. This process will be based on a random seed, or possibly user entered seeds to allow for sharing of interesting maps. 
    
### ADVTOPIC2: PHYSICS SIMULATION

**General Topic:** Computer simulations are programs that are "run on a computer that uses step-by-step methods to explore the approximate behavior of a mathematical model" and are a comprehensive method for studying systems. It can also be described as “any computer-implemented method for exploring the properties of mathematical models where analytic methods are not available.” Computer simulations have a wide range of uses in many fields such as astrophysics, particle physics, materials science, engineering, fluid mechanics, climate science, evolutionary biology, ecology, economics, decision theory, medicine, sociology, and epidemiology. 

Computer Simulations have 3 general purposes which are for predictions (making data), understanding given data, and also for exporatory/heuristic purposes. Simulations are great for making predictions because they can give reliable predictions for very specific circumstances where experiments are not a feasible option for collecting data. There is 2 primary type of simulations which are Equations-based simulations, where the whole simulation is based on global rules where "there is governing theory that can guide the construction of mathematical models based on differential equations", and agent-based simulations where the "networked interaction of many individuals is being studied" and has no global equation governing the actions of the individuals but is instead based local rules. There are also sub-categories such as multiscale simulations and Monte Carlo simulations.

Equations-based simulations are most common in the physical sciences and will most likely be what we will implement in our game.

**How we will implement:**
For our physics engine we will be implementing physics for the player, pickaxe, dynamite, and crossbow. The gravity physics will be used for the player, dynamite, and crossbow. This will be implemented using a constant of 9.8 to simulate gravity. This simulation will affect how the player moves and how the throwable objects are handled through the air. For the dynamite will be modelling the kinetic energy of an explosion. Calculating how much the energy drops off from the epicenter of the dynamite. This kinetic energy modelling will also go hand in hand with how we implement destructible parts of our game. We will need to model the pixels from the explosion and how it will affect the environment. We would implement this with a destructible system of particles and the energy that is imparted from the explosion that could damage the enemies and player. 

## Midterm Goals
* Player can start a new game. The level generation at this point won't be fully implemented, so there should be an example level, could be smaller than the generated levels.
* Game Over and Victory Screens, as well as conditions for reaching them
	* Player health, where enemies can damage them
	* Exit Door, which gives the Win screen
* Basic player controls
	* Collision with walls and floors
	* Ability to move left and right
	* Ability to jump and fall
	* Ability to swing Axe
	* Axe can damage enemies
## Final Goals

* Procedural Level Generation: The game is able to create a new level for the player to explore (50%)
	* The level is aproximately 100x100 rooms (To demonstrate the generation works on a large scale, finding an exit in a maze this large seems unlikely) (20%)
	* Some rooms contain enemy mobs that can interact with the player (Determined by the generator) (15%)
	* The level contains at least 2 types of items the player can pick up, i.e. Dynamite, Crossbow, placed in rooms by the generator (15%)
* Physics for thrown objects(dynamite), and explosions (50%)
	* Simulation of force created by explosions, which determines what in the environment is broken by them and how much (35%)
	* Broken objects in the environment have physics to determine what direction they fly and their speed (15%)

## Stretch Goals

* Fluid/water simulation (PhySim team)
* Boss Fight AI (ProGen team)
