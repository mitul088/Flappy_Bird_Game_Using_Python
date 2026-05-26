Note : This repository is an individual project repository I developed locally in October 2023 using python. It was migrated to GitHub in May 2026 for documentation and review purposes.

# Flappy Bird Game

A desktop recreation of the classic Flappy Bird arcade game, built with Python and [Pygame](https://www.pygame.org/). Guide the bird through gaps in moving pipes, earn points, and try to beat your best run.

---

## Overview

This project is a single-player side-scrolling game inspired by Flappy Bird. You control a bird that falls with gravity and rises when you flap. Avoid pipes and the ground; each pipe you pass safely increases your score.

The game includes **two visual themes** (Mode 1 and Mode 2), sound effects, a pause menu with restart, and a mode-selection screen when you launch the application.

---

## Features

| Feature | Description |
|--------|-------------|
| **Two game modes** | Choose between two backgrounds and themes from the main menu |
| **Classic gameplay** | Gravity, flapping, randomly generated pipe gaps |
| **Score tracking** | On-screen score display; progress also printed to the console |
| **Sound effects** | Wing flap, scoring, collision, and UI feedback |
| **Pause & restart** | Pause during play and return to the mode menu via the restart control |
| **Welcome screens** | Short intro screen before each mode starts |

---

## Requirements

- **Python** 3.6 or newer (3.8+ recommended)
- **Pygame** 2.x

Install Pygame with pip:

```bash
pip install pygame
```

---

## Getting Started

### 1. Clone or download the project

Place the project folder on your computer. The folder must keep this structure intact (especially the `gallery` directory).

### 2. Open a terminal in the project folder

**Windows (PowerShell or Command Prompt):**

```bash
cd "path\to\Flappy Bird Game"
```

**macOS / Linux:**

```bash
cd "/path/to/Flappy Bird Game"
```

### 3. Run the game

```bash
python FlappyBirdGamePlay.py
```

On some systems you may need:

```bash
python3 FlappyBirdGamePlay.py
```

A game window titled **Flappy Bird Game** should open.

---

## How to Play

### Main menu

1. When the game starts, you see the **mode selection** screen.
2. Click **Mode 1** or **Mode 2** to pick a theme.
3. On the welcome screen, press **Space** or **Up Arrow** to begin.

### During gameplay

| Action | Key / Input |
|--------|-------------|
| Flap (rise) | **Space** or **Up Arrow** |
| Pause / open menu | **Left Shift** or **Right Shift** |
| Restart (while paused) | Click the **restart** button in the top-left |
| Quit | **Escape** or close the window |

### Objective

- Fly through the gap between upper and lower pipes.
- Each pipe passed adds **1** to your score.
- Hitting a pipe, the ceiling, or the ground ends the run; you return to the welcome flow for that mode.
- From the welcome screen, you can use the on-screen control (top-left) to go back to the **mode selection** menu.

---

## Project Structure

```
Flappy Bird Game/
├── FlappyBirdGamePlay.py    # Main game logic and entry point
├── README.md                 # This file
└── gallery/
    ├── audio/                # Sound effects (.wav)
    │   ├── die.wav
    │   ├── hit.wav
    │   ├── point.wav
    │   ├── swoosh.wav
    │   └── wing.wav
    └── sprites/              # Images (bird, pipes, UI, backgrounds, digits)
        ├── bird.png
        ├── pipe.png
        ├── background.png
        ├── mode1.jpg
        ├── mode2.jpg
        └── ...
```

**`FlappyBirdGamePlay.py`** contains:

- Mode selection and game loop (`ma()`)
- Welcome screens and main gameplay for each mode
- Pipe generation, collision detection, and scoring
- Pause and restart handling

Do not move or rename asset files without updating the paths in the source code.

---

## Configuration

Default display and timing settings are defined at the top of `FlappyBirdGamePlay.py`:

| Setting | Default | Purpose |
|---------|---------|---------|
| `FPS` | 32 | Game frame rate |
| `SCREENWIDTH` | 289 | Window width (pixels) |
| `SCREENHEIGHT` | 511 | Window height (pixels) |

Adjust these values only if you understand how they affect layout and physics.

---

## Troubleshooting

| Problem | What to try |
|---------|-------------|
| `ModuleNotFoundError: No module named 'pygame'` | Run `pip install pygame` for the same Python you use to start the game |
| Window opens but images/sounds are missing | Run the script from the **project root** so `gallery/` paths resolve correctly |
| Game runs slowly | Close other heavy applications; lower system display scaling if needed |
| `python` not found | Use `python3` or install Python from [python.org](https://www.python.org/downloads/) |

---

## Acknowledgments

Gameplay is inspired by the original **Flappy Bird** by Dong Nguyen. Sprites and audio in `gallery/` are used for this educational/desktop project implementation.
