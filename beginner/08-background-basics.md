# Background Basics

> 10 properties

Colors, images, tiling, sizing, clipping, and origin.

---

## Color & Image

---

## background-color

**Syntax:** `background-color: <color>`

Solid color — fills the element with a background color.

**Values:**
- `transparent` — no color (default)
- `red` — named color
- `currentColor` — matches text color
- `#ff5733` — hex color
- `#f00` — short hex
- `rgb(255, 0, 0)` — RGB color
- `rgba(255, 0, 0, 0.5)` — RGB with alpha
- `hsl(0, 100%, 50%)` — HSL color
- `hsla(0, 100%, 50%, 0.5)` — HSL with alpha
- `inherit` — inherits from parent
- `initial` — sets to default (transparent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create colored sections and cards
- Highlight interactive elements on hover

**Example:**
```css
.card {
  background-color: #f5f5f5;
}

.button:hover {
  background-color: #0066cc;
}
```

---

## background-image

**Syntax:** `background-image: none | <image>`

Background image — tiled by default to fill the element.

**Values:**
- `none` — no image (default)
- `url('image.jpg')` — image URL
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add background images to sections
- Create gradient backgrounds

**Example:**
```css
.hero {
  background-image: url('hero.jpg');
}

.gradient {
  background-image: linear-gradient(135deg, #667eea, #764ba2);
}
```

---

## background-repeat

**Syntax:** `background-repeat: repeat | no-repeat | repeat-x | repeat-y | round | space`

Tiling behavior — repeat, no-repeat, repeat-x, repeat-y, round, space.

**Values:**
- `repeat` — tile in both directions (default)
- `no-repeat` — no tiling
- `repeat-x` — tile horizontally only
- `repeat-y` — tile vertically only
- `round` — tile and resize to fit
- `space` — tile with even spacing
- `repeat space` — horizontal repeat, vertical space
- `inherit` — inherits from parent
- `initial` — sets to default (repeat)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create seamless pattern backgrounds
- Prevent image tiling

**Example:**
```css
.pattern {
  background-image: url('pattern.png');
  background-repeat: repeat;
}

.no-tiling {
  background-image: url('hero.jpg');
  background-repeat: no-repeat;
}
```

---

## background-size

**Syntax:** `background-size: auto | cover | contain | <length> | <percentage>`

Image dimensions — auto, cover (fill), or contain (fit).

**Values:**
- `auto` — intrinsic size (default)
- `cover` — scale to fill container
- `contain` — scale to fit inside container
- `200px` — fixed width
- `200px 100px` — fixed width and height
- `50%` — percentage of container
- `50% 75%` — width and height percentages
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make hero images fill entire sections
- Create responsive background images

**Example:**
```css
.hero {
  background-image: url('hero.jpg');
  background-size: cover;
  background-position: center;
}

.contained {
  background-image: url('logo.png');
  background-size: contain;
  background-repeat: no-repeat;
}
```

---

## background-position

**Syntax:** `background-position: <position>`

Image placement — keyword pairs or x/y coordinates.

**Values:**
- `top` — top edge
- `bottom` — bottom edge
- `left` — left edge
- `right` — right edge
- `center` — centered (default)
- `20px` — x offset
- `50%` — percentage
- `top right` — keyword pair
- `center bottom` — center horizontal, bottom vertical
- `right 10px bottom 20px` — precise positioning
- `inherit` — inherits from parent
- `initial` — sets to default (0% 0%)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center background images
- Pin decorative elements to corners

**Example:**
```css
.hero {
  background-position: center;
}

.corner-accent {
  background-position: right 20px bottom 10px;
}
```
---

## background

**Syntax:** `background: <bg-image> <position> <size> <repeat> <attachment> <clip> <origin> <color>`

Shorthand — combines color, image, position, repeat, size, and attachment.

**Values:**
- `red` — just color
- `url('image.jpg')` — just image
- `center` — just position
- `no-repeat` — just repeat
- `fixed` — just attachment
- `url('image.jpg') center no-repeat` — multiple values
- `red url('image.jpg') center/cover no-repeat` — full shorthand
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify background declarations
- Set multiple background properties at once

**Example:**
```css
.hero {
  background: url('hero.jpg') center/cover no-repeat;
}

.card {
  background: #f5f5f5 url('pattern.png') repeat;
}
```

---

**[View Example](../examples/beginner/08-background-basics/index.html)**

← **Previous Topic:** [Color Functions Basics](../beginner/07-color-functions-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography Basics](../beginner/09-typography-basics.md) →
