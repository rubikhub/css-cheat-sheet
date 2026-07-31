# Background Advanced

> 12 properties

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

## aspect-ratio

**Syntax:** `aspect-ratio: auto | <ratio>`

Sets the preferred width/height ratio of a box.

**Values:**
- `auto` — replaced elements use their intrinsic ratio (default)
- `aspect-ratio: 1 / 1` — square
- `aspect-ratio: 16 / 9` — widescreen
- `aspect-ratio: 3 / 2` — photo ratio

**Use Cases:**
- Keep media frames responsive without fixed heights
- Reserve layout space before images load

**Example:**
```css
.video {
  width: 100%;
  aspect-ratio: 16 / 9;
}

.card-image {
  aspect-ratio: 4 / 3;
  object-fit: cover;
}
```

---

## object-fit

**Syntax:** `object-fit: fill | contain | cover | none | scale-down`

Controls how replaced content fits inside its box.

**Values:**
- `fill` — stretch to fill the box (default)
- `contain` — fit inside, preserving aspect ratio
- `cover` — fill the box, cropping overflow
- `none` — natural size, may overflow
- `scale-down` — like none or contain, whichever is smaller

**Use Cases:**
- Crop images to a fixed frame
- Letterbox videos in a set aspect ratio

**Example:**
```css
.avatar {
  width: 80px;
  height: 80px;
  border-radius: 50%;
  object-fit: cover;
}
```

---

## object-position

**Syntax:** `object-position: <position>`

Offsets the placed object within its content box.

**Values:**
- `50% 50%` — centered (default)
- `top` — align to the top edge
- `left` — align to the left edge
- `right 20px bottom 10px` — offset from edges

**Use Cases:**
- Choose which part of a cover image shows
- Focus a crop on a face or subject

**Example:**
```css
.banner {
  height: 300px;
  object-fit: cover;
  object-position: top;
}
```

---

## image-set()

**Syntax:** `background-image: image-set(<url> <resolution>, ...)`

Provides multiple image candidates for different resolutions.

**Values:**
- `image-set('photo@1x.png' 1x, 'photo@2x.png' 2x)` — device-pixel-ratio variants
- `image-set('photo-640.jpg' 640w, 'photo-1280.jpg' 1280w)` — width-based variants
- `image-set(url(a.avif) type('image/avif'), url(a.jpg))` — type filtering

**Use Cases:**
- Serve sharp backgrounds on retina screens
- Offer modern formats with fallbacks

**Example:**
```css
.hero {
  background-image: image-set(
    'hero-1x.jpg' 1x,
    'hero-2x.jpg' 2x
  );
}
```

---

**[View Example](../examples/intermediate/03-background-advanced/index.html)**

← **Previous Topic:** [Logic Matching Selectors](../intermediate/02-logic-matching-selectors.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography Advanced](../intermediate/04-typography-advanced.md) →
