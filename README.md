# Dog Animation with Interactive Control

## 🚀 About the Project
This project demonstrates an **interactive animated dog** that moves and reacts based on directional input. The animation is crafted using **HTML**, **CSS**, and **JavaScript**, showcasing dynamic movement of the dog’s legs, tail, and overall body. The logic includes:
- Precise positioning of body parts for smooth animations.
- Dynamic direction control for the dog’s movement.

---

## 🛠️ Technologies Used

- **HTML**: For the structure of the animated dog and its parts.
- **CSS**: To style and animate the dog's movements.
- **JavaScript**: Implements the animation logic and interactive controls.

---

## 📂 Project Structure

```plaintext
├── index.html    # Contains the structure of the animated dog
├── style.css     # Handles the styling and animation details
├── script.js     # Contains logic for movement and interactive controls
```

### **HTML (index.html)**
The HTML file defines the structure of the dog, including its body, legs, and tail. It also contains marker elements for movement debugging or tracking.

### **CSS (style.css)**
CSS is responsible for the appearance of the dog and its smooth animation. Key components include:
- `@keyframes` for animation sequences.
- Styling for `.dog`, `.body`, `.tail`, and `.leg` elements.

### **JavaScript (script.js)**
JavaScript drives the logic for interactive animations. Key features include:
- Dynamic adjustment of the dog's movement based on directional inputs.
- Animation frames for realistic leg and tail motions.

---

## 🔑 Features

1. **Interactive Directional Movement**: The dog adjusts its direction and moves accordingly.
2. **Realistic Animations**: Smooth transitions for the legs and tail mimic natural movement.
3. **Modular Design**: The code is organized to allow easy modifications and extensions.

---

## 🧑‍💻 Code Overview

### Initialization
The `init` function initializes key elements and sets up the animation logic.

```javascript
function init() {
  const elements = {
    body: document.querySelector('.wrapper'),
    dog: document.querySelector('.dog'),
    marker: document.querySelectorAll('.marker'),
  };

  const animationFrames = {
    rotate: [[0], [1], [2], [3], [5], [3, 'f'], [2, 'f'], [1, 'f']]
  };

  const directionConversions = {
    360: 'up', 45: 'upright', 90: 'right', 135: 'downright',
    180: 'down', 225: 'downleft', 270: 'left', 315: 'upleft',
  };
}
```

### Leg Position Logic
The `partPositions` array defines frame-by-frame positioning for the dog’s legs, ensuring seamless walking animations.

```javascript
const partPositions = [
  { leg1: { x: 26, y: 43 }, leg2: { x: 54, y: 43 }, ... },
  { leg1: { x: 33, y: 56 }, leg2: { x: 55, y: 56 }, ... },
  // Additional frames...
];
```

### Tail and Direction Control
The script dynamically rotates and aligns the dog's body based on directional input using predefined animation frames and directional mappings.

---

## 🎨 CSS Highlights
The CSS file defines the animations and styles for a visually appealing and responsive experience. Key sections include:
- **Dog Styling**: `.dog`, `.body`, `.tail`, `.leg`.
- **Animations**: Smooth transitions for walking and tail wagging.

```css
@keyframes walk {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(45deg); }
}
```

---

## 🖥️ How to Run

1. Clone the repository or download the project files.
2. Open `index.html` in any modern browser.
3. Observe and interact with the animation.

---

## 📝 Customization
To tweak animations or controls:
- Modify `partPositions` in `script.js` for leg positions.
- Adjust `@keyframes` in `style.css` for animation speeds.
- Update HTML structure in `index.html` to add or remove components.

---

## 💡 Future Enhancements

- Add keyboard controls for more interactivity.
- Include sound effects to enhance the user experience.
- Create a mobile-responsive version.

---

## Live Link
<https://dog-follow-ghost.vercel.app/>
![My Image](https://i.ibb.co/kx3ZbSh/Dog-and-5-more-pages-Personal-Microsoft-Edge-2024-01-31-02-16-47.gif)
