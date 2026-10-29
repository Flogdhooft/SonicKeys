# SonicKeys

An **interactive piano design project** built as part of the *[freeCodeCamp](https://www.freecodecamp.org/learn/responsive-web-design-v9/workshop-piano/step-1) **Responsive Web Design Certification** curriculum. This application models a realistic and styled piano keyboard, featuring media queries to ensure a smooth and responsive layout across different screen sizes[cite: 4].

---

## Key Features

* **Component Styling & Positioning :** Uses advanced CSS properties (`position: relative`, `float`, and `::after` pseudo-elements) to accurately structure the white and black piano keys.
* **Responsive Layout Design :** Integrates media queries (`max-width: 768px` and `max-width: 1199px`) to dynamically adapt the keyboard and container widths depending on the device.
* **Visual Effects & Interactions :** Applies hover effects (`:hover`) and drop shadows (`box-shadow`, `border-bottom`) to simulate the physical relief and key depression.

---

## Concepts & Technologies Applied

* **HTML5 :** Semantic page structure and integration of graphic elements.
* **CSS3 :** Box model (`box-sizing`), positioning, floats/layout, and shadows.
* **Responsive Web Design :** Media queries and adaptive units.
* **Pseudo-elements :** Utilization of `::after` for the precise rendering of black keys.

---

## Code Structure Example

Excerpt from the CSS stylesheet managing the main piano component and its interactions with media queries :

```css
.piano {
  position: relative;
  width: 992px;
  height: 290px;
  margin: 120px auto;
  padding: 90px 20px 0 20px;
  background-color: #a51d3a;
  border-radius: 16px;
  box-shadow: 0px 15px #661325;
}

.key:hover {
  background-color: rgb(236, 238, 255);
  border-bottom: 6px solid rgb(144, 149, 187);
  transform: translate(0, 2px);
}

[...]

@media (max-width: 768px) {
  .piano {
    width: 358px;
  }

  .keys {
    width: 318px;
  }

  .logo {
    width: 150px;
  }
}

@media (max-width: 1199px) and (min-width: 769px) {
  .piano {
    width: 675px;
  }

  .keys {
    width: 633px;
  }
}
