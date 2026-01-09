# 2D Platformer Game

A side-scrolling 2D platformer game built with Python and Pygame, featuring player characters, enemies, collectibles, and challenging level design.

## Features

- **Player Character**: Control a player with smooth movement, jumping, and attack mechanics
- **Enemy AI**: Intelligent enemies with patrol behavior, vision detection, and ranged attacks
- **Level Design**: Tile-based levels loaded from CSV files for easy customization
- **Collectibles**: Collect coins and health items scattered throughout levels
- **Health System**: Manage player health with health pickups and enemy damage
- **Parallax Scrolling**: Dynamic background with multiple parallax layers for depth
- **Animations**: Smooth sprite animations for idle, running, jumping, and death states
- **Camera System**: Smooth camera following with screen scroll boundaries

## Project Structure

```
2d-platformer-game/
├── main.py              # Main game file
├── tileinfo.txt         # Tile information reference
├── level_1.csv          # Level map data
├── assets/
│   ├── background/      # Parallax background layers (1-5.png)
│   ├── player/          # Player character animations
│   │   ├── idle/
│   │   ├── run/
│   │   ├── jump/
│   │   ├── death/
│   │   └── attack/
│   ├── enemy/           # Enemy character animations
│   │   ├── idle/
│   │   ├── run/
│   │   ├── jump/
│   │   ├── death/
│   │   └── attack/
│   ├── tiles/           # Tileset graphics (0-49.png)
│   ├── coin.png         # Collectible coin sprite
│   ├── health.png       # Health pickup sprite
│   ├── arrow.png        # Arrow projectile sprite
│   └── icon.png         # Game window icon
└── levels/              # Level data files
    └── level_1.csv      # First level map
```

## Game Mechanics

### Player Controls

- **A/D or Arrow Keys**: Move left/right
- **SPACE**: Jump
- **Shift**: Attack/Shoot arrows

### Gameplay Elements

- **Movement**: Navigate through platforms using smooth movement and jumping mechanics
- **Combat**: Defeat enemies by shooting arrows at them
- **Collectibles**: Gather coins and health items to stay alive
- **Health**: Health decreases when hit by enemies; collect health items to restore
- **Level Navigation**: Progress through tile-based levels with obstacles and platforms
- **Water Hazard**: Avoid water sections that instantly defeat the player

### Game Settings

- **Screen Resolution**: 1280x720
- **Frame Rate**: 75 FPS
- **Gravity**: 0.5 (affects falling speed)
- **Tile Size**: 45 pixels (720 / 16 rows)
- **Player Speed**: 5 pixels per frame
- **Max Tile Types**: 50

## Requirements

- Python 3.x
- Pygame

## Installation

1. Clone or download this project
2. Install Pygame:
   ```bash
   pip install pygame
   ```

## Running the Game

Execute the main game file:

```bash
python main.py
```

## Level Design

Levels are defined in CSV files located in the `levels/` folder. Each number in the CSV represents a different tile type from the tileset. Create custom levels by:

1. Creating a new CSV file in the `levels/` folder
2. Populating it with tile IDs (0-49) to create your level layout
3. Updating the game to load your custom level

## Asset Requirements

To run the game, ensure all required image assets are present in the `assets/` folder:
- Background images (1-5.png)
- 50 tile graphics (0-49.png)
- Player animations (4 action types with multiple frames each)
- Enemy animations (4 action types with multiple frames each)
- UI elements (coin, health, arrow, icon)

## Game Classes

### Player
Main controllable character with movement, jumping, health, and animation system.

### Enemy
AI-controlled enemy with pathfinding, patrol behavior, vision detection, and attack capabilities.

### Arrow
Projectile weapon fired by the player and enemies.

### World
Manages level layout, tile collision, and level data from CSV files.

## Tips

- Use platforms strategically to reach higher areas
- Watch out for enemy patrol patterns and plan your shots
- Collect health items to extend your survival
- The camera follows the player, so stay in the center for the best view

## Future Enhancements

- Additional levels and difficulty progression
- Power-ups with special abilities
- Boss encounters
- Particle effects and visual polish
- Sound effects and background music
- Save/load system for progress

---

Enjoy the game!
