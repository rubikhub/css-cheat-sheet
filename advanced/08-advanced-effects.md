# Advanced Visual Effects

Backdrop filters, blend modes, and CSS masking.

---

## backdrop-filter
**Type:** function list | **Initial:** none

Applies filter effects to the area **behind** an element (frosted glass effect).

```css
backdrop-filter: none;
backdrop-filter: blur(10px);
backdrop-filter: brightness(150%);
backdrop-filter: contrast(200%);
backdrop-filter: grayscale(100%);
backdrop-filter: blur(5px) brightness(150%);

/* Global values */
backdrop-filter: inherit;
backdrop-filter: initial;
```

```html
<div class="glass-container">
  <div class="glass-card">Frosted Glass</div>
</div>
```

```css
.glass-container {
  background: repeating-linear-gradient(45deg, #ff6b6b, #ff6b6b 10px, #4d96ff 10px, #4d96ff 20px);
}

.glass-card {
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  background: rgba(255, 255, 255, 0.25);
  border: 1px solid rgba(255, 255, 255, 0.3);
  border-radius: 8px;
  padding: 1rem;
}
```

---

## mix-blend-mode
**Type:** keyword | **Initial:** normal

Determines how an element's content blends with what's behind it.

```css
mix-blend-mode: normal;
mix-blend-mode: multiply;
mix-blend-mode: screen;
mix-blend-mode: overlay;
mix-blend-mode: darken;
mix-blend-mode: lighten;
mix-blend-mode: color-dodge;
mix-blend-mode: color-burn;
mix-blend-mode: hard-light;
mix-blend-mode: soft-light;
mix-blend-mode: difference;
mix-blend-mode: exclusion;
mix-blend-mode: hue;
mix-blend-mode: saturation;
mix-blend-mode: color;
mix-blend-mode: luminosity;

/* Global values */
mix-blend-mode: inherit;
mix-blend-mode: initial;
```

---

## mask-image
**Type:** url | gradient | **Initial:** none

Hides parts of an element based on the mask's alpha or luminance.

```css
mask-image: none;
mask-image: url('mask.png');
mask-image: linear-gradient(black 40%, transparent);
mask-image: radial-gradient(circle, black 30%, transparent 70%);

/* Global values */
mask-image: inherit;
mask-image: initial;
```

---

## mask-mode
**Type:** keyword | **Initial:** match-source

Interprets mask source as luminance or alpha.

```css
mask-mode: luminance;
mask-mode: alpha;
mask-mode: match-source;
```

---

## mask-composite
**Type:** keyword | **Initial:** add

Controls how multiple mask layers combine.

```css
mask-composite: add;
mask-composite: subtract;
mask-composite: intersect;
mask-composite: exclude;
```

---

## mask-size
**Type:** length | % | cover | contain | auto | **Initial:** auto

Controls the size of the mask image.

```css
mask-size: auto;
mask-size: 50% 50%;
mask-size: cover;
mask-size: contain;
mask-size: 100px 200px;
```

---

## mask-position
**Type:** position | **Initial:** 0% 0%

Positions the mask image within the element.

```css
mask-position: center;
mask-position: top left;
mask-position: 50% 50%;
mask-position: 10px 20px;
```


---

[Example](../examples/advanced/08-advanced-effects/index.html)

← **Previous Topic:** [Animation — Direction, Fill Mode & Play State](../advanced/07-animation-fill-and-play-state.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS Counters — Complex Patterns](../advanced/09-css-counters-complex.md) →
