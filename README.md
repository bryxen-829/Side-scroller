# Side Scroller - Mario-like Game

A mobile-friendly side-scrolling platformer game built with Godot and GDScript, featuring multiple worlds, levels, and power-ups.

## Features

### Gameplay
- **Multiple Worlds & Levels**: 4 worlds with multiple levels each
- **Progressive Difficulty**: Levels unlock as you progress
- **Time Limit**: Complete levels before time runs out
- **Collectibles**: Coins to collect for points

### Power-ups
1. **Mushroom**: Increases speed and jump height
2. **Flower**: Enables fire projectile attacks
3. **Star**: Temporary invincibility with enhanced speed

### Mobile Controls
- **Arrow Keys / Touch Left**: Move left
- **Arrow Keys / Touch Right**: Move right
- **Spacebar / Touch Bottom**: Jump
- **X Key**: Use action (fire flower)

### Enemy System
- Patrol enemies with simple AI
- Jumping on enemies defeats them
- Collision damage with invulnerability

## Project Structure

```
res://
├── scenes/
│   ├── player/
│   │   └── Player.gd
│   ├── levels/
│   │   └── Level.gd
│   ├── enemies/
│   │   └── Enemy.gd
│   ├── powerups/
│   │   └── Powerup.gd
│   ├── collectibles/
│   │   └── Coin.gd
│   ├── projectiles/
│   │   └── Fireball.gd
│   └── ui/
│       ├── MainMenu.gd
│       ├── LevelSelect.gd
│       └── WorldSelect.gd
├── project.godot
└── README.md
```

## Getting Started

1. **Install Godot**: Download Godot 3.x engine
2. **Import Project**: Open this project in Godot
3. **Create Scenes**: Build the scene files (.tscn) using the provided scripts
4. **Add Assets**: Import or create sprite sheets for characters and enemies
5. **Configure Levels**: Design level layouts using tile sets

## Game Development Checklist

- [ ] Create Player sprite sheets (idle, run, jump, damaged)
- [ ] Create Enemy sprite sheets (Goomba, Koopa variations)
- [ ] Create Powerup sprites
- [ ] Create Coin animation sprites
- [ ] Create UI graphics (buttons, menus)
- [ ] Design level layouts (World 1-4, multiple levels each)
- [ ] Add sound effects (jump, coin, powerup, enemy defeat)
- [ ] Add background music
- [ ] Implement parallax scrolling
- [ ] Fine-tune physics and controls
- [ ] Create level progression system
- [ ] Add game over and level complete screens
- [ ] Implement pause menu
- [ ] Add difficulty scaling

## Controls Reference

| Action | Keyboard | Mobile |
|--------|----------|--------|
| Move Left | Arrow Left | Touch Left Side |
| Move Right | Arrow Right | Touch Right Side |
| Jump | Spacebar | Touch Bottom |
| Action/Fire | X | On-Screen Button |

## Physics Parameters

- **Player Speed**: 200 pixels/sec (250 with mushroom)
- **Jump Force**: 400 pixels/sec² (500 with mushroom)
- **Gravity**: 800 pixels/sec²
- **Acceleration**: 1200 pixels/sec²
- **Friction**: 800 pixels/sec²

## How to Create Scene Files

1. Create a new Scene in Godot
2. Add the appropriate script to the root node
3. Structure the node hierarchy as needed
4. Add sprites, collision shapes, and audio nodes
5. Save the scene file in the appropriate folder

### Example Player Scene Structure:
```
Player (KinematicBody2D) -> Player.gd
├── AnimatedSprite
├── CollisionShape2D
└── Camera2D
```

## Extensibility

The codebase is designed to be easily extended:
- Add new enemy types by extending `Enemy.gd`
- Create new power-ups by adding to the power-up system
- Design new levels using the existing level template
- Add new worlds by duplicating world directories

## Next Steps

1. Create all scene files (.tscn) using the provided scripts
2. Add sprite animations for the player
3. Create level layouts with TileMaps
4. Implement sound effects and music
5. Test on mobile devices with touch controls

---

**Happy Game Development! 🎮**
