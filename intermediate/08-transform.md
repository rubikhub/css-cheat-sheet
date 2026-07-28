# Transform
---
## Container Properties
### transform
**Type/Initial:** transform list | none

**Description:** Transform — applies 2D or 3D transformations to an element.

**CSS:**
```css
/* 2D Transforms */
transform: none;
transform: rotate(45deg);
transform: rotate(-45deg);
transform: scale(2);
transform: scale(0.5);
transform: scale(2, 0.5);
transform: scaleX(2);
transform: scaleY(0.5);
transform: skew(20deg);
transform: skew(20deg, -10deg);
transform: skewX(20deg);
transform: skewY(-10deg);
transform: translate(100px, 50px);
transform: translateX(100px);
transform: translateY(50px);
transform: translate(50%, 50%);

/* 3D Transforms */
transform: perspective(500px) rotateX(45deg);
transform: perspective(500px) rotateY(45deg);
transform: perspective(500px) rotateZ(45deg);
transform: rotate3d(1, 1, 1, 45deg);
transform: scale3d(1, 1, 2);
transform: translate3d(100px, 50px, 200px);
transform: translateZ(200px);
transform: scaleZ(2);

/* Multiple combined */
transform: rotate(45deg) scale(1.5);
transform: translateX(100px) rotate(45deg);
transform: perspective(500px) rotateY(45deg) translateX(50px);

/* Global values */
transform: inherit;
transform: initial;
transform: revert;
transform: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    rotate(45deg)
  </div>
  <div class="db style-c">
    scale(1.5)
  </div>
  <div class="db style-d">
    skewX(20deg)
  </div>
  <div class="db style-e">
    translateX(30px)
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
  gap: 1rem;
  padding: 3rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: scale(1.5);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: skewX(20deg);
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: translateX(30px);
}
```

### transform-origin
**Type/Initial:** position | 50% 50% 0

**Description:** Origin — sets the point around which transforms are applied.

**CSS:**
```css
/* Keyword values */
transform-origin: center;
transform-origin: top left;
transform-origin: bottom right;

/* Length values */
transform-origin: 100px 50px;
transform-origin: 0 0;
transform-origin: 50% 50%;

/* Three-value syntax (3D) */
transform-origin: 50% 50% 100px;
transform-origin: left bottom 200px;

/* Global values */
transform-origin: inherit;
transform-origin: initial;
transform-origin: revert;
transform-origin: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    center
  </div>
  <div class="db style-c">
    top left
  </div>
  <div class="db style-d">
    bottom right
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
  gap: 2rem;
  padding: 3rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
  transform-origin: center;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
  transform-origin: top left;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
  transform-origin: bottom right;
}
```

### transform-box
**Type/Initial:** keyword | border-box

**Description:** Box — defines the reference box for transform-origin.

**CSS:**
```css
transform-box: content-box;
transform-box: border-box;
transform-box: fill-box;
transform-box: stroke-box;
transform-box: view-box;

transform-box: inherit;
transform-box: initial;
transform-box: revert;
transform-box: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    border-box
  </div>
  <div class="db style-c">
    content-box
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
  gap: 2rem;
  padding: 3rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
  transform-origin: top left;
  transform-box: border-box;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(45deg);
  transform-origin: top left;
  transform-box: content-box;
}
```

### perspective
**Type/Initial:** length | none

**Description:** Perspective — sets the distance from the viewer to the z=0 plane (parent level).

**CSS:**
```css
perspective: none;
perspective: 200px;
perspective: 500px;
perspective: 1000px;

perspective: inherit;
perspective: initial;
perspective: revert;
perspective: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    200px
  </div>
  <div class="db style-c">
    500px
  </div>
  <div class="db style-d">
    1000px
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
  gap: 1rem;
  padding: 2rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  perspective: 200px;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  perspective: 500px;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  perspective: 1000px;
}
```

### perspective-origin
**Type/Initial:** position | 50% 50%

**Description:** Perspective origin — sets the vanishing point for perspective.

**CSS:**
```css
perspective-origin: 50% 50%;
perspective-origin: 0 0;
perspective-origin: 100% 100%;
perspective-origin: center top;
perspective-origin: left bottom;
perspective-origin: 200px 100px;

perspective-origin: inherit;
perspective-origin: initial;
perspective-origin: revert;
perspective-origin: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    left top
  </div>
  <div class="db style-c">
    center center
  </div>
  <div class="db style-d">
    right bottom
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
  gap: 1rem;
  padding: 2rem 1rem;
  perspective: 500px;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotateY(30deg);
  perspective-origin: left top;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotateY(30deg);
  perspective-origin: center center;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotateY(30deg);
  perspective-origin: right bottom;
}
```

### backface-visibility
**Type/Initial:** keyword | visible

**Description:** Back face — determines whether the back face is visible when element is flipped.

**CSS:**
```css
backface-visibility: visible;
backface-visibility: hidden;

backface-visibility: inherit;
backface-visibility: initial;
backface-visibility: revert;
backface-visibility: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    visible
  </div>
  <div class="db style-c">
    hidden
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
  gap: 2rem;
  padding: 3rem 1rem;
  perspective: 600px;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotateY(180deg);
  backface-visibility: visible;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotateY(180deg);
  backface-visibility: hidden;
}
```

---

[Example](../examples/intermediate/08-transform/index.html)

← **Previous Topic:** [Border Advanced](../intermediate/07-border-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transform Functions](../intermediate/09-transform-functions.md) →
