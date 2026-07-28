# Transform Functions
---
## Container Properties
### translate()
**Type/Initial:** function | (none)

**Description:** Function — moves an element from its current position.

**CSS:**
```css
/* 2D translation */
transform: translate(100px, 50px);
transform: translate(100px);
transform: translateX(100px);
transform: translateY(50px);

/* Percentage values */
transform: translate(50%, 50%);
transform: translateX(100%);
transform: translateY(-50%);

/* 3D translation */
transform: translate3d(100px, 50px, 200px);
transform: translateZ(200px);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    translateX(40px)
  </div>
  <div class="db style-c">
    translateY(-20px)
  </div>
  <div class="db style-d">
    translate(30px, 20px)
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
  padding: 3rem 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: translateX(40px);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: translateY(-20px);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: translate(30px, 20px);
}
```

### rotate()
**Type/Initial:** function | (none)

**Description:** Function — rotates an element clockwise or counter-clockwise.

**CSS:**
```css
/* 2D rotation */
transform: rotate(45deg);
transform: rotate(-45deg);
transform: rotate(0.5turn);
transform: rotate(3.14rad);

/* 3D rotation */
transform: rotateX(45deg);
transform: rotateY(45deg);
transform: rotateZ(45deg);
transform: rotate3d(1, 1, 1, 45deg);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    45deg
  </div>
  <div class="db style-c">
    -45deg
  </div>
  <div class="db style-d">
    0.25turn
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
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(-45deg);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: rotate(0.25turn);
}
```

### scale()
**Type/Initial:** function | (none)

**Description:** Function — resizes an element.

**CSS:**
```css
/* 2D scale */
transform: scale(2);
transform: scale(0.5);
transform: scale(2, 0.5);
transform: scaleX(2);
transform: scaleY(0.5);

/* 3D scale */
transform: scale3d(1, 1, 2);
transform: scaleZ(2);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    scale(2)
  </div>
  <div class="db style-c">
    scale(0.5)
  </div>
  <div class="db style-d">
    scale(1.5, 0.8)
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
  transform: scale(2);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: scale(0.5);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: scale(1.5, 0.8);
}
```

### skew()
**Type/Initial:** function | (none)

**Description:** Function — skews an element on the X and Y axes.

**CSS:**
```css
/* 2D skew */
transform: skew(20deg);
transform: skew(20deg, -10deg);
transform: skewX(20deg);
transform: skewY(-10deg);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    skewX(20deg)
  </div>
  <div class="db style-c">
    skewY(-10deg)
  </div>
  <div class="db style-d">
    skew(20deg, -10deg)
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
  transform: skewX(20deg);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: skewY(-10deg);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: skew(20deg, -10deg);
}
```

### perspective()
**Type/Initial:** function | (none)

**Description:** Function — defines a perspective view for 3D transforms (element level).

**CSS:**
```css
transform: perspective(200px) rotateY(45deg);
transform: perspective(500px) rotateX(30deg);
transform: perspective(1000px) rotateY(-20deg) translateZ(100px);
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
  transform: perspective(200px) rotateY(45deg);
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: perspective(500px) rotateX(30deg);
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transform: perspective(1000px) rotateY(-20deg);
}
```

---

[Example](../examples/intermediate/09-transform-functions/index.html)

← **Previous Topic:** [Transform](../intermediate/08-transform.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Background Advanced](../intermediate/10-background-advanced.md) →
