# CSS Shapes

> 3 properties

Wrap text around custom shapes using floats.

---

## shape-outside

**Syntax:** `shape-outside: none | <basic-shape> | <shape-box> | <image>`

Defines a shape that adjacent inline content wraps around.

**Values:**
- `none` — the float box is used (default)
- `circle(50%)` — circular wrap shape
- `ellipse(50% 40%)` — elliptical wrap shape
- `inset(20px)` — inset rectangle wrap
- `polygon(...)` — polygonal wrap shape
- `margin-box` / `border-box` / `padding-box` / `content-box` — shape box
- `url(image.png)` — shape from an image's alpha channel

**Use Cases:**
- Wrap text around circular avatars
- Flow text around a polygon or image shape

**Example:**
```css
.avatar {
  float: left;
  shape-outside: circle(50%);
}

.photo {
  float: right;
  shape-outside: url(shape.png);
}
```

---

## shape-margin

**Syntax:** `shape-margin: <length-percentage>`

Adds margin around a shape-outside shape.

**Values:**
- `0` — no extra margin (default)
- `20px` — text stops 20px from the shape
- `10%` — percentage of the reference box

**Use Cases:**
- Add breathing room between text and shapes

**Example:**
```css
.avatar {
  float: left;
  shape-outside: circle(50%);
  shape-margin: 1rem;
}
```

---

## shape-image-threshold

**Syntax:** `shape-image-threshold: <number>`

Sets the alpha threshold used to derive a shape from an image.

**Values:**
- `0.0` — any opaque pixel counts (default)
- `0.5` — pixels above 50% opacity count
- `1.0` — only fully opaque pixels count

**Use Cases:**
- Control how much of a soft-edged image wraps text

**Example:**
```css
.photo {
  float: left;
  shape-outside: url(soft.png);
  shape-image-threshold: 0.3;
}
```

---

**[View Example](../examples/intermediate/28-css-shapes/index.html)**

← **Previous Topic:** [Media Queries](../intermediate/27-media-queries.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Performance & Rendering](../intermediate/29-performance-and-rendering.md) →
