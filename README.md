# Area51 Waitlist Landing Page

A futuristic alien-themed waitlist landing page featuring an interactive 3D UFO built with Three.js.

## Features

- **Interactive 3D UFO**: Rotate, zoom, and drag a glowing UFO model using your mouse
- **Three.js 3D Graphics**: Powered by Three.js for smooth 3D rendering
- **OrbitControls**: Intuitive camera controls for interacting with the UFO
- **Bold headline**: "Unlock the Secrets of Area51"
- **Subheadline**: "Join the waitlist. First contact is coming."
- **Holographic signup form**: Styled like a futuristic console for name and email
- **Dark space background**: Stars and neon green/purple accents
- **Live countdown timer**: Shows time remaining until launch (set to 30 days)
- **Fully responsive**: Mobile-friendly design

## Installation

### Prerequisites
- Node.js and npm installed on your system

### Steps

1. **Install Three.js via npm:**
   ```bash
   npm install three
   ```

2. **The project structure should look like:**
   ```
   Area51-waitlist/
   ├── index.html
   ├── package.json
   ├── package-lock.json
   └── node_modules/
       └── three/
   ```

## How to Import Three.js

Three.js is imported as an ES6 module in the HTML file:

```javascript
// Import Three.js core library
import * as THREE from './node_modules/three/build/three.module.js';

// Import OrbitControls for camera interaction
import { OrbitControls } from './node_modules/three/examples/jsm/controls/OrbitControls.js';
```

## Usage

### For Local Development:

You need to serve the files with a local web server (due to ES6 module restrictions):

**Option 1: Using Python 3**
```bash
python3 -m http.server 8000
```

**Option 2: Using Node.js http-server**
```bash
npx http-server -p 8000
```

Then open your browser to `http://localhost:8000`

### For Production Deployment:

Upload all files including the `node_modules/three` directory to your web hosting service, or use a bundler like Webpack/Vite to bundle Three.js into your application.

## Interactive Features

- **Rotate**: Click and drag to rotate the UFO
- **Zoom**: Scroll mouse wheel to zoom in/out
- **Pan**: Right-click and drag to pan the camera

## Technologies

- **Three.js**: 3D graphics library for WebGL
- **OrbitControls**: Camera controls for 3D interaction
- **HTML5 Canvas**: For rendering 3D scene and space background
- **CSS3**: Animations, gradients, and holographic effects
- **Vanilla JavaScript**: Countdown timer, form handling, and 3D scene setup
- **LocalStorage**: Client-side demo for storing waitlist entries

## Code Structure

The `index.html` file contains:

1. **Three.js Setup**: Scene, camera, renderer, and lighting configuration
2. **UFO 3D Model**: Created with Three.js geometry (torus for disc, sphere for dome)
3. **OrbitControls**: Mouse/touch interaction setup
4. **Animation Loop**: Continuous rendering and UFO rotation
5. **Space Background**: Canvas-based starfield
6. **Holographic Form**: Styled signup form overlaying the 3D scene

## Customization

### Change Countdown Date
```javascript
// Modify the number of days in the future
targetDate.setDate(targetDate.getDate() + 30);
```

### Adjust UFO Appearance
```javascript
// Modify UFO materials and colors in the Three.js setup section
const discMaterial = new THREE.MeshStandardMaterial({
    color: 0x00ff7f,  // Change color
    emissive: 0x00ff7f,  // Change glow
    emissiveIntensity: 0.5  // Adjust glow intensity
});
```

### Production Considerations

For production use:
- Replace localStorage with a proper backend API
- Consider using a bundler (Webpack, Vite, Parcel) to optimize Three.js imports
- Implement proper form validation and security measures
- Add analytics tracking for waitlist conversions