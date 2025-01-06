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

### Playing Different DOOM Games (DOOM 2, Final DOOM, etc.)

You can play different DOOM games by using their respective WAD files. Here's how:

1. First, backup your current working WAD files:
   ```bash
   rename doom1.wad doom1.wad.backup
   rename doomgeneric.data doomgeneric.data.backup
   ```

2. Copy your new WAD file (e.g., doom2.wad, tnt.wad, plutonia.wad) to the directory

3. Rename it to match what the game expects:
   ```bash
   rename your_game.wad doom1.wad
   ```

4. Create the data file:
   ```bash
   copy doom1.wad doomgeneric.data
   ```

5. Restart the Python server and refresh your browser

To switch back to a different WAD:
1. Backup current WAD files (steps 1 above)
2. Restore the WAD you want to play:
   ```bash
   rename desired_wad.wad.backup doom1.wad
   copy doom1.wad doomgeneric.data
   ```

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
- `doomgeneric.data`: Game data file (copy of active WAD)
- `doom1.wad`: Active DOOM WAD file

## Troubleshooting

If the game doesn't start:
1. Make sure you're using a modern browser with WebAssembly support
2. Check if all files are present in the directory
3. Ensure the Python server is running and you can access http://localhost:8000
4. Check the browser's console (F12) for any error messages
5. When switching WAD files:
   - Make sure both doom1.wad and doomgeneric.data are exact copies
   - Verify the WAD file is a valid DOOM WAD
   - Try restoring the original WAD files from backup to verify the system works

## Credits

This is a WebAssembly port of DoomGeneric. Original implementation by ozkl.
