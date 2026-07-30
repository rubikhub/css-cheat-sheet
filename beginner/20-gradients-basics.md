# Gradients Basics

> 6 functions

Ways to create gradient backgrounds in CSS.

---

## linear-gradient()

**Syntax:** `linear-gradient(<angle>, <color-stops>)`

Transitions colors along a straight line.

**Values:**
- `to right` — left to right
- `to bottom` — top to bottom (default)
- `135deg` — diagonal
- `red, blue` — simple two-color
- `#6c5ce7, #a29bfe, #fd79a8` — multi-color
- `red 0%, blue 100%` — color stops
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create colorful hero sections
- Add depth to buttons and cards
- Build visual hierarchy

**Example:**
```css
.hero {
  background: linear-gradient(135deg, #6c5ce7, #a29bfe, #fd79a8);
}

.button {
  background: linear-gradient(to right, #00b894, #00cec9);
}

.subtle {
  background: linear-gradient(to bottom, #f5f5f5, #e0e0e0);
}
```

---

## radial-gradient()

**Syntax:** `radial-gradient(<shape>, <color-stops>)`

Radiates colors outward from a center point.

**Values:**
- `circle` — circular gradient
- `ellipse` — elliptical gradient (default)
- `at center` — centered position
- `at top left` — positioned at corner
- `red, blue` — simple two-color
- `#00b894, #00cec9, #0984e3` — multi-color
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create spotlight effects
- Add depth to circular elements
- Build radial backgrounds

**Example:**
```css
.spotlight {
  background: radial-gradient(circle at center, #fff, #000);
}

.circle {
  background: radial-gradient(circle, #00b894, #0984e3);
  border-radius: 50%;
}

.vignette {
  background: radial-gradient(ellipse at center, transparent 50%, rgba(0,0,0,0.5));
}
```

---

## conic-gradient()

**Syntax:** `conic-gradient(<color-stops>)`

Sweeps colors around a center point like a color wheel.

**Values:**
- `red, orange, yellow, green, blue` — color wheel
- `#ff6b6b, #feca57, #48dbfb` — custom colors
- `from 0deg` — starting angle
- `from 90deg` — rotated start
- `at center` — center position
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create color wheels and pie charts
- Add circular gradient effects
- Build progress indicators

**Example:**
```css
.color-wheel {
  background: conic-gradient(#ff6b6b, #feca57, #48dbfb, #ff9ff3);
  border-radius: 50%;
}

.pie {
  background: conic-gradient(#00b894 0% 50%, #0984e3 50% 100%);
  border-radius: 50%;
}

.progress {
  background: conic-gradient(#00b894 0% var(--progress), #e0e0e0 var(--progress) 100%);
}
```

---

**[View Example](../examples/beginner/20-gradients-basics/index.html)**

← **Previous Topic:** [Transition Basics](../beginner/19-transition-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Logical Properties](../beginner/21-logical-properties.md) →
