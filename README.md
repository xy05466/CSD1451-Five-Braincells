# Just Two Guys

**Just Two Guys** is a 2D puzzle-platformer built by **Five Braincells** at DigiPen. Switch between a shield-wielding melee character and a ranged character with a bow to solve puzzles, cross platforming sections, and fight enemies and mini-bosses across three levels.

## How to play

Switch characters to suit the obstacle ahead. The melee character can raise a shield, the ranged character can aim and fire arrows, and a well-placed crate can defeat an enemy. Either character can reach the exit to advance the level. Checkpoints save the current positions of both characters, and optional side paths offer upgrades.

| Input | Action |
| --- | --- |
| `A` / `D` | Move left or right |
| `Space` | Jump |
| `E` | Switch to the melee character |
| `R` | Switch to the ranged character |
| Hold `Q` as melee | Raise the shield |
| Hold `Q` as ranged, then move the mouse | Aim the bow |
| Left click while aiming | Fire an arrow |
| `F` near a crate or level exit | Grab or release the crate, or enter the exit |

For quick level testing in debug mode, press `3`, `4`, or `5` to jump to Levels 1, 2, or 3 respectively.

## Build and run

1. On Windows, open [Project1.sln](Project1.sln) in Visual Studio 2022 with the **Desktop development with C++** workload.
2. Select **Debug | x64** or **Release | x64**, then build and run the project.
3. If launching the executable directly, start it from its output folder under `bin/`. The build copies the assets and runtime libraries into that folder.

## Technical highlights

- **Data-driven levels.** [MapManager.cpp](MapManager.cpp) loads tile layouts from CSV files. Tile tags link puzzle elements, so a lever can toggle a group of lasers without hard-coding their positions.
- **Component-based game objects.** Game objects compose components for behaviours such as sprite rendering, animation, and collision. The project is written in C++ with DigiPen’s Alpha Engine.
- **Checkpoint persistence.** [SaveManager.cpp](SaveManager.cpp) stores player, map, enemy, and audio state in separate save files. Reloading restores both characters and the saved level state.

## My contributions

I worked on the CSV-driven tilemap and level layouts, including tile tags, background tiles, lever-controlled lasers, and fading cloud platforms. I also contributed to saving player and object state and restoring that data during level transitions.

## Team

Five Braincells is Choy Phui Mun, Nadyrah Binte Tarmidi, Kon Xin Yi, Chua Qi Jun, and Ang Zi Jun. Our final presentation highlighted version control and clear communication as two lessons from building the game together.
