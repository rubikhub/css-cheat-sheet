# Scroll-Driven Animations

> 6 properties

Animations driven by scroll position instead of time.

---

## animation-timeline

**Syntax:** `animation-timeline: scroll() | view()`

Connects an animation to scroll or view progress.

**Values:**
- `scroll()` — scroll container progress
- `view()` — element visibility progress
- `scroll(root)` — the root scroll container
- `scroll(nearest, block)` — nearest scroll container, block axis
- `auto` — time-based animation (default)
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Animate a progress bar with page scroll
- Reveal elements as they enter the viewport

**Example:**
```css
.progress-bar {
  animation: grow-width linear;
  animation-timeline: scroll(root block);
}

@keyframes grow-width {
  from { transform: scaleX(0); }
  to { transform: scaleX(1); }
}
```

---

## animation-range

**Syntax:** `animation-range: <start> <end>`

Defines the range of the animation timeline.

**Values:**
- `0% 100%` — full percentage range
- `entry 0% entry 100%` — from element entry to fully entered
- `exit 0% exit 100%` — from exit start to fully exited
- `cover 0% cover 100%` — full covered range
- `contain 0% contain 100%` — full contained range
- `normal` — default range (default)
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Start a reveal animation as an element enters
- Delay animation until partway through scroll

**Example:**
```css
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

---

## animation-range-name

**Syntax:** `animation-range-name: <custom-ident> | normal`

Names a specific point in the animation range.

**Values:**
- `--my-range` — a named range point
- `normal` — default range name (default)
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reference named range points
- Coordinate start and end with named ranges

**Example:**
```css
.element {
  animation-range-name: --my-range;
  animation-range-start: --my-range;
  animation-range-end: --my-range;
}
```

---

## animation-range-start / animation-range-end

**Syntax:** `animation-range-start: <start>` | `animation-range-end: <end>`

Sets the start or end boundary of the animation range.

**Values:**
- `entry 20%` — start at 20% through entry
- `exit 80%` — end at 80% through exit
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Fine-tune when an animation begins
- Control when an animation ends

**Example:**
```css
.reveal {
  animation: fade-in linear;
  animation-timeline: view();
  animation-range-start: entry 20%;
  animation-range-end: exit 80%;
}
```

---

## view-timeline

**Syntax:** `view-timeline-name: <name>; view-timeline-axis: <axis>`

Declares a named view timeline on an element.

**Values:**
- `view-timeline-name: --reveal` — the timeline name
- `view-timeline-axis: block` — the scroll axis
- `inherit` — inherits from parent
- `initial` — sets to default (none block)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Share a named timeline across elements
- Trigger animations based on element visibility

**Example:**
```css
.timeline-item {
  view-timeline-name: --reveal;
  view-timeline-axis: block;
}
```

---

## timeline-scope

**Syntax:** `timeline-scope: <name> | none`

Provides access to named timelines across the DOM.

**Values:**
- `--my-timeline` — the name of the timeline to scope
- `none` — no scoped timeline (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Use a timeline declared on another element
- Share scroll timelines between components

**Example:**
```css
.timeline-scope {
  timeline-scope: --my-timeline;
}
```

---

**[View Example](../examples/advanced/22-scroll-animations/index.html)**

← **Previous Topic:** [Anchor Positioning](../advanced/21-anchor-positioning.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scroll State Queries](../advanced/23-scroll-state.md) →
