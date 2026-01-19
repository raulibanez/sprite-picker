# Sprite Picker

A simple browser-based tool for extracting sprite regions from sprite sheets.

## Features

- **Drag & Drop**: Load any image by dragging it onto the canvas
- **Click to Open**: Click the drop zone to open a file picker
- **Paste from Clipboard**: Use Ctrl+V to paste images directly
- **Precise Selection**: Draw rectangles to select sprite regions with pixel-perfect accuracy
- **Resize Selections**: Drag the bottom-right corner handle to fine-tune selection size
- **Zoom**: Mouse wheel to zoom in/out, centered on cursor position
- **Pan**: Alt+drag or middle mouse button to pan around the image (works even while selecting)
- **Pixel Grid**: Automatic pixel grid overlay when zoomed in (6x+)
- **Named Sprites**: Give each selection a custom name
- **Move Selections**: Click and drag on labels to reposition selections
- **Rename**: Double-click on labels to rename sprites
- **Copy Coordinates**: Click on coordinates to copy individual sprites
- **Format Toggle**: Switch between `[x, y, w, h]` and `[x1, y1, x2, y2]` coordinate formats
- **Export All**: Copy all selections as a JavaScript object ready to use

## Usage

1. Open `index.html` in your browser
2. Load an image:
   - Drag and drop a sprite sheet image onto the canvas, or
   - Click the drop zone to select a file, or
   - Copy an image and press Ctrl+V to paste it
3. Draw rectangles around the sprites you want to extract
4. Name each sprite when prompted
5. Use the format toggle to switch between coordinate formats if needed
6. Click "Copy All" to get the coordinates as a JS object

## Output Format

### Default format `[x, y, w, h]`:
```javascript
const spriteRegions = {
    player_idle: [0, 0, 32, 32],
    player_walk: [32, 0, 32, 32],
    enemy: [64, 0, 16, 16],
};
```

### Alternative format `[x1, y1, x2, y2]`:
```javascript
const spriteRegions = {
    player_idle: [0, 0, 32, 32],
    player_walk: [32, 0, 64, 32],
    enemy: [64, 0, 80, 16],
};
```

## Controls

| Action | Control |
|--------|---------|
| Load image | Drag & drop / Click drop zone / Ctrl+V |
| Select region | Click and drag |
| Resize selection | Drag bottom-right corner handle |
| Zoom | Mouse wheel |
| Pan | Alt + drag / Middle mouse (works during selection) |
| Move selection | Drag label |
| Rename | Double-click label |
| Copy single | Click coordinates |
| Copy all | Click "Copy All" button |
| Toggle format | Click format button |

## License

MIT
