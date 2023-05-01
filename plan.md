# Design doc for IBL game

Player is standing on the stern of a large sailing ship behind the wheel. Using their hands they can grab any point on the outside of the wheel, which matches the wheel position to the relative angle of their hand.

## Game loop

- Rotate ship using wheel to aim toward the [sun/moon/north star]
- Two levels: flat ocean and blue sky (intro) with full contrast, and thunderstorm where we run a staircase procedure on the contrast

## Implementation

### Game logic

- New trial signal: level 1 is ?, level 2 is thunderclap
- Green flash when trial is correct, lightning flash when incorrect? 
- Game loop runs indefinitely or until a predefined timer (e.g. 5 minutes for SfN?)

### Ship

- Ship is a 3D model that remains flat at all times
- Wheel object and interactions
- Wheel should have mass during interactions, slow to accelerate fast to stop
- Use controller vibration to indicate inverse of vibration (exponential dropoff)

### Computer fans for rotation effects

- Socket connection to an arduino, which powers up or down a front/left/right fan depending on the ships movement, should reduce nausea.
- Fans might not be powerful enough alone, might need 4-5 fans grouped together?

### Atmospheric effects / Ocean

- Ocean should have waves in level 2, basic shader effect
- Rain falling, probably using particles?
- Rain spatter on surface of ship

### Mouse brain

Would be cool to add mouse brain data into visualization in some way. 

- Could surround the ship and be activated according to the state within the trial?
- Could be shown as stars in the sky?

## Juice

- Fog
- Far in the distance, we animate some 3D models of humans in lab coats that move around slowly just out of sight
- Flapping sails

## To-do list by importance:

- Rough out objects and scale
- VR interaction with wheel
- Core game loop, with swapabble graphics (for sun/moon/gabor)
- Computer fans
- Juice on core interactions: wheel, audio in game loop
- Ocean effects
- Atmospheric effects
- Human models in distance
- Mouse brain in distance