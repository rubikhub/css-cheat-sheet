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

## repeating-linear-gradient()

**Syntax:** `repeating-linear-gradient(<angle>, <color-stops>)`

Tiles a linear gradient pattern.

**Values:**
- `0deg, red 0px, red 10px, blue 10px, blue 20px` — striped pattern
- `45deg, #667eea 0px, #667eea 8px, transparent 8px, transparent 16px` — diagonal stripes
- `90deg, #d63031 0px, #d63031 20px, #fdcb6e 20px, #fdcb6e 40px` — vertical bars
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create striped patterns
- Build repeating backgrounds
- Add texture to elements

**Example:**
```css
.stripes {
  background: repeating-linear-gradient(
    45deg,
    #667eea 0px,
    #667eea 8px,
    transparent 8px,
    transparent 16px
  );
}

.vertical-bars {
  background: repeating-linear-gradient(
    90deg,
    #d63031 0px,
    #d63031 20px,
    #fdcb6e 20px,
    #fdcb6e 40px
  );
}
```

---

## repeating-radial-gradient()

**Syntax:** `repeating-radial-gradient(<shape>, <color-stops>)`

Tiles a radial gradient pattern.

**Values:**
- `circle, #2d3436 0px, #2d3436 10px, #636e72 10px, #636e72 20px` — concentric circles
- `ellipse, red 0px, red 5px, blue 5px, blue 10px` — radial stripes
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create concentric ring patterns
- Build target-like designs
- Add radial texture

**Example:**
```css
.concentric {
  background: repeating-radial-gradient(
    circle,
    #2d3436 0px,
    #2d3436 10px,
    #636e72 10px,
    #636e72 20px
  );
}

.target {
  background: repeating-radial-gradient(
    circle,
    red 0px,
    red 5px,
    white 5px,
    white 10px
  );
}
```

---

## repeating-conic-gradient()

**Syntax:** `repeating-conic-gradient(<color-stops>)`

Tiles a conic gradient pattern.

**Values:**
- `red 0deg 10deg, blue 10deg 20deg` — alternating wedges
- `#ff6b6b 0deg 30deg, #feca57 30deg 60deg` — color wheel sections
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create checkerboard patterns
- Build color wheel designs
- Add radial striped textures

**Example:**
```css
.checkerboard {
  background: repeating-conic-gradient(
    #000 0% 25%,
    #fff 0% 50%
  ) 50% / 20px 20px;
}

.color-wheel {
  background: repeating-conic-gradient(
    red 0deg 30deg,
    orange 30deg 60deg,
    yellow 60deg 90deg,
    green 90deg 120deg,
    blue 120deg 150deg,
    purple 150deg 180deg
  );
  border-radius: 50%;
}
```

---

**[View Example](../examples/beginner/20-gradients-basics/index.html)**

← **Previous Topic:** [Transition Basics](../beginner/19-transition-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Logical Properties](../beginner/21-logical-properties.md) →
