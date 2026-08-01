

## Attribute selectors

`[attribute~="value"]`

- `[class~="active"]` — word list match
- `[data-role="button"]` — custom attributes

## background-color

**Syntax:** `background-color: <color>`

Solid color — fills the element with a background color.

**Values:**

- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property



---

## Gradient

---

## linear-gradient()

**Syntax:** `linear-gradient(<angle>, <color-stops>)`

Linear gradient — transitions colors along a straight line.

**Values:**
- `to right` — left to right
- `to bottom` — top to bottom
- `135deg` — diagonal
- `red, blue` — simple two-color
- `#6c5ce7, #a29bfe, #fd79a8` — multi-color
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create colorful hero sections
- Add depth to buttons and cards

**Example:**
```css
.hero {
  background: linear-gradient(135deg, #6c5ce7, #a29bfe, #fd79a8);
}

.button {
  background: linear-gradient(to right, #00b894, #00cec9);
}
```

---

## radial-gradient()

**Syntax:** `radial-gradient(<shape>, <color-stops>)`

Radial gradient — radiates colors outward from a center point.

**Values:**
- `circle` — circular gradient
- `ellipse` — elliptical gradient (default)
- `at center` — centered position
- `red, blue` — simple two-color
- `#00b894, #00cec9, #0984e3` — multi-color
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create spotlight effects
- Add depth to circular elements

**Example:**
```css
.spotlight {
  background: radial-gradient(circle at center, #fff, #000);
}

.circle {
  background: radial-gradient(circle, #00b894, #0984e3);
  border-radius: 50%;
}
```

---

## conic-gradient()

**Syntax:** `conic-gradient(<color-stops>)`

Conic gradient — sweeps colors around a center point like a color wheel.

**Values:**
- `red, orange, yellow, green, blue` — color wheel
- `#ff6b6b, #feca57, #48dbfb` — custom colors
- `from 0deg` — starting angle
- `at center` — center position
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create color wheels and pie charts
- Add circular gradient effects

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
```



## font-style
- `oblique` — slanted (synthetic)
- `oblique 14deg` — oblique with specific angle

## text-shadow

**Syntax:** `text-shadow: none | <shadow-list>`

Text shadow — adds drop shadow effect to text.

**Values:**
- `none` — no shadow (default)
- `2px 2px #555` — offset + color
- `1px 1px 2px rgba(0,0,0,0.5)` — offset + blur + color
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add depth to headings
- Create retro text effects

**Example:**
```css
h1 {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}
```



## Outline

---

## outline

**Syntax:** `outline: <width> <style> <color>`

Shorthand — sets outline width, style, and color.

