# Scroll-Driven Animations

Animations driven by scroll position instead of time.

---

## animation-timeline
**Type:** keyword | function | **Initial:** auto

Connects an animation to scroll or view progress.

```css
/* Scroll progress */
animation-timeline: scroll();

/* View progress */
animation-timeline: view();

/* Named scroll container */
animation-timeline: scroll(root);

/* Named element */
animation-timeline: scroll(nearest, block);
```

---

## animation-range
**Type:** keyword | length | percentage | **Initial:** normal

Defines the range of the animation timeline.

```css
/* Percentage range */
animation-range: 0% 100%;

/* Entry/exit */
animation-range: entry 0% entry 100%;
animation-range: exit 0% exit 100%;

/* Covering */
animation-range: cover 0% cover 100%;

/* Containing */
animation-range: contain 0% contain 100%;
```

---

## animation-range-name
**Type:** name | **Initial:** normal

Names a specific point in the animation range.

```css
animation-range-name: --my-range;
animation-range-start: --my-range;
animation-range-end: --my-range;
```

---

## animation-range-start / animation-range-end
**Type:** keyword | length | percentage

```css
animation-range-start: entry 20%;
animation-range-end: exit 80%;
```

```css
/* Progress bar tied to scroll */
.progress-bar {
  animation: grow-width linear;
  animation-timeline: scroll(root block);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: blue;
  transform-origin: left;
}

@keyframes grow-width {
  from { transform: scaleX(0); }
  to { transform: scaleX(1); }
}

/* Reveal on scroll */
.reveal {
  animation: fade-in linear;
  animation-timeline: view();
  animation-range: entry 0% entry 100%;
}

@keyframes fade-in {
  from { opacity: 0; transform: translateY(30px); }
  to { opacity: 1; transform: translateY(0); }
}
```

```html
<div class="progress-bar"></div>
<div class="content">
  <div class="reveal">Item 1</div>
  <div class="reveal">Item 2</div>
  <div class="reveal">Item 3</div>
</div>
```

```css
.progress-bar {
  animation: grow-width linear;
  animation-timeline: scroll(root block);
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(to right, #667eea, #764ba2);
  transform-origin: left;
}

@keyframes grow-width {
  from { transform: scaleX(0); }
  to { transform: scaleX(1); }
}
```

---

## view-timeline
**Type:** keyword | **Initial:** auto

Declares a named view timeline on an element.

```css
.timeline-item {
  view-timeline-name: --reveal;
  view-timeline-axis: block;
}
```

---

## timeline-scope
**Type:** name | **Initial:** none

Provides access to named timelines across the DOM.

```css
.timeline-scope {
  timeline-scope: --my-timeline;
}
```
