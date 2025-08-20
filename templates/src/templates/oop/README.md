# Rogue Game - Terminal Dungeon Crawler

A Python-based roguelike dungeon crawler game featuring ASCII graphics, multiple character classes, dungeon exploration, combat, and item collection.

![Welcome Screen](docs/welcome_ascii.png)

## 🎮 Game Description

**Rogue Game** is a classic terminal-based dungeon crawler where players navigate through multiple levels of procedurally generated dungeons, fight various enemies (gnomos), collect powerful items, and ultimately retrieve the treasure to win the game.

### 🌟 Key Features

- **Three Character Classes**: Choose between Barbarian, Knight, and Ninja, each with unique stats
- **Multi-level Dungeons**: Explore 3 levels of challenging dungeons
- **Combat System**: Real-time combat with different damage mechanics
- **Item Collection**: Find and use pickaxe, sword, and amulet
- **Enemy Variety**: Face different types of gnomos (Kobold, Knoker, Spriggan)
- **ASCII Graphics**: Classic terminal-based visual representation
- **Procedural Generation**: Each playthrough features different dungeon layouts

## 🎯 Game Objective

Navigate through the dungeon levels, defeat enemies, collect items, and retrieve the magical amulet to achieve victory. Use your pickaxe to dig through walls, your sword to deal extra damage, and strategy to survive the challenges ahead.

## 🖥️ System Requirements

- Python 3.7 or higher
- Windows OS (for `msvcrt` module support) or compatible terminal
- Terminal with Unicode support for proper character display

### Dependencies

The game uses Python standard library modules:
- `random` - For procedural generation
- `time` - For game timing
- `typing` - For type hints
- `msvcrt` - For keyboard input (Windows-specific)
- `sys` - For system operations

## 🚀 Installation & Setup

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ignaschuemer7/pc_tp3.git
   cd pc_tp3/templates/src/templates/oop
   ```

2. **Run the game**:
   ```bash
   python menu.py
   ```

## 🎮 How to Play

### Starting the Game

1. Run `python menu.py` to start
2. Select "Play" from the main menu
3. Enter your player name (max 10 characters)
4. Choose your character class:
   - **Barbarian** (@) - High HP, Low Damage
   - **Knight** (𓀝) - Medium HP, Medium Damage  
   - **Ninja** (🀀) - Low HP, High Damage

### Game Controls

- **WASD Keys**: Move your character
  - W - Move up
  - A - Move left  
  - S - Move down
  - D - Move right
- **Combat**: Automatic when adjacent to enemies
- **Stairs**: 
  - `<` - Climb up to previous level
  - `>` - Descend to next level
- **Items**: Automatic pickup when walking over them

### Game Elements

#### Characters
- **@** - Barbarian (HP: 370, Base damage: 10-21)
- **𓀝** - Knight (HP: 320, Base damage: 23-25) 
- **🀀** - Ninja (HP: 270, Base damage: 20-43)

#### Items
- **Pickaxe**: Allows digging through walls to create new paths
- **Sword**: Increases damage output significantly
- **Amulet**: The treasure you need to collect to win

#### Enemies (Gnomos)
- **Kobold**: Found on Level 1
- **Knoker**: Found on Level 2
- **Spriggan**: Found on Level 3

#### Map Symbols
- **▓** - Wall (solid rock)
- **' '** - Empty space (walkable)
- **<** - Stairs up
- **>** - Stairs down
- **%** - Dead enemy corpse

### Winning Conditions

- Collect the amulet (treasure) 
- Return to the surface (Level 0 and above)
- Stay alive throughout the journey

## 📁 Project Structure

```
templates/src/templates/oop/
├── menu.py           # Main menu and game entry point
├── game.py           # Core game loop and mechanics
├── player.py         # Base player class
├── human.py          # Player character classes (Barbarian, Knight, Ninja)
├── gnomo.py          # Enemy classes (Kobold, Knoker, Spriggan)
├── items.py          # Game items (Pickaxe, Sword, Amulet)
├── mapping.py        # Dungeon generation and level management
├── actions.py        # Game actions (movement, combat, interactions)
├── presentations.py  # UI elements and game text
├── magic.py          # Additional game mechanics
├── README.md         # This file
└── LICENSE           # MIT License
```

### Core Classes

- **Player**: Base class for all game entities
- **Human**: Player character with inventory management
- **Gnomo**: Enemy base class with AI behavior
- **Dungeon**: Handles level generation and rendering
- **Item**: Base class for collectible objects

## 🛠️ Development

### Code Architecture

The game follows an object-oriented design pattern with clear separation of concerns:

- **Model**: Player, Gnomo, Item classes handle game state
- **View**: Presentations module handles display
- **Controller**: Menu and Game modules manage user input and game flow

### Key Design Patterns

- **Inheritance**: Character classes inherit from Player base class
- **Composition**: Dungeon contains multiple Level objects
- **Factory Pattern**: Dynamic character and enemy creation
- **State Management**: Game state tracked through dungeon levels

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 🐛 Known Issues

- Game requires Windows OS for `msvcrt` module (keyboard input)
- Some Unicode characters may not display properly on all terminals
- Game balance may need tweaking based on player feedback

## 📞 Support

For questions, issues, or contributions, please open an issue on the GitHub repository.

---

**Enjoy your dungeon crawling adventure!** 🗡️⚔️🛡️