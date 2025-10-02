# Brick Breaker Game

A Java-based brick breaker game with advanced features including multiple obstacle types, special abilities, and a map editor. This project is a modern take on the classic Pong/Arkanoid-style arcade game.

## 🎮 Game Description

Brick Breaker Game is an enhanced version of the classic brick breaker arcade game. Players control a paddle to bounce a ball and destroy various types of obstacles (bricks) while collecting power-ups and avoiding hazards. The game features a custom map editor for creating and saving custom levels, plus a challenging "Ymir" system that periodically introduces random game-changing events.

## ✨ Features

### Game Modes
- **Building Mode**: Create custom maps with a visual editor
- **Running Mode**: Play through created or loaded maps
- **Map Save/Load System**: Store and retrieve custom maps from a PostgreSQL database

### Obstacle Types
- **Simple Obstacles** (Wall Maria): Basic bricks with 1 hit point
- **Firm Obstacles** (Stein's Gate): Stronger bricks requiring 2-5 hits
- **Explosive Obstacles** (Pandora's Box): Dangerous bricks that end the game if they reach the paddle
- **Gift Obstacles** (Gift of Uranus): Drop random power-ups when destroyed

### Special Abilities
- **Expansion (E)**: Doubles the paddle width temporarily (30 seconds)
- **Unstoppable (U)**: Ball destroys all obstacles in one hit (30 seconds)
- **Hex (H)**: Activates dual cannons that shoot additional projectiles (30 seconds)
- **Extra Life (C)**: Gained from gift obstacles

### Ymir System
A unique game mechanic that randomly triggers challenging events every 30 seconds:
- **Infinite Void**: Freezes 8 random obstacles temporarily
- **Double Acceleration**: Slows down the ball
- **Hollow Purple**: Spawns 8 new purple obstacles

### Gameplay Features
- **Paddle Rotation**: Rotate the paddle left/right (±45°) for strategic ball angles
- **Score System**: Time-based scoring that rewards quick obstacle destruction
- **Lives System**: 3 lives per game
- **Frozen Obstacles**: Temporarily invulnerable obstacles (shown in green)
- **Physics-based Ball Movement**: Realistic collision detection and bouncing

## 🎯 Controls

### Building Mode
- **Arrow Keys**: Navigate the grid
- **Space**: Select/place obstacles
- **Generate Obstacles Button**: Add obstacles to the map
- **Save Map Button**: Save current map to database
- **Start Game Button**: Begin playing the current map

### Running Mode
- **W**: Launch the ball
- **Left/Right Arrow Keys**: Move paddle horizontally
- **A/D**: Rotate paddle left/right
- **T**: Activate Expansion ability
- **H**: Activate Hex ability
- **U**: Activate Unstoppable ability
- **P**: Pause game

## 🛠️ Technical Details

### Technologies Used
- **Java Swing**: GUI framework
- **PostgreSQL**: Database for map storage
- **JUnit 5**: Unit testing framework
- **Java 2D Graphics**: Game rendering

### Design Patterns
- **Singleton Pattern**: Used for Controller, Game, Paddle, and UI panels
- **Factory Pattern**: FactoryObstacle for creating different obstacle types
- **MVC Architecture**: Separation of domain logic, UI, and data persistence

### Key Classes
- **Controller**: Main game controller managing obstacles and game state
- **Game**: Core game loop and collision detection
- **Ball**: Ball physics and movement
- **Paddle**: Paddle movement and rotation
- **Obstacle**: Base class for all obstacle types
- **Abilities**: Power-up system management
- **Ymir**: Random event generator


1. **Clone the repository**
   ```bash
   git clone <your-repository-url>
