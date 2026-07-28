# Animation — Direction, Fill Mode & Play State

Advanced animation control for direction, state persistence, and playback.

---

## animation-direction
**Type:** keyword | **Initial:** normal

Controls whether the animation plays forward, backward, or alternating.

```css
animation-direction: normal;
animation-direction: reverse;
animation-direction: alternate;
animation-direction: alternate-reverse;

/* Global values */
animation-direction: inherit;
animation-direction: initial;
```

```html
<div class="normal">normal</div>
<div class="reverse">reverse</div>
<div class="alternate">alternate</div>
```

```css
@keyframes slide {
  0% { transform: translateX(0); }
  100% { transform: translateX(60px); }
}

.normal {
  animation: slide 1.5s ease infinite;
  animation-direction: normal;
}

.reverse {
  animation: slide 1.5s ease infinite;
  animation-direction: reverse;
}

.alternate {
  animation: slide 1.5s ease infinite;
  animation-direction: alternate;
}
```

---

## animation-fill-mode
**Type:** keyword | **Initial:** none

Determines styles applied before and after the animation plays.

```css
animation-fill-mode: none;
animation-fill-mode: forwards;
animation-fill-mode: backwards;
animation-fill-mode: both;

/* Global values */
animation-fill-mode: inherit;
animation-fill-mode: initial;
```

- **none** — No styles applied before/after
- **forwards** — Retains the final keyframe values
- **backwards** — Applies the first keyframe values during the delay
- **both** — Applies both forwards and backwards

---

## animation-play-state
**Type:** keyword | **Initial:** running

Pauses or resumes an animation.

```css
animation-play-state: running;
animation-play-state: paused;

/* Global values */
animation-play-state: inherit;
animation-play-state: initial;
```

```css
.box:hover {
  animation-play-state: paused;
}
```


---

[Example](../examples/advanced/07-animation-fill-and-play-state/index.html)

← **Previous Topic:** [3D Transforms](../advanced/06-3d-transforms.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced Visual Effects](../advanced/08-advanced-effects.md) →
