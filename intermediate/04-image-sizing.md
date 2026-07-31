# Image Sizing

> 4 properties

Sizing and positioning for images and video — aspect ratios, object fit, and resolution-aware sources.

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

**[View Example](../examples/intermediate/04-image-sizing/index.html)**

← **Previous Topic:** [Background Advanced](../intermediate/03-background-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography Advanced](../intermediate/05-typography-advanced.md) →

