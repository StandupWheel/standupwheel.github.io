# Standup Wheel

A modern, interactive spinning wheel application for randomly selecting names. Perfect for facilitating standup meetings, choosing speakers, or any situation where you need to randomly pick from a list of names.

## Features

- **Interactive Wheel**: Spin a colorful, animated wheel to randomly select a name
- **Name Management**: Add, edit, or remove names from the list
- **Persistent Storage**: Automatically saves your name list to browser local storage
- **Configuration Support**: Load default names and spin settings from an optional config file
- **Responsive Design**: Works seamlessly on desktop, tablet, and mobile devices
- **Dark Theme**: Easy on the eyes with a beautiful dark color scheme
- **Auto-Remove**: Selected names are automatically removed from the wheel
- **Smooth Animations**: Easing animations and polished visual feedback

## Usage

### Basic Usage

1. Enter names in the text area (one per line)
2. Click the **Save** button to store your list
3. Click the wheel to spin and select a random name
4. The selected name appears in a dialog
5. Choose to spin again or close the dialog
6. Each spin removes the selected name from the list

### Buttons

- **Save**: Saves the current name list to browser storage
- **Refresh**: Resets to the default configuration (if available)

## Configuration

The application can load default names and spin settings from a `config/wheel.json` file:

```json
{
  "names": ["Alice", "Bob", "Charlie", "Diana", "Eve"],
  "spinDurationSeconds": 3,
  "spinSpeed": 5
}
```

**Configuration Options:**
- `names`: Array of names to display on the wheel
- `spinDurationSeconds`: Animation duration in seconds (default: 3)
- `spinSpeed`: Number of full rotations during spin (default: 5, range: 0.5-50)

The app looks for config in:
- `/config/wheel.json`
- `config/wheel.json`
- `wheel.json`

## Technical Details

- **Single File**: All HTML, CSS, and JavaScript in one file
- **No Dependencies**: Pure vanilla JavaScript with no external libraries
- **Canvas Drawing**: Custom wheel rendering using HTML5 Canvas
- **Local Storage**: Uses browser localStorage to persist name lists
- **Responsive Layout**: Flexbox-based responsive design
- **Smooth Animations**: RequestAnimationFrame-based spinning animation with easing

### Color Scheme

The application uses a carefully chosen color palette with intelligent color rotation to ensure adjacent segments on the wheel never share the same color:

- Primary colors: Blue (#4285F4), Red (#EA4335), Green (#34A853), Yellow (#FBBC05)
- Dark background with high contrast text for readability

## Browser Support

Works on all modern browsers that support:
- HTML5 Canvas
- localStorage
- CSS Grid/Flexbox
- HTML5 Dialog element (with fallback to `alert()`)

## Installation

Simply open `index.html` in a web browser. No installation or build process required.

For GitHub Pages hosting, the repository can be deployed directly since it's a static site.

## Default Configuration

The application ships with default names included:
- James
- Sophia
- Michael
- Emma
- David

These can be overridden by creating a `config/wheel.json` file or by manually entering names in the application.

## Keyboard & Interaction

- **Spin**: Click anywhere on the wheel
- **Edit Names**: Type or paste into the text area
- **Responsive**: Works with touch on mobile devices

## License

This project is available on GitHub Pages.
