# PhysicsGame
Project with Unreal Engine 5

This project consist of three mini-games designed to explore and implement various physics-based mechanics with UE. 
The goal was to rely entirely on the engine's physics solver for gameplay. 

## 1. Archery Range
A precision game where the trajectory is determined by mechanical force

Physics Mechanic : Impulsion Force applied to the projectile (Arrow)

Technical choices : - Dynamic force calculation

Projectile physics : gravity is enabled only upon to ensure a clean launch.
Lerp used to visually simulate to the bowstring tension
Huge Problem : Control the projectile and the shoot of the bow (impulsion force) The Target and Chest Loop was a bit difficult to control at the beginning

## 2. Plateform
An agillity course featuring unpredictable, physics-driven obstacles

Physics Mechanic : Heavy use of Physics constraints

Technical choices : Swinging Plateform : Configured constraints with specific Angular Limits and Angular Drive to create a natural pendulum effect. (and math on blueprint, that help a lot)

Huge Problem : at first i tried with just a timeline, but not worked at all. with angular parameters and a little calculate of sinus on pitch(y) that fine !

## 3. Grab Puzzle ( + pressures plates)
Object manipulation and weight-based logic

Physics Mechanic : Physics Handle component and Overlap Events

Technical choices : - Grab system instead of simply attaching the cube to the hand, i usesd physics handle. This allow the cube to still collide with walls and react to the environment while being carried.

Pressure Plates : Detection is handle via OnComponentBeginOverlap.
Huge Problem : Not very had a huge problem on this game, but at first i forgot to check simulate physic, that allow the player to press the button but not the cube.....

## Key Takeaways
Substepping: Learned how to enable physics substepping to stabilize complex simulations. Impulse vs. Force: Mastered the difference between applying an instantaneous change in velocity (Impulse) versus a gradual change (Force). Collision Optimization: Optimized collision presets (BlockAll vs. Overlap) to maintain performance.
