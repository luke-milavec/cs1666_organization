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

- **Player:** The player will be able to move left and right using 'A' and 'D', and will be able to jump with the space bar. Ladders will be ascended and descended using 'W' and 'S' respectively.
- **Inventory Items:** These will be accessed by tabbing through the different options of pickaxe (default), crossbow, and dynamite. The dynamite will be picked up later in the game for specific uses.
- **Pickaxe:** This will be used to break portions of the map and damage enemies and is activated by clicking the mouse. 
- **Crossbow:** Will be used to damage enemies at a range, and interact with map elements from a distance. The crossbow will be aimed by controlling the mouse location on screen and fired with a mouse click.
- **Dynamite:** This will be an item that can be picked up later in the game and added to your inventory. It is a throwable item and will have an arched path. The explosion will cause a larger amount of damage to the map.
- **Mobs:** Will be angry groundhogs that move side to side and can damage players.
- **Health:** The player will have a health bar that will be affected by mobs, possible damage from explosions, and staying underwater for too long.
- **Water:** Will be randomly generated in ceratin segments of the map and will include a player oxygen level when entered. Water will have a different movement style when traversed.

**Scope of the Game: Map Size** The game will contain 100x100 subrooms, each subroom contains 25 4x4 subroom grids. 

## Advanced Topic Description

### ADVTOPIC1: PROCEDURAL GENERATION

**General Topic:** Procedural Generation is programmatic random or pseudo random process to generate game content as opposed to handcrafting it. Procedural generation allows for more content and more replayability because the game is always generating new content. Since the content is being generated programmatically, more content can always be made by tweaking some seed parameters. 

**How we will implement:** We will construct a grid of rooms for the player to explore, each room being created procedurally. We will do this using cellular automata to create natural looking environments. Using rules such as the 4-5 method allows for production of structures that look natural. This process will be based on a random seed, or possibly user entered seeds to allow for sharing of interesting maps. 

Sources: https://csharpcodewhisperer.blogspot.com/2013/07/Rouge-like-dungeon-generation.html
https://developer.amazon.com/blogs/appstore/post/5cb9c2c4-7bf1-456e-a97c-6d3a0486c063/how-to-generate-random-terrain-with-cellular-automata
    
### ADVTOPIC2: PHYSICS SIMULATION

**General Topic:** Computer simulations are programs that are "run on a computer that uses step-by-step methods to explore the approximate behavior of a mathematical model" and are a comprehensive method for studying systems. It can also be described as “any computer-implemented method for exploring the properties of mathematical models where analytic methods are not available.” Computer simulations have a wide range of uses in many fields such as astrophysics, particle physics, materials science, engineering, fluid mechanics, climate science, evolutionary biology, ecology, economics, decision theory, medicine, sociology, and epidemiology. 

Computer Simulations have 3 general purposes which are for predictions (making data), understanding given data, and also for exporatory/heuristic purposes. Simulations are great for making predictions because they can give reliable predictions for very specific circumstances where experiments are not a feasible option for collecting data. There is 2 primary type of simulations which are Equations-based simulations, where the whole simulation is based on global rules where "there is governing theory that can guide the construction of mathematical models based on differential equations", and agent-based simulations where the "networked interaction of many individuals is being studied" and has no global equation governing the actions of the individuals but is instead based local rules. There are also sub-categories such as multiscale simulations and Monte Carlo simulations.

Equations-based simulations are most common in the physical sciences and will most likely be what we will implement in our game.

**How we will implement:**
 For the dynamite we will be modelling the kinetic energy of an explosion. Calculating how much the energy drops off from the epicenter of the dynamite. This kinetic energy modelling will also go hand in hand with how we implement destructible parts of our game. We will need to model the pixels from the explosion and how it will affect the environment. We would implement this with a destructible system of particles and the energy that is imparted from the explosion that could damage the enemies and player. This would be a model of collisions of explosion particles/destructible environment physics.

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
	* At least one type of enemy that can harm the player
## Final Goals
* Basic Functionality (10%)
	* Game Over and Victory Conditions: The player wins when they find the exit, and loses if they run out of health. (2%)
	* Movement: The player can move left and right, jump around, and stay in-bounds. (3%)
	* Combat: The player is able to swing their Axe, or shoot their crossbow (if applicable). Enemies are able to damage the player, and the player can damage the enemies. The game has enemies. (5%)
* Procedural Level Generation: The game is able to create a new level for the player to explore (45%)
	* The level is aproximately 100x100 rooms (To demonstrate the generation works on a large scale, finding an exit in a maze this large seems unlikely) (25%)
	* Some rooms contain enemy mobs that can interact with the player (Determined by the generator) (10%)
	* The level contains at least 2 types of items the player can pick up, i.e. Dynamite, Crossbow, placed in rooms by the generator (10%)
* Physics for thrown objects(dynamite), and explosions (45%)
	* Simulation of force created by explosions, which determines what in the environment is broken by them and how much (30%)
	* Broken objects in the environment have physics to determine what direction they fly and their speed (15%)

## Stretch Goals

* Fluid/water simulation (PhySim team)
	- Certain portions of the map will generate with sections of water. Once submerged in the water, a player oxygen meter will appear to show how much time you can remain fully submerged. The player movement in the water will be much slower than on ground, and the player will be able to swim up by repeatedly pressing space. Explosions under water will be much smaller than on the ground to accurately simulate how water will dampen its effects and range.
* Boss Fight AI (ProGen team)
	Our development of the Boss Fight AI will focus on the three techniques: line of sight, image recognition of the level, and pathfinding.
	- Line of sight: line of sight will limit the things the enemy reacts onto what they sees, in a similar fashion to how a player only react to what is displayed on the screen. This can be implemented with assistance of Bresenham's algorithm.
	- Image recognition of the level: make the enemy AI agents see their closest surroundings; a technique for knowing when to jump, duck and do all other kinds of evasion maneuvers when the enemy AI moves between two points on the level, and there are blocks in the way blocking the straight path. To achieve this, we will draw support from the collision detection algorithms developed by our physics simulation team.
	- Pathfinding: a technique to make the enemy less predictable. Pathfinding with A* is an established pathfinding algorithm that we have the aid of.
