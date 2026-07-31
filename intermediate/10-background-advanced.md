# Background Advanced

> 8 properties

Advanced background control — colors, images, gradients, tiling, sizing, and positioning.

---

## Color & Image

---

## background-image

**Syntax:** `background-image: <image> | <gradient> | none`

Background image — tiled by default to fill the element.

**Values:**
- `none` — no image
- `url('image.jpg')` — image from a URL
- `linear-gradient(to right, red, blue)` — linear gradient
- `linear-gradient(135deg, #667eea 0%, #764ba2 100%)` — angled gradient with explicit stops
- `radial-gradient(circle, red, blue)` — radial gradient
- `conic-gradient(red, orange, yellow, green, blue)` — conic gradient
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add images behind content
- Create gradient backgrounds

**Example:**
```css
.hero {
  background-image: url('hero.jpg');
}

.card {
  background-image: linear-gradient(135deg, #667eea, #764ba2);
}
```

---

## Gradient

---

## repeating-linear-gradient()

**Syntax:** `background: repeating-linear-gradient(<angle>, <color-stops>)`

Repeating linear — tiles a gradient pattern.

**Values:**
- `90deg, #d63031 0px, #d63031 20px, #fdcb6e 20px, #fdcb6e 40px` — vertical stripes repeating every 40px

**Use Cases:**
- Create stripes and repeating patterns
- Build progress-bar textures

**Example:**
```css
.stripes {
  background: repeating-linear-gradient(45deg, #d63031 0, #d63031 10px, #fdcb6e 10px, #fdcb6e 20px);
}
```

---

## repeating-radial-gradient()

**Syntax:** `background: repeating-radial-gradient(<shape>, <color-stops>)`

Repeating radial — tiles a radial gradient pattern.

**Values:**
- `circle, #2d3436 0px, #2d3436 10px, #636e72 10px, #636e72 20px` — concentric rings

**Use Cases:**
- Create concentric ring patterns
- Build radar or target designs

**Example:**
```css
.target {
  background: repeating-radial-gradient(circle, #2d3436 0, #2d3436 10px, #636e72 10px, #636e72 20px);
}
```

---

## Repeat & Size

---

## background-repeat

**Syntax:** `background-repeat: repeat | repeat-x | repeat-y | no-repeat | space | round`

Tiling behavior — repeat, no-repeat, repeat-x, repeat-y, round, space.

**Values:**
- `repeat` — tile in both directions (default)
- `repeat-x` — tile horizontally only
- `repeat-y` — tile vertically only
- `no-repeat` — no tiling
- `space` — tile with even spacing between images
- `round` — tile and scale to fit the area
- `repeat space` — repeat horizontally, space vertically
- `repeat round` — repeat horizontally, round vertically
- `no-repeat space` — no-repeat horizontally, space vertically
- `inherit` — inherits from parent
- `initial` — sets to default (repeat)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control how background images tile
- Create seamless patterns

**Example:**
```css
.pattern {
  background-image: url('dot.png');
  background-repeat: round;
}

.hero {
  background-image: url('hero.jpg');
  background-repeat: no-repeat;
}
```

---

## background-position

**Syntax:** `background-position: <position> | <x> <y>`

Image placement — keyword pairs or x/y coordinates.

**Values:**
- `center` — centered (default)
- `top` — top edge
- `bottom` — bottom edge
- `left` — left edge
- `right` — right edge
- `20px` — single offset
- `50%` — single percentage
- `20px 40px` — x and y offsets
- `top right` — keyword pair
- `center bottom` — keyword pair
- `right 10px bottom 20px` — edge offsets
- `inherit` — inherits from parent
- `initial` — sets to default (0% 0%)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position background images precisely
- Pin accents to corners

**Example:**
```css
.badge {
  background-image: url('icon.png');
  background-position: right 10px bottom 10px;
  background-repeat: no-repeat;
}
```

---

## background-attachment

**Syntax:** `background-attachment: scroll | fixed | local`

Scroll behavior — fixed (viewport), local (scroll container), or scroll.

**Values:**
- `scroll` — scrolls with the page (default)
- `fixed` — stays fixed to the viewport
- `local` — scrolls with the element content
- `local scroll` — local vertically, scroll horizontally
- `inherit` — inherits from parent
- `initial` — sets to default (scroll)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create parallax effects
- Keep backgrounds fixed while content scrolls

**Example:**
```css
.parallax {
  background-image: url('mountains.jpg');
  background-attachment: fixed;
  background-size: cover;
}
```

---

## Clip & Origin

---

## background-clip

**Syntax:** `background-clip: border-box | padding-box | content-box | text`

Paint boundary — how far the background extends (border-box, padding-box, content-box, text).

**Values:**
- `border-box` — extends under the border (default)
- `padding-box` — stops at the padding edge
- `content-box` — stops at the content edge
- `text` — clipped to the text shape
- `inherit` — inherits from parent
- `initial` — sets to default (border-box)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create gradient text headings
- Keep backgrounds inside the content area

**Example:**
```css
.heading {
  background: linear-gradient(135deg, #fd79a8, #fdcb6e);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}
```

---

## background-origin

**Syntax:** `background-origin: border-box | padding-box | content-box`

Position origin — coordinate system for background-position.

**Values:**
- `padding-box` — relative to the padding box (default)
- `border-box` — relative to the border box
- `content-box` — relative to the content box
- `inherit` — inherits from parent
- `initial` — sets to default (padding-box)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align backgrounds to the content area
- Create offset background effects

**Example:**
```css
.card {
  background-image: linear-gradient(135deg, #d63031, #fdcb6e);
  background-origin: content-box;
  background-clip: content-box;
  padding: 10px;
}
```

---

**[View Example](../examples/intermediate/10-background-advanced/index.html)**

← **Previous Topic:** [Transform Functions](../intermediate/09-transform-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Flexbox Advanced](../intermediate/11-flexbox-advanced.md) →
