# Advanced Visual Effects

> 7 properties

Backdrop filters, blend modes, and CSS masking.

---

## backdrop-filter

**Syntax:** `backdrop-filter: <filter-function-list> | none`

Applies filter effects to the area behind an element (frosted glass effect).

**Values:**
- `none` — no backdrop filter (default)
- `blur(10px)` — gaussian blur on the backdrop
- `brightness(150%)` — adjusts backdrop brightness
- `contrast(200%)` — adjusts backdrop contrast
- `grayscale(100%)` — converts backdrop to grayscale
- `blur(5px) brightness(150%)` — combines multiple filters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create frosted glass cards
- Blur content behind modals

**Example:**
```css
.glass-card {
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  background: rgba(255, 255, 255, 0.25);
  border: 1px solid rgba(255, 255, 255, 0.3);
}
```

---

## mix-blend-mode

**Syntax:** `mix-blend-mode: normal | multiply | screen | overlay | darken | lighten | color-dodge | color-burn | hard-light | soft-light | difference | exclusion | hue | saturation | color | luminosity`

Determines how an element's content blends with what's behind it.

**Values:**
- `normal` — no blending (default)
- `multiply` — multiplies colors, darkens
- `screen` — inverts multiply, lightens
- `overlay` — combines multiply and screen
- `darken` — keeps the darker color
- `lighten` — keeps the lighter color
- `color-dodge` — brightens the backdrop
- `color-burn` — darkens the backdrop
- `hard-light` — strong contrast blend
- `soft-light` — subtle contrast blend
- `difference` — subtracts colors
- `exclusion` — like difference, softer
- `hue` — uses element hue with backdrop saturation/luminosity
- `saturation` — uses element saturation
- `color` — uses element hue and saturation
- `luminosity` — uses element luminosity
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Blend text or shapes over images
- Create textured overlays

**Example:**
```css
.text-over-image {
  mix-blend-mode: multiply;
}

.logo {
  mix-blend-mode: screen;
}
```

---

## mask-image

**Syntax:** `mask-image: <image> | none`

Hides parts of an element based on the mask's alpha or luminance.

**Values:**
- `none` — no mask (default)
- `url('mask.png')` — image mask
- `linear-gradient(black 40%, transparent)` — gradient mask
- `radial-gradient(circle, black 30%, transparent 70%)` — radial gradient mask
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Fade images with gradient masks
- Mask shapes with image files

**Example:**
```css
.faded {
  mask-image: linear-gradient(black 40%, transparent);
}

.circular {
  mask-image: radial-gradient(circle, black 30%, transparent 70%);
}
```

---

## mask-mode

**Syntax:** `mask-mode: match-source | alpha | luminance`

Interprets mask source as luminance or alpha.

**Values:**
- `match-source` — alpha for images, luminance for SVG (default)
- `alpha` — mask by alpha channel
- `luminance` — mask by luminance values
- `inherit` — inherits from parent
- `initial` — sets to default (match-source)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Use SVG luminance masks
- Control how the mask is interpreted

**Example:**
```css
.mask-lum {
  mask-image: url('mask.svg');
  mask-mode: luminance;
}
```

---

## mask-composite

**Syntax:** `mask-composite: add | subtract | intersect | exclude`

Controls how multiple mask layers combine.

**Values:**
- `add` — layers overlaid (default)
- `subtract` — later layers cut out
- `intersect` — keeps the overlapping area
- `exclude` — keeps non-overlapping areas
- `inherit` — inherits from parent
- `initial` — sets to default (add)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Cut shapes out of masks
- Combine several mask layers

**Example:**
```css
.layer {
  mask-image: url('circle.png'), url('square.png');
  mask-composite: subtract;
}
```

---

## mask-size

**Syntax:** `mask-size: <length> | <percentage> | auto | cover | contain`

Controls the size of the mask image.

**Values:**
- `auto` — natural mask size (default)
- `cover` — scales to cover the element
- `contain` — scales to fit the element
- `50% 50%` — percentage sizing
- `100px 200px` — length sizing
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Scale masks to fill elements
- Size gradient masks precisely

**Example:**
```css
.cover-mask {
  mask-image: url('mask.png');
  mask-size: cover;
}
```

---

## mask-position

**Syntax:** `mask-position: <position>`

Positions the mask image within the element.

**Values:**
- `center` — centered
- `top left` — top-left corner
- `50% 50%` — percentage position
- `10px 20px` — offset position
- `inherit` — inherits from parent
- `initial` — sets to default (0% 0%)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align mask images within the element
- Offset masks from the edges

**Example:**
```css
.offset-mask {
  mask-image: url('mask.png');
  mask-position: center;
}
```

---

**[View Example](../examples/advanced/17-advanced-effects/index.html)**

← **Previous Topic:** [Animation — Direction, Fill Mode & Play State](../advanced/16-animation-fill-and-play-state.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scroll Snap & Touch Interaction](../advanced/18-scroll-snap.md) →
