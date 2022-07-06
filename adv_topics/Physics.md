# Physics advanced topic presentation outline

* Quick basic intro
	* Intro to computer simulation:
	* Types: Equations-based, agent-based (individual-based), multiscale, monte carlo
	* Purposes: wide range of fields use computer simulations, including physics. Computer simulations have 3 main purposes which are for Predicting/generating data, understanding given data, and also for exploratory/heuristic purposes. Simulations give reliable predictions when experiments are not possible or very difficult.
		* Resource: https://plato.stanford.edu/entries/simulations-science/
* Explosion Simulation
	* General concept of explosion in physics (conservation of momentum…)
		* https://openoregon.pressbooks.pub/bodyphysics/chapter/locomotion/ 
		* https://imechanica.org/files/physics-I_0.pdf
	* Since we would be using equations-based computer simulations for our physics engines, we will be looking at different physics equations that we would need to implement to simulate the energy in an explosion. 
		* https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.118.4404&rep=rep1&type=pdf
		* https://ieeexplore-ieee-org.pitt.idm.oclc.org/document/6376430 
			* Need to use Pitt account thru hillman to access
	* Rust/Pseudo code: how we would implement this in our game
* Reach Goal: Fluids
	* General concept of fluid motion
	* Water Ripple
	* Smoothed-particle hydrodynamics
		* https://en.wikipedia.org/wiki/Smoothed-particle_hydrodynamics 
	* Schwarz–Christoffel mapping
		* https://en.wikipedia.org/wiki/Schwarz%E2%80%93Christoffel_mapping
	* Modeling Laminar Flow (smooth running water)
		* https://towardsdatascience.com/computational-fluid-dynamics-using-python-modeling-laminar-flow-272dad1ebec 
	* Resource: http://bugman123.com/FluidMotion/ 
