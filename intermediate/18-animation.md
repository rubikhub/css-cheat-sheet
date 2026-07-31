# Animation

> 11 properties

Animate elements with keyframes and animation timing controls.

---

## Animation

---

## animation

**Syntax:** `animation: <name> <duration> <timing> <delay> <iteration> <direction> <fill-mode> <play-state>`

Shorthand — combines all animation properties into one declaration.

**Values:**
- `fadeIn 1s ease-in-out` — name and duration
- `fadeIn 1s ease-in-out, slideUp 0.5s ease` — multiple animations
- `fadeIn 1s ease-in-out 0.2s infinite alternate both` — full shorthand
- `inherit` — inherits from parent
- `initial` — sets to default (none 0s ease 0s 1 normal none running)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add entrance animations
- Combine multiple effects

**Example:**
```css
.fade-in {
  animation: fadeIn 1s ease-in-out;
}
```

---

## animation-name

**Syntax:** `animation-name: none | <keyframe-name>`

Name — specifies the name of the @keyframes animation.

**Values:**
- `none` — no animation (default)
- `fadeIn` — run the fadeIn keyframes
- `slideUp` — run the slideUp keyframes
- `fadeIn, pulse` — multiple animations
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reuse keyframe definitions
- Chain multiple animations

**Example:**
```css
.box {
  animation-name: pulse;
  animation-duration: 1s;
}
```

---

## animation-duration

**Syntax:** `animation-duration: <time>`

Duration — specifies how long one cycle of the animation takes.

**Values:**
- `0s` — no animation (default)
- `0.5s` — half a second
- `1s` — one second
- `2000ms` — milliseconds
- `1s, 0.5s` — multiple durations
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control animation speed
- Time multi-step sequences

**Example:**
```css
.box {
  animation-name: fadeIn;
  animation-duration: 1s;
}
```

---

## animation-timing-function

**Syntax:** `animation-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier() | steps()`

Timing — defines the speed curve of the animation.

**Values:**
- `ease` — slow start and end (default)
- `linear` — constant speed
- `ease-in` — accelerates
- `ease-out` — decelerates
- `ease-in-out` — accelerate and decelerate
- `cubic-bezier(0.25, 0.1, 0.25, 1)` — custom curve
- `steps(5, end)` — stepped animation
- `inherit` — inherits from parent
- `initial` — sets to default (ease)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create natural motion
- Add custom timing curves

**Example:**
```css
.box {
  animation-name: fadeIn;
  animation-timing-function: ease-in-out;
}
```

---

## animation-delay

**Syntax:** `animation-delay: <time>`

Delay — specifies when the animation starts.

**Values:**
- `0s` — start immediately (default)
- `0.3s` — start after a delay
- `1s` — start after one second
- `-0.5s` — start mid-animation
- `0s, 0.3s` — multiple delays
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Stagger list items
- Sequence animations

**Example:**
```css
.item {
  animation-name: fadeIn;
  animation-delay: 0.3s;
}
```

---

## animation-iteration-count

**Syntax:** `animation-iteration-count: <number> | infinite`

Iteration count — specifies how many times the animation plays.

**Values:**
- `1` — play once (default)
- `3` — play three times
- `0.5` — play half a cycle
- `infinite` — loop forever
- `1, 3` — multiple counts
- `inherit` — inherits from parent
- `initial` — sets to default (1)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Loop loading spinners
- Play effects a set number of times

**Example:**
```css
.spinner {
  animation-name: spin;
  animation-duration: 1s;
  animation-iteration-count: infinite;
}
```

---

## animation-direction

**Syntax:** `animation-direction: normal | reverse | alternate | alternate-reverse`

Direction — specifies whether the animation plays forward, reverse, or alternating.

**Values:**
- `normal` — play forward (default)
- `reverse` — play backward
- `alternate` — forward then backward
- `alternate-reverse` — backward then forward
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create pulsing effects
- Reverse animations for symmetric motion

**Example:**
```css
.pulse {
  animation-name: pulse;
  animation-duration: 1s;
  animation-iteration-count: infinite;
  animation-direction: alternate;
}
```

---

## animation-fill-mode

**Syntax:** `animation-fill-mode: none | forwards | backwards | both`

Fill mode — determines styles applied before/after the animation.

**Values:**
- `none` — no styles outside the animation (default)
- `forwards` — keep the end styles
- `backwards` — apply start styles during the delay
- `both` — apply both
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep the final state after an animation
- Pre-apply the start state during the delay

**Example:**
```css
.box {
  animation-name: fadeIn;
  animation-fill-mode: both;
}
```

---

## animation-play-state

**Syntax:** `animation-play-state: running | paused`

Play state — controls whether the animation is playing or paused.

**Values:**
- `running` — playing (default)
- `paused` — paused
- `inherit` — inherits from parent
- `initial` — sets to default (running)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Pause animations on hover
- Control animations with JavaScript

**Example:**
```css
.card:hover {
  animation-play-state: paused;
}
```

---

## @keyframes

**Syntax:** `@keyframes <name> { <selector> { <declaration> } }`

Keyframes — defines the stages of an animation sequence.

**Values:**
- `from { ... }` — start state
- `to { ... }` — end state
- `0% { ... }` — explicit start state
- `50% { ... }` — midpoint state
- `100% { ... }` — explicit end state
- `0%, 100% { ... }` — shared states

**Use Cases:**
- Define reusable animation sequences
- Animate transforms and opacity

**Example:**
```css
@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

@keyframes pulse {
  0%, 100% {
    transform: scale(1);
  }
  50% {
    transform: scale(1.05);
  }
}
```

---

## animation-composition

**Syntax:** `animation-composition: replace | add | accumulate`

Defines how multiple animations combine values for the same property.

**Values:**
- `replace` — later animation overrides earlier ones (default)
- `add` — values are added together
- `accumulate` — values are accumulated

**Use Cases:**
- Compose transform animations from different keyframes

**Example:**
```css
.ball {
  animation:
    move 2s linear infinite,
    bounce 1s ease-in-out infinite;
  animation-composition: add;
}
```

---

**[View Example](../examples/intermediate/18-animation/index.html)**

← **Previous Topic:** [UI & Scroll](../intermediate/17-ui-and-scroll.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Math Functions](../intermediate/19-math-functions.md) →
