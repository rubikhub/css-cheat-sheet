# Animation — Direction, Fill Mode & Play State

> 3 properties

Advanced animation control for direction, state persistence, and playback.

---

## animation-direction

**Syntax:** `animation-direction: normal | reverse | alternate | alternate-reverse`

Controls whether the animation plays forward, backward, or alternating.

**Values:**
- `normal` — plays forward (default)
- `reverse` — plays backward
- `alternate` — alternates forward and backward
- `alternate-reverse` — alternates backward then forward
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Play animations in reverse
- Create alternating motion effects

**Example:**
```css
.normal {
  animation: slide 1.5s ease infinite;
  animation-direction: normal;
}

.reverse {
  animation: slide 1.5s ease infinite;
  animation-direction: reverse;
}
```

---

## animation-fill-mode

**Syntax:** `animation-fill-mode: none | forwards | backwards | both`

Determines styles applied before and after the animation plays.

**Values:**
- `none` — no styles applied before/after (default)
- `forwards` — retains the final keyframe values
- `backwards` — applies the first keyframe values during the delay
- `both` — applies both forwards and backwards
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep the final state after an animation ends
- Apply the starting state during the delay

**Example:**
```css
.retain {
  animation: slide 1s ease 1s forwards;
}

.delayed {
  animation: fadeIn 2s ease 1s backwards;
}
```

---

## animation-play-state

**Syntax:** `animation-play-state: running | paused`

Pauses or resumes an animation.

**Values:**
- `running` — animation plays normally (default)
- `paused` — animation is paused
- `inherit` — inherits from parent
- `initial` — sets to default (running)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Pause animations on hover
- Control playback from JavaScript

**Example:**
```css
.box {
  animation: spin 2s linear infinite;
}

.box:hover {
  animation-play-state: paused;
}
```

---

**[View Example](../examples/advanced/07-animation-fill-and-play-state/index.html)**

← **Previous Topic:** [3D Transforms](../advanced/06-3d-transforms.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced Visual Effects](../advanced/08-advanced-effects.md) →
