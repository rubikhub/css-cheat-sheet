# Filter & Clip Path
---
## Container Properties
### filter
**Type/Initial:** filter function | none

**Description:** Filter — applies graphical effects like blur, brightness, and contrast.

**CSS:**
```css
/* None */
filter: none;

/* Single filter */
filter: blur(5px);
filter: brightness(1.5);
filter: contrast(200%);
filter: grayscale(100%);
filter: hue-rotate(90deg);
filter: invert(100%);
filter: opacity(50%);
filter: saturate(200%);
filter: sepia(100%);
filter: drop-shadow(2px 2px 4px rgba(0, 0, 0, 0.3));
filter: url("filter.svg");

/* Multiple filters */
filter: blur(2px) brightness(1.2);
filter: grayscale(50%) contrast(1.5) brightness(1.1);
filter: drop-shadow(1px 1px 2px black) blur(1px);

/* Global values */
filter: inherit;
filter: initial;
filter: revert;
filter: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    blur
  </div>
  <div class="db style-c">
    brightness
  </div>
  <div class="db style-d">
    grayscale
  </div>
  <div class="db style-e">
    drop-shadow
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  filter: blur(2px);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  filter: brightness(1.5);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  filter: grayscale(100%);
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  filter: drop-shadow(2px 2px 4px rgba(0, 0, 0, 0.3));
}
```

### clip-path
**Type/Initial:** shape | none

**Description:** Clip path — defines a visible region of an element using shapes.

**CSS:**
```css
/* None */
clip-path: none;

/* Basic shapes */
clip-path: circle(50%);
clip-path: circle(30% at 50% 50%);
clip-path: ellipse(50% 30% at 50% 50%);
clip-path: inset(10px 20px 30px 40px round 10px);
clip-path: polygon(50% 0%, 100% 100%, 0% 100%);
clip-path: polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%);
clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);

/* Path */
clip-path: path("M 0 0 L 100 0 L 100 100 L 0 100 Z");

/* URL reference */
clip-path: url("clip.svg");

/* Global values */
clip-path: inherit;
clip-path: initial;
clip-path: revert;
clip-path: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    circle
  </div>
  <div class="db style-c">
    polygon
  </div>
  <div class="db style-d">
    star
  </div>
  <div class="db style-e">
    inset
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  padding: 2rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  clip-path: circle(50%);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  clip-path: polygon(50% 0%, 100% 100%, 0% 100%);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  clip-path: polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%);
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  clip-path: inset(10px 20px 30px 40px round 10px);
}
```

---

[Example](../examples/intermediate/14-filter-and-clip-path/index.html)

← **Previous Topic:** [Counters & Markers](../intermediate/13-counters-and-markers.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Pseudo Elements Advanced](../intermediate/15-pseudo-elements-advanced.md) →
