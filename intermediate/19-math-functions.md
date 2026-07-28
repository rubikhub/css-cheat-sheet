# Math Functions
---
## Container Properties
### calc()
**Type/Initial:** function | (none)

**Description:** Function — performs mathematical calculations on values.

**CSS:**
```css
width: calc(100% - 40px);
height: calc(100vh - 80px);
margin: calc(1rem + 10px);
padding: calc(2 * 1rem);
font-size: calc(14px + 0.5vw);
left: calc(50% - 100px);
top: calc(100% - 50px);

/* Nested */
width: calc(100% - calc(2 * 20px));

/* Mixed units */
font-size: calc(1.2rem + 2px);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    calc(100% - 40px)
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  width: calc(100% - 40px);
}
```

### min()
**Type/Initial:** function | (none)

**Description:** Function — returns the smallest value from a list.

**CSS:**
```css
width: min(50%, 300px);
height: min(100vh, 600px);
font-size: min(2vw, 16px);
padding: min(2rem, 40px);
max-width: min(90%, 800px);
margin: min(5%, 50px);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    min(50%, 300px)
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  width: min(50%, 300px);
}
```

### max()
**Type/Initial:** function | (none)

**Description:** Function — returns the largest value from a list.

**CSS:**
```css
width: max(50%, 300px);
height: max(100vh, 600px);
font-size: max(1rem, 16px);
padding: max(2rem, 40px);
max-width: max(80%, 600px);
margin: max(5%, 50px);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    max(50%, 300px)
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  width: max(50%, 300px);
}
```

### clamp()
**Type/Initial:** function | (none)

**Description:** Function — clamps a value between a minimum and maximum.

**CSS:**
```css
font-size: clamp(12px, 2vw, 16px);
width: clamp(300px, 50%, 800px);
padding: clamp(0.5rem, 2vw, 2rem);
margin: clamp(1rem, 3vw, 3rem);
height: clamp(200px, 50vh, 600px);
gap: clamp(0.5rem, 1vw, 1rem);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    clamp(12px, 2vw, 16px)
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  font-size: clamp(12px, 2vw, 16px);
}
```

---

[Example](../examples/intermediate/19-math-functions/index.html)

← **Previous Topic:** [Animation](../intermediate/18-animation.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transition Advanced](../intermediate/20-transition-advanced.md) →
