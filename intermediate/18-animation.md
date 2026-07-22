# Animation
---
## Container Properties
### animation
**Type/Initial:** shorthand | none 0s ease 0s 1 normal none running

**Description:** Shorthand — combines all animation properties into one declaration.

**CSS:**
```css
/* Single animation */
animation: fadeIn 1s ease-in-out;

/* Multiple animations */
animation: fadeIn 1s ease-in-out, slideUp 0.5s ease;

/* With all values */
animation: fadeIn 1s ease-in-out 0.2s infinite alternate both;

/* Global values */
animation: inherit;
animation: initial;
animation: revert;
animation: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    fadeIn 1s
  </div>
  <div class="db style-c">
    slideUp 0.5s
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation: fadeIn 1s ease-in-out;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation: slideUp 0.5s ease;
}
```

### animation-name
**Type/Initial:** keyframe name | none

**Description:** Name — specifies the name of the @keyframes animation.

**CSS:**
```css
animation-name: none;
animation-name: fadeIn;
animation-name: slideUp;
animation-name: pulse;

/* Multiple */
animation-name: fadeIn, pulse;

animation-name: inherit;
animation-name: initial;
animation-name: revert;
animation-name: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    fadeIn
  </div>
  <div class="db style-c">
    pulse
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: pulse;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
```

### animation-duration
**Type/Initial:** time | 0s

**Description:** Duration — specifies how long one cycle of the animation takes.

**CSS:**
```css
animation-duration: 0s;
animation-duration: 0.5s;
animation-duration: 1s;
animation-duration: 2000ms;

/* Multiple durations */
animation-duration: 1s, 0.5s;

animation-duration: inherit;
animation-duration: initial;
animation-duration: revert;
animation-duration: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    0.5s
  </div>
  <div class="db style-c">
    1s
  </div>
  <div class="db style-d">
    2s
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
  animation-name: fadeIn;
  animation-duration: 0.5s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 2s;
}
```

### animation-timing-function
**Type/Initial:** keyword | ease

**Description:** Timing — defines the speed curve of the animation.

**CSS:**
```css
animation-timing-function: ease;
animation-timing-function: linear;
animation-timing-function: ease-in;
animation-timing-function: ease-out;
animation-timing-function: ease-in-out;
animation-timing-function: cubic-bezier(0.25, 0.1, 0.25, 1);
animation-timing-function: steps(5, end);
animation-timing-function: step-start;
animation-timing-function: step-end;

animation-timing-function: inherit;
animation-timing-function: initial;
animation-timing-function: revert;
animation-timing-function: unset;
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
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-timing-function: ease;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-timing-function: linear;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-timing-function: ease-in-out;
}
```

### animation-delay
**Type/Initial:** time | 0s

**Description:** Delay — specifies when the animation starts.

**CSS:**
```css
animation-delay: 0s;
animation-delay: 0.3s;
animation-delay: 1s;
animation-delay: -0.5s;

/* Multiple delays */
animation-delay: 0s, 0.3s;

animation-delay: inherit;
animation-delay: initial;
animation-delay: revert;
animation-delay: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    0s
  </div>
  <div class="db style-c">
    0.3s
  </div>
  <div class="db style-d">
    0.6s
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
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0s;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0.3s;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0.6s;
}
```

### animation-iteration-count
**Type/Initial:** number | 1

**Description:** Iteration count — specifies how many times the animation plays.

**CSS:**
```css
animation-iteration-count: 1;
animation-iteration-count: 3;
animation-iteration-count: 0.5;
animation-iteration-count: infinite;

/* Multiple counts */
animation-iteration-count: 1, 3;

animation-iteration-count: inherit;
animation-iteration-count: initial;
animation-iteration-count: revert;
animation-iteration-count: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    3
  </div>
  <div class="db style-d">
    infinite
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
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: 1;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: 3;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
```

### animation-direction
**Type/Initial:** keyword | normal

**Description:** Direction — specifies whether the animation plays forward, reverse, or alternating.

**CSS:**
```css
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;

/* Multiple directions */
animation-direction: normal, reverse;

animation-direction: inherit;
animation-direction: initial;
animation-direction: revert;
animation-direction: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    normal
  </div>
  <div class="db style-c">
    reverse
  </div>
  <div class="db style-d">
    alternate
  </div>
  <div class="db style-e">
    alternate-reverse
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
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: normal;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: reverse;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: alternate-reverse;
}
```

### animation-fill-mode
**Type/Initial:** keyword | none

**Description:** Fill mode — determines styles applied before/after animation.

**CSS:**
```css
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;

/* Multiple fill modes */
animation-fill-mode: none, forwards;

animation-fill-mode: inherit;
animation-fill-mode: initial;
animation-fill-mode: revert;
animation-fill-mode: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    none
  </div>
  <div class="db style-c">
    forwards
  </div>
  <div class="db style-d">
    backwards
  </div>
  <div class="db style-e">
    both
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
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-fill-mode: none;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-fill-mode: forwards;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-fill-mode: backwards;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-fill-mode: both;
}
```

### animation-play-state
**Type/Initial:** keyword | running

**Description:** Play state — controls whether the animation is playing or paused.

**CSS:**
```css
animation-play-state: running;
animation-play-state: paused;

/* Multiple play states */
animation-play-state: running, paused;

animation-play-state: inherit;
animation-play-state: initial;
animation-play-state: revert;
animation-play-state: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    running
  </div>
  <div class="db style-c">
    paused
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-play-state: running;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-play-state: paused;
}
```

### @keyframes
**Type/Initial:** at-rule | (none)

**Description:** Keyframes — defines the stages of an animation sequence.

**CSS:**
```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes slideUp {
  0% {
    transform: translateY(100px);
    opacity: 0;
  }
  100% {
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes pulse {
  0% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
  100% {
    transform: scale(1);
  }
}

@keyframes bounce {
  0%, 100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-20px);
  }
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    fadeIn
  </div>
  <div class="db style-c">
    pulse
  </div>
  <div class="db style-d">
    bounce
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
  animation: fadeIn 1s ease-in-out;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation: pulse 1s ease-in-out infinite;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  animation: bounce 0.6s ease-in-out infinite;
}
```