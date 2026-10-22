# Bubble Bobble

A Java Swing remake of the classic arcade game *Bubble Bobble*, built as a team class project by Mohammed and Samuel Tucker.

Move your hero around the platforms, trap monsters in bubbles, pop them for fruit and points, and clear all four levels to win.

## Features

- Four tile-based levels loaded from plain-text level files
- Hero with running, jumping and gravity, plus three lives per level
- Two monster types with different movement patterns
- Bubbles that trap monsters, which then turn into collectible fruit
- Live score and lives counter, win and restart handling
- Debug keys to jump between levels

## Controls

| Key | Action |
| --- | --- |
| ← / → | Move left / right |
| ↑ | Jump |
| Space | Shoot a bubble |
| R | Restart |
| U / D | Next / previous level |

## Run it

Requires a JDK (8 or newer).

```bash
javac *.java
java Main
```

The game reads its levels from `levels/level1.txt` through `levels/level4.txt`, relative to the folder you run it from. **These files are not in the repository yet**, so add them before running. Each level is a grid of characters, where each character is a 50×50 px tile:

| Char | Tile |
| --- | --- |
| `P` | Platform |
| `L` / `R` | Left / right edge wall |
| `H` | Hero start position |
| `1` / `2` | Monster type 1 / type 2 |
| (space) | Empty |

## Project layout

```
Main.java           Window, score/lives panel and game loop timer
GameComponent.java  Game state: update loop, collisions, levels, scoring
LevelLoader.java    Parses level text files into game objects
MyKeyListener.java  Keyboard controls
Drawable.java       Base class for anything drawn on screen
Movable.java        Shared movement and gravity logic
Hero.java           The player
Monster*.java       Enemies
Bubble.java, Bullet.java, Fruit.java, Platform.java
```
