# Transition Advanced

> 7 properties

Smooth property changes over time using the transition shorthand and its longhand properties.

---

## Transitions

---

## transition

**Syntax:** `transition: <property> <duration> <timing> <delay>`

Shorthand — combines all transition properties into one declaration.

**Values:**
- `color 0.3s ease` — transition a single property
- `color 0.3s ease, background 0.5s ease-in-out` — transition multiple properties
- `all 0.3s ease` — transition all properties
- `inherit` — inherits from parent
- `initial` — sets to default (all 0s ease 0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Animate property changes on hover
- Simplify transition declarations into one line

**Example:**
```css
.card {
  transition: all 0.3s ease;
}

.card:hover {
  transform: scale(1.05);
}
```

---

## transition-property

**Syntax:** `transition-property: <property> | none | all`

Property — specifies which CSS properties to animate.

**Values:**
- `color` — transition color changes
- `background-color` — transition background changes
- `opacity` — transition opacity changes
- `transform` — transition transforms
- `box-shadow` — transition shadow changes
- `color, background-color, opacity` — transition multiple properties
- `all` — transition all properties
- `none` — transition nothing
- `inherit` — inherits from parent
- `initial` — sets to default (all)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Limit which properties animate
- Optimize performance by avoiding all-property transitions

**Example:**
```css
.button {
  transition-property: background-color;
  transition-duration: 0.3s;
}

.button:hover {
  background-color: #0055aa;
}
```

---

## transition-duration

**Syntax:** `transition-duration: <time>`

Duration — specifies how long the transition takes.

**Values:**
- `0s` — no transition (default)
- `0.3s` — quick transition
- `500ms` — half-second transition
- `1s` — one-second transition
- `2.5s` — slow transition
- `0.3s, 0.5s` — per-property durations
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control how fast changes animate
- Create staggered transitions

**Example:**
```css
.link {
  transition-property: color;
  transition-duration: 0.3s;
}
```

---

## transition-timing-function

**Syntax:** `transition-timing-function: <timing-function>`

Timing — defines the speed curve of the transition.

**Values:**
- `ease` — slow start and end (default)
- `linear` — constant speed
- `ease-in` — slow start, fast end
- `ease-out` — fast start, slow end
- `ease-in-out` — slow start and end
- `cubic-bezier(0.25, 0.1, 0.25, 1)` — custom curve
- `cubic-bezier(0.68, -0.55, 0.27, 1.55)` — bounce curve
- `steps(5, end)` — jump in discrete steps
- `step-start` — jump to end instantly
- `step-end` — hold until the end
- `inherit` — inherits from parent
- `initial` — sets to default (ease)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add natural easing to transitions
- Create custom acceleration curves
- Animate in discrete steps

**Example:**
```css
.card {
  transition: transform 0.3s cubic-bezier(0.68, -0.55, 0.27, 1.55);
}
```

---

## transition-delay

**Syntax:** `transition-delay: <time>`

Delay — specifies when the transition starts.

**Values:**
- `0s` — start immediately (default)
- `0.2s` — short delay
- `500ms` — half-second delay
- `1s` — one-second delay
- `0s, 0.2s` — per-property delays
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Stagger multiple transitions
- Create dropdown and menu expansion effects

**Example:**
```css
.menu-item {
  transition: opacity 0.3s ease;
  transition-delay: 0.2s;
}
```

---

## linear() easing

**Syntax:** `transition-timing-function: linear(<points>)`

Defines a piecewise-linear easing function from stop points between 0 and 1.

**Values:**
- `linear(0, 0.5, 1)` — a three-point ramp
- `linear(0, 0.3 20%, 0.9 80%, 1)` — stops with positions
- Use to approximate complex curves with segments

**Use Cases:**
- Multi-stage easing without keyframes

**Example:**
```css
.card {
  transition: transform 300ms linear(0, 0.5 40%, 1);
}
```

---

## transition-behavior

**Syntax:** `transition-behavior: normal | allow-discrete`

Controls whether discrete properties (like display) can transition.

**Values:**
- `normal` — no discrete property transitions (default)
- `allow-discrete` — allows transitions of discrete properties

**Use Cases:**
- Animate element appearance together with @starting-style

**Example:**
```css
.dropdown {
  transition:
    display 0.5s allow-discrete,
    opacity 0.5s;
}
```

---

**[View Example](../examples/intermediate/13-transition-advanced/index.html)**

← **Previous Topic:** [Pseudo Elements Advanced](../intermediate/12-pseudo-elements-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transform](../intermediate/14-transform.md) →
