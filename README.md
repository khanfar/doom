# DoomGeneric WebAssembly Port

This is a WebAssembly port of the classic DOOM game, allowing you to play DOOM directly in your web browser.

## Setup Instructions

### Prerequisites
- Python 3.x installed on your system
- A modern web browser (Chrome, Firefox, or Edge recommended)

### Running the Game

1. Open a terminal/command prompt in this directory
2. Start the Python server by running:
   ```bash
   python server.py
   ```
3. Open your web browser and go to:
   ```
   http://localhost:8000
   ```

The game should start automatically.

## Controls

- **Arrow keys**: Move forward/backward/turn left/right
- **Ctrl** or **Space**: Shoot/Use
- **Alt**: Strafe
- **Shift**: Run
- **1-9**: Select weapons
- **Esc**: Open menu
- **Tab**: View map
- **Right-click**: Toggle fullscreen

## Files Description

- `index.html`: Main game page
- `server.py`: Python server script with proper MIME type configuration
- `doomgeneric.js`: JavaScript code for the game
- `doomgeneric.wasm`: WebAssembly binary
- `doomgeneric.data`: Game data file
- `doom1.wad`: Original DOOM WAD file

## Troubleshooting

If the game doesn't start:
1. Make sure you're using a modern browser with WebAssembly support
2. Check if all files are present in the directory
3. Ensure the Python server is running and you can access http://localhost:8000
4. Check the browser's console (F12) for any error messages

## Credits

This is a WebAssembly port of DoomGeneric. Original implementation by ozkl.
