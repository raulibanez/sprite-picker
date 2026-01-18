# Sprite Picker

A simple browser-based tool for extracting sprite regions from sprite sheets.

## Features

- **Drag & Drop**: Load any image by dragging it onto the canvas
- **Precise Selection**: Draw rectangles to select sprite regions with pixel-perfect accuracy
- **Zoom**: Mouse wheel to zoom in/out, centered on cursor position
- **Pan**: Alt+drag or middle mouse button to pan around the image
- **Pixel Grid**: Automatic pixel grid overlay when zoomed in (6x+)
- **Named Sprites**: Give each selection a custom name
- **Move Selections**: Click and drag on labels to reposition selections
- **Rename**: Double-click on labels to rename sprites
- **Copy Coordinates**: Click on coordinates to copy individual sprites
- **Export All**: Copy all selections as a JavaScript object ready to use

## Usage

1. Open `index.html` in your browser
2. Drag and drop a sprite sheet image onto the canvas
3. Draw rectangles around the sprites you want to extract
4. Name each sprite when prompted
5. Click "Copy All" to get the coordinates as a JS object

## Output Format

```javascript
const spriteRegions = {
    player_idle: [0, 0, 32, 32],
    player_walk: [32, 0, 32, 32],
    enemy: [64, 0, 16, 16],
};
```

Each entry contains `[x, y, width, height]` in pixels.

## Controls

| Action | Control |
|--------|---------|
| Select region | Click and drag |
| Zoom | Mouse wheel |
| Pan | Alt + drag / Middle mouse |
| Move selection | Drag label |
| Rename | Double-click label |
| Copy single | Click coordinates |
| Copy all | Click "Copy All" button |

## License

MIT
