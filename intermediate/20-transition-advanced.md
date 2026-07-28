# Transition Advanced
---
## Container Properties
### transition
**Type/Initial:** shorthand | all 0s ease 0s

**Description:** Shorthand — combines all transition properties into one declaration.

**CSS:**
```css
/* Single property */
transition: color 0.3s ease;

/* Multiple properties */
transition: color 0.3s ease, background 0.5s ease-in-out;

/* All properties */
transition: all 0.3s ease;

/* Global values */
transition: inherit;
transition: initial;
transition: revert;
transition: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    all 0.3s ease
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
  transition: all 0.3s ease;
}
```

### transition-property
**Type/Initial:** keyword | all

**Description:** Property — specifies which CSS properties to animate.

**CSS:**
```css
/* Single property */
transition-property: color;
transition-property: background-color;
transition-property: opacity;
transition-property: transform;
transition-property: box-shadow;

/* Multiple properties */
transition-property: color, background-color, opacity;

/* All properties */
transition-property: all;

/* No properties */
transition-property: none;

/* Global values */
transition-property: inherit;
transition-property: initial;
transition-property: revert;
transition-property: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    color
  </div>
  <div class="db style-c">
    background-color
  </div>
  <div class="db style-d">
    transform
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
  transition-property: color;
  transition-duration: 0.3s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: background-color;
  transition-duration: 0.3s;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
}
```

### transition-duration
**Type/Initial:** time | 0s

**Description:** Duration — specifies how long the transition takes.

**CSS:**
```css
transition-duration: 0s;
transition-duration: 0.3s;
transition-duration: 500ms;
transition-duration: 1s;
transition-duration: 2.5s;

/* Multiple durations */
transition-duration: 0.3s, 0.5s;

transition-duration: inherit;
transition-duration: initial;
transition-duration: revert;
transition-duration: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    0.1s
  </div>
  <div class="db style-c">
    0.3s
  </div>
  <div class="db style-d">
    1s
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
  transition-property: all;
  transition-duration: 0.1s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: all;
  transition-duration: 0.3s;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: all;
  transition-duration: 1s;
}
```

### transition-timing-function
**Type/Initial:** keyword | ease

**Description:** Timing — defines the speed curve of the transition.

**CSS:**
```css
/* Keyword values */
transition-timing-function: ease;
transition-timing-function: linear;
transition-timing-function: ease-in;
transition-timing-function: ease-out;
transition-timing-function: ease-in-out;

/* Bezier curves */
transition-timing-function: cubic-bezier(0.25, 0.1, 0.25, 1);
transition-timing-function: cubic-bezier(0.42, 0, 1, 1);
transition-timing-function: cubic-bezier(0, 0, 0.58, 1);
transition-timing-function: cubic-bezier(0.42, 0, 0.58, 1);
transition-timing-function: cubic-bezier(0.68, -0.55, 0.27, 1.55);

/* Step functions */
transition-timing-function: steps(5, end);
transition-timing-function: step-start;
transition-timing-function: step-end;

transition-timing-function: inherit;
transition-timing-function: initial;
transition-timing-function: revert;
transition-timing-function: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    ease
  </div>
  <div class="db style-c">
    linear
  </div>
  <div class="db style-d">
    ease-in-out
  </div>
  <div class="db style-e">
    cubic-bezier(0.68, -0.55, 0.27, 1.55)
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
  transition-property: transform;
  transition-duration: 0.3s;
  transition-timing-function: ease;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
  transition-timing-function: linear;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
  transition-timing-function: ease-in-out;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
  transition-timing-function: cubic-bezier(0.68, -0.55, 0.27, 1.55);
}
```

### transition-delay
**Type/Initial:** time | 0s

**Description:** Delay — specifies when the transition starts.

**CSS:**
```css
transition-delay: 0s;
transition-delay: 0.2s;
transition-delay: 500ms;
transition-delay: 1s;

/* Multiple delays */
transition-delay: 0s, 0.2s;

transition-delay: inherit;
transition-delay: initial;
transition-delay: revert;
transition-delay: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    0s delay
  </div>
  <div class="db style-c">
    0.3s delay
  </div>
  <div class="db style-d">
    0.6s delay
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
  transition-property: transform;
  transition-duration: 0.3s;
  transition-delay: 0s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
  transition-delay: 0.3s;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition-property: transform;
  transition-duration: 0.3s;
  transition-delay: 0.6s;
}
```

---

[Example](../examples/intermediate/20-transition-advanced/index.html)

← **Previous Topic:** [Math Functions](../intermediate/19-math-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Nesting](../intermediate/21-nesting.md) →