**Values:**
- `2px solid #0066cc` — width style color
- `none` — no outline (default)
- `3px dashed red` — emphasis outline
- `inherit` — inherits from parent
- `initial` — sets to default (medium none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create focus indicators for accessibility
- Add emphasis without affecting layout

**Example:**
```css
button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}
```

---

## outline-offset

**Syntax:** `outline-offset: <length>`

Outline spacing — adds space between border and outline.

**Values:**
- `2px` — small gap
- `4px` — larger gap
- `0` — no gap (default)
- `-2px` — inset outline
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create focus rings with visible gap
- Style accessible interactive elements

**Example:**
```css
button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 3px;
}
```

---


## empty-cells

**Syntax:** `empty-cells: show | hide`

Empty cell visibility — show or hide borders/backgrounds.

**Values:**
- `show` — show empty cells (default)
- `hide` — hide empty cells
- `inherit` — inherits from parent
- `initial` — sets to default (show)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Hide empty table cells
- Create cleaner table layouts

**Example:**
```css
table {
  empty-cells: hide;
}
```

---




## vertical-align

**Syntax:** `vertical-align: baseline | sub | super | text-top | text-bottom | middle | top | bottom`

Vertical alignment — aligns inline/table cell content.

**Values:**
- `baseline` — align to baseline (default)
- `sub` — subscript
- `super` — superscript
- `text-top` — align to text top
- `text-bottom` — align to text bottom
- `middle` — vertical middle
- `top` — align to top
- `bottom` — align to bottom
- `inherit` — inherits from parent
- `initial` — sets to default (baseline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align icons with text
- Position table cell content

**Example:**
```css
.icon {
  vertical-align: middle;
}

td {
  vertical-align: top;
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
---

## Archived Duplicates

Cards removed from the intermediate level because they duplicate beginner-level content.

<!-- source: intermediate/06-state-pseudo-classes.md -->
## :hover

**Syntax:** `:hover`

Targets elements when the pointer is over them.

**Values:**
- `a:hover` — links on hover
- `button:hover` — buttons on hover
- `.card:hover` — cards on hover

**Use Cases:**
- Add hover effects to interactive elements
- Provide visual feedback

**Example:**
```css
a:hover {
  color: red;
  text-decoration: underline;
}

button:hover {
  background: darkblue;
  color: white;
}
```

---

<!-- source: intermediate/11-flexbox-advanced.md -->
## display

**Syntax:** `display: flex | inline-flex`

Flex container — enables flex layout on children.

**Values:**
- `flex` — block-level flex container
- `inline-flex` — inline-level flex container
- `inherit` — inherits from parent
- `initial` — sets to default (inline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create flexible layouts
- Align items in a row or column

**Example:**
```css
.container {
  display: flex;
}
```

---

<!-- source: intermediate/11-flexbox-advanced.md -->
## flex-direction

**Syntax:** `flex-direction: row | row-reverse | column | column-reverse`

Main axis direction — horizontal or vertical layout.

**Values:**
- `row` — horizontal, left to right (default)
- `row-reverse` — horizontal, right to left
- `column` — vertical, top to bottom
- `column-reverse` — vertical, bottom to top
- `inherit` — inherits from parent
- `initial` — sets to default (row)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create horizontal navigation
- Stack items vertically

**Example:**
```css
.nav {
  flex-direction: row;
}

.sidebar {
  flex-direction: column;
}
```

---

<!-- source: intermediate/11-flexbox-advanced.md -->
## flex-wrap

**Syntax:** `flex-wrap: nowrap | wrap | wrap-reverse`

Wrapping behavior — whether items wrap to new lines.

**Values:**
- `nowrap` — all items on one line (default)
- `wrap` — items wrap to new lines
- `wrap-reverse` — items wrap upward
- `inherit` — inherits from parent
- `initial` — sets to default (nowrap)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create responsive grids
- Prevent items from overflowing

**Example:**
```css
.card-grid {
  display: flex;
  flex-wrap: wrap;
}
```

---

<!-- source: intermediate/11-flexbox-advanced.md -->
## flex-grow

**Syntax:** `flex-grow: <number>`

Growth factor — how much an item grows relative to siblings.

**Values:**
- `0` — don't grow (default)
- `1` — grow equally
- `2` — grow twice as much
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make one item fill remaining space
- Create proportional columns

**Example:**
```css
.main {
  flex-grow: 1;
}

.sidebar {
  flex-grow: 0;
}
```

---

<!-- source: intermediate/11-flexbox-advanced.md -->
## flex-shrink

**Syntax:** `flex-shrink: <number>`

Shrink factor — how much an item shrinks when space is limited.

**Values:**
- `0` — don't shrink
- `1` — shrink equally (default)
- `2` — shrink twice as much
- `inherit` — inherits from parent
- `initial` — sets to default (1)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent items from shrinking
- Control which items compress first

**Example:**
```css
.logo {
  flex-shrink: 0;
}

.title {
  flex-shrink: 1;
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## background-color

**Syntax:** `background-color: <color> | transparent`

Solid color — fills the element with a background color.

**Values:**
- `transparent` — no background color
- `red` — named color
- `currentColor` — uses the element's text color
- `#ff5733` — hex color
- `#f00` — shorthand hex
- `rgb(255, 0, 0)` — RGB color
- `rgba(255, 0, 0, 0.5)` — RGB color with alpha
- `hsl(0, 100%, 50%)` — HSL color
- `hsla(0, 100%, 50%, 0.5)` — HSL color with alpha
- `inherit` — inherits from parent
- `initial` — sets to default (transparent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set brand and UI colors
- Layer translucent overlays with rgba() or hsla()

**Example:**
```css
.button {
  background-color: #6c5ce7;
}

.button:hover {
  background-color: rgba(108, 92, 231, 0.5);
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## background

**Syntax:** `background: <color> | <image> <position>/<size> <repeat> <attachment>`

Shorthand — combines color, image, position, repeat, size, and attachment.

**Values:**
- `red` — color only
- `url('image.jpg')` — image only
- `center` — position only
- `no-repeat` — repeat only
- `fixed` — attachment only
- `url('image.jpg') center no-repeat` — image with position and repeat
- `red url('image.jpg') center/cover no-repeat` — full shorthand
- `inherit` — inherits from parent
- `initial` — sets to default (transparent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set complete backgrounds in one line
- Combine gradients with fallback colors

**Example:**
```css
.hero {
  background: url('hero.jpg') center/cover no-repeat;
}

.banner {
  background: #6c5ce7 url('pattern.png') no-repeat;
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## linear-gradient()

**Syntax:** `background: linear-gradient(<angle>, <color-stops>)`

Linear gradient — transitions colors along a straight line.

**Values:**
- `to right, red, blue` — gradient from left to right
- `135deg, #667eea 0%, #764ba2 100%` — angle with explicit color stops
- `135deg, #6c5ce7, #a29bfe, #fd79a8` — diagonal gradient through three colors
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create smooth color transitions
- Build layered gradient backgrounds

**Example:**
```css
.hero {
  background: linear-gradient(135deg, #6c5ce7, #a29bfe, #fd79a8);
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## radial-gradient()

**Syntax:** `background: radial-gradient(<shape> <size> at <position>, <color-stops>)`

Radial gradient — radiates colors outward from a center point.

**Values:**
- `circle, red, blue` — circular gradient
- `circle, #00b894, #00cec9, #0984e3` — circular gradient through three colors
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create spotlight or glow effects
- Add depth to buttons

**Example:**
```css
.button {
  background: radial-gradient(circle, #00b894, #00cec9, #0984e3);
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## conic-gradient()

**Syntax:** `background: conic-gradient(<from-angle> at <position>, <color-stops>)`

Conic gradient — sweeps colors around a center point like a color wheel.

**Values:**
- `#ff6b6b, #feca57, #48dbfb, #ff9ff3, #ff6b6b` — color wheel sweep
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Build color wheels and donut charts
- Create rotating-hue effects

**Example:**
```css
.wheel {
  background: conic-gradient(#ff6b6b, #feca57, #48dbfb, #ff9ff3, #ff6b6b);
  border-radius: 50%;
}
```

---

<!-- source: intermediate/10-background-advanced.md -->
## background-size

**Syntax:** `background-size: auto | <length> | <percentage> | cover | contain`

Image dimensions — auto, cover (fill), or contain (fit).

**Values:**
- `auto` — natural image size (default)
- `cover` — fills the area, cropping as needed
- `contain` — fits entirely inside
- `200px` — single width value
- `200px 100px` — width and height
- `50%` — single percentage
- `50% 75%` — width and height percentages
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Cover backgrounds in hero sections
- Fit logos and icons cleanly

**Example:**
```css
.hero {
  background: url('image.jpg') center no-repeat;
  background-size: cover;
}

.icon {
  background: url('icon.png') no-repeat;
  background-size: contain;
}
```

---

<!-- source: intermediate/07-border-advanced.md -->
## border-width

**Syntax:** `border-width: <length> | thin | medium | thick`

Thickness — sets the width of the border on all sides.

**Values:**
- `thin` — thin border
- `medium` — medium border
- `thick` — thick border
- `1px` — pixel-based width
- `0.5em` — em-based width
- `0` — no border
- `inherit` — inherits from parent
- `initial` — sets to default (medium)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control border thickness
- Remove a border edge

**Example:**
```css
.card {
  border-style: solid;
  border-width: 2px;
}
```

---

<!-- source: intermediate/07-border-advanced.md -->
## border-color

**Syntax:** `border-color: <color>`

Line color — sets the color of the border on all sides.

**Values:**
- `currentColor` — matches the element's text color
- `red` — named color
- `transparent` — invisible border
- `#ff5733` — hex color
- `rgb(255, 0, 0)` — rgb color
- `rgba(255, 0, 0, 0.5)` — rgba color with opacity
- `hsl(0, 100%, 50%)` — hsl color
- `inherit` — inherits from parent
- `initial` — sets to default (currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Color a border to match a brand
- Create invisible borders for layout alignment

**Example:**
```css
.card {
  border-style: solid;
  border-color: #6c5ce7;
}
```

---

<!-- source: intermediate/07-border-advanced.md -->
## border-collapse

**Syntax:** `border-collapse: separate | collapse`

Table model — collapses adjacent borders or keeps them separate.

**Values:**
- `separate` — keep borders separate (default)
- `collapse` — merge adjacent borders
- `inherit` — inherits from parent
- `initial` — sets to default (separate)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Clean up tables with double borders
- Create compact table layouts

**Example:**
```css
table {
  border-collapse: collapse;
}
```

---

<!-- source: intermediate/07-border-advanced.md -->
## border-spacing

**Syntax:** `border-spacing: <length>`

Cell gap — sets the space between cell borders in the separate model.

**Values:**
- `6px` — equal horizontal and vertical spacing
- `0` — no spacing (default)
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add breathing room between table cells
- Style data tables without merged borders

**Example:**
```css
table {
  border-collapse: separate;
  border-spacing: 6px;
}
```

---

<!-- source: intermediate/13-counters-and-markers.md -->
## list-style-image

**Syntax:** `list-style-image: <url> | none`

Marker image — uses an image as the list marker.

**Values:**
- `none` — no image marker
- `url("check.svg")` — custom SVG marker
- `url("arrow.png")` — custom PNG marker
- `url("bullet.gif")` — custom GIF marker
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Replace bullets with custom icons
- Use brand-specific markers

**Example:**
```css
li {
  list-style-image: url("check.svg");
}
```

---

<!-- source: intermediate/13-counters-and-markers.md -->
## list-style-position

**Syntax:** `list-style-position: outside | inside`

Marker position — whether the marker is inside or outside the content box.

**Values:**
- `outside` — marker outside the content box (default)
- `inside` — marker inside the content box
- `inherit` — inherits from parent
- `initial` — sets to default (outside)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep markers outside list text
- Wrap markers with text in indented lists

**Example:**
```css
ul {
  list-style-position: inside;
}
```

---

<!-- source: intermediate/13-counters-and-markers.md -->
## list-style

**Syntax:** `list-style: <type> | <type> <position> | <image> <position>`

List style shorthand — combines type, position, and image.

**Values:**
- `none` — remove markers
- `disc outside` — disc marker outside
- `square inside` — square marker inside
- `url("check.svg") outside` — image marker outside
- `decimal-leading-zero inside` — numbered marker inside
- `lower-roman url("marker.png") outside` — combined type and image
- `inherit` — inherits from parent
- `initial` — sets to default (disc outside none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reset list styles quickly
- Set complete marker styling in one line

**Example:**
```css
.nav {
  list-style: none;
}

.toc {
  list-style: decimal inside;
}
```

---

<!-- source: intermediate/02-attribute-selectors.md -->
## [attr]

**Syntax:** `[attr]`

Targets elements that have the specified attribute.

**Values:**
- `[title]` — elements with a title attribute
- `[href]` — elements with an href attribute
- `[data-active]` — elements with a data-active attribute

**Use Cases:**
- Style elements that have a specific attribute
- Target elements by data attributes

**Example:**
```css
[href] {
  color: blue;
}

[data-active] {
  font-weight: bold;
}
```

---

<!-- source: intermediate/02-attribute-selectors.md -->
## [attr="value"]

**Syntax:** `[attr="value"]`

Targets elements with an exact attribute value match.

**Values:**
- `[type="text"]` — text inputs
- `[type="email"]` — email inputs
- `[type="password"]` — password inputs
- `[data-status="active"]` — elements with an active status

**Use Cases:**
- Style inputs by type
- Target elements by exact data values

**Example:**
```css
[type="text"] {
  border: 2px solid blue;
}

[type="email"] {
  border: 2px solid green;
}
```

---

<!-- source: intermediate/12-grid-advanced.md -->
## display

**Syntax:** `display: grid | inline-grid`

Grid container — enables grid layout on children.

**Values:**
- `grid` — block-level grid container
- `inline-grid` — inline-level grid container
- `inherit` — inherits from parent
- `initial` — sets to default (inline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create complex page layouts
- Build responsive card grids

**Example:**
```css
.container {
  display: grid;
}
```

---

<!-- source: intermediate/12-grid-advanced.md -->
## gap

**Syntax:** `gap: <length> | <percentage>`

Gutters — sets spacing between grid rows and columns.

**Values:**
- `0` — no gap (default)
- `10px` — fixed gap
- `1rem 2rem` — row-gap column-gap
- `5% 10%` — percentage gaps
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create consistent spacing in grids
- Replace margins on grid children

**Example:**
```css
.grid {
  display: grid;
  gap: 20px;
}
```

---

<!-- source: intermediate/01-structural-pseudo-classes.md -->
## :first-child

**Syntax:** `:first-child`

Selects the first child element of its parent.

**Values:**
- `li:first-child` — first list item
- `.item:first-child` — first .item element
- `.card:first-child` — first card
- `p:first-child` — first paragraph

**Use Cases:**
- Style the first element in a group
- Remove the top border of a first child

**Example:**
```css
li:first-child {
  font-weight: bold;
}

p:first-child {
  font-size: 1.2em;
}

.card:first-child {
  background: lightyellow;
}
```

---

<!-- source: intermediate/01-structural-pseudo-classes.md -->
## :last-child

**Syntax:** `:last-child`

Selects the last child element of its parent.

**Values:**
- `li:last-child` — last list item
- `.item:last-child` — last .item element
- `.card:last-child` — last card
- `p:last-child` — last paragraph

**Use Cases:**
- Style the last element in a group
- Remove the bottom border of a last child

**Example:**
```css
li:last-child {
  font-weight: bold;
  color: red;
}

.item:last-child {
  border-bottom: 2px solid green;
}

p:last-child {
  margin-bottom: 0;
}
```

---

<!-- source: intermediate/01-structural-pseudo-classes.md -->
## :nth-last-child(an+b)

**Syntax:** `:nth-last-child(an+b)`

Selects elements based on position from the end.

**Values:**
- `1` — last element
- `odd` — odd positions from the end
- `even` — even positions from the end
- `3n` — every third from the end
- `-n+2` — last two elements

**Use Cases:**
- Style elements near the end of a group
- Create reverse counting patterns

**Example:**
```css
li:nth-last-child(1) {
  color: red;
}

li:nth-last-child(odd) {
  background: lightgray;
}

li:nth-last-child(-n+2) {
  border-right: 3px solid blue;
}
```

---

<!-- source: intermediate/01-structural-pseudo-classes.md -->
## :only-child

**Syntax:** `:only-child`

Selects an element that is the only child of its parent.

**Values:**
- `li:only-child` — only list item
- `.item:only-child` — only .item element
- `.card:only-child` — only card
- `p:only-child` — only paragraph

**Use Cases:**
- Style single items differently
- Adjust spacing for solo elements

**Example:**
```css
li:only-child {
  font-weight: bold;
  color: blue;
}

.item:only-child {
  border: 2px solid green;
}

p:only-child {
  font-size: 1.2em;
}
```

---

<!-- source: intermediate/17-ui-and-scroll.md -->
## cursor

**Syntax:** `cursor: auto | default | pointer | text | move | url(<url>), <fallback>`

Cursor — specifies the mouse cursor appearance.

**Values:**
- `auto` — browser chooses based on context (default)
- `default` — standard arrow
- `pointer` — hand pointer for links and buttons
- `text` — text caret for selection
- `move` — drag/move cursor
- `not-allowed` — indicates a disabled action
- `grab` — draggable element
- `zoom-in` — zoom available
- `url("cursor.svg"), auto` — custom cursor with fallback
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Signal clickable elements
- Show drag affordances

**Example:**
```css
a,
button {
  cursor: pointer;
}

.draggable {
  cursor: grab;
}
```

---

<!-- source: intermediate/03-combinators-advanced.md -->
## ~ (General Sibling)

**Syntax:** `A ~ B`

Targets all siblings that come after the element.

**Values:**
- `h2 ~ p` — paragraphs after an h2
- `.active ~ .item` — items after an active element
- `.checked ~ label` — labels after a checked input
- `.selected ~ .option` — options after a selected element

**Use Cases:**
- Style all siblings following an element
- Apply a shared style to a group after a trigger

**Example:**
```css
h2 ~ p {
  color: gray;
}

.active ~ .item {
  opacity: 0.5;
}
```

---

<!-- source: intermediate/03-combinators-advanced.md -->
## + (Adjacent Sibling)

**Syntax:** `A + B`

Targets the immediately following sibling.

**Values:**
- `h2 + p` — paragraph right after an h2
- `.active + .item` — item right after an active element
- `.checked + label` — label right after a checked input
- `.selected + .option` — option right after a selected element

**Use Cases:**
- Style the first element after a heading
- Style the label next to a checked input

**Example:**
```css
h2 + p {
  font-weight: bold;
}

.checked + label {
  color: blue;
}
```

---

<!-- source: intermediate/03-combinators-advanced.md -->
## > (Child)

**Syntax:** `A > B`

Targets direct children only.

**Values:**
- `.nav > li` — direct list items in a nav
- `.container > .item` — direct item children
- `.list > li` — direct list items
- `.grid > div` — direct div children

**Use Cases:**
- Target only direct children, not nested ones
- Style the top level of nested lists

**Example:**
```css
.nav > li {
  display: inline-block;
}

.container > .item {
  margin-bottom: 1rem;
}
```

---

<!-- source: intermediate/03-combinators-advanced.md -->
## (space) Descendant

**Syntax:** `A B`

Targets all descendants at any depth.

**Values:**
- `nav a` — all links inside a nav
- `.container p` — all paragraphs inside a container
- `.card h2` — all headings inside a card
- `.list li` — all list items inside a list

**Use Cases:**
- Style all nested elements of a type
- Apply styles to deeply nested content

**Example:**
```css
nav a {
  text-decoration: none;
}

.container p {
  margin-bottom: 1rem;
}
```

---

