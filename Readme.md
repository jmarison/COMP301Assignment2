# Week 2 Example — Movement + Boundaries

This example supports the Week 2 slides.

## Learning goals
- Define a playfield separate from the HUD
- Update movement with dt and a velocity vector
- Implement boundary rules (clamp/wrap/bounce)
- Add a simple goal loop (reach target) + a second object (teleporter)

## Run
From this folder:

- `python3 -m pip install pygame`
- `python3 main.py`

## Controls
- Arrow keys / WASD: move
- `Tab`: cycle boundary mode
- `P`: toggle platformer mode (jump + gravity)
- `Up` / `W`: jump (platformer mode)
- `R`: reset level
- `Space`: start (from title)
- `Esc`: quit

## What to change first
- `PLAYFIELD_PADDING`, `PLAYER_MAX_SPEED`, `TIMER_SECONDS`
- Try swapping boundary mode defaults
- Try making the teleporter a hazard instead

## Changes
- Added increasing amount of teleporters depending on the level. This increases the difficulty as the player progresses requiring them to move slower as levels progress
- Adjusted friction to reduce the slippery "icy" feel
- Created a powerup which adds 3 seconds to the remaining time on each level
- Time powerup gives the player a choice to potentially either go out of the way to pick it up or head directly towards the goal
- Decreased time from 30 to 15 seconds due to having more precise control from the greater friction and a powerup which gives time

## Future Changes
- Occasionally there is a problem with the player's movement. Where it the movement does not completely stop but rather moves in a direction at a steady, slow rate (in my testing this typically happens moving up or left)
- Could add a score which gives points based on the remaining time within the level.  This would also reward going out of the way for the power up since it would give more time remaining
- As levels go on, I think the power up should give more time due to the increased amount of obstacles on each level requiring more time to get through the levels
