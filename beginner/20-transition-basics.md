# Transition Basics

> 5 properties

Smooth animations between property values over time.

---

## transition-property

**Syntax:** `transition-property: none | all | <property-list>`

Which properties to animate — specify properties or all.

**Values:**
- `none` — no transitions (default)
- `all` — animate all properties
- `opacity` — animate opacity only
- `transform` — animate transform only
- `background-color` — animate background color
- `color, opacity` — animate multiple properties
- `inherit` — inherits from parent
- `initial` — sets to default (all)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Animate specific properties for performance
- Create smooth hover effects

**Example:**
```css
.button {
  transition-property: background-color, transform;
}

.card {
  transition-property: all;
}
```

---

## transition-duration

**Syntax:** `transition-duration: <time>`

Animation length — how long the transition takes.

**Values:**
- `0s` — instant (default)
- `0.2s` — fast transition
- `0.3s` — standard transition
- `0.5s` — slow transition
- `1s` — very slow transition
- `200ms` — milliseconds
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create responsive hover effects
- Control animation speed

**Example:**
```css
.button {
  transition-duration: 0.2s;
}

.slow-fade {
  transition-duration: 1s;
}
```

---

## transition-timing-function

**Syntax:** `transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out | cubic-bezier() | steps()`

Animation curve — controls the acceleration of the transition.

**Values:**
- `ease` — starts slow, speeds up, ends slow (default)
- `linear` — constant speed
- `ease-in` — starts slow
- `ease-out` — ends slow
- `ease-in-out` — slow start and end
- `cubic-bezier(0.4, 0, 0.2, 1)` — custom curve
- `steps(5, end)` — stepped animation
- `inherit` — inherits from parent
- `initial` — sets to default (ease)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create natural-feeling animations
- Match Material Design or iOS timing

**Example:**
```css
.button {
  transition-timing-function: ease-in-out;
}

.smooth {
  transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
}
```

---

## transition-delay

**Syntax:** `transition-delay: <time>`

Start delay — waits before starting the transition.

**Values:**
- `0s` — start immediately (default)
- `0.1s` — small delay
- `0.2s` — noticeable delay
- `100ms` — milliseconds
- `inherit` — inherits from parent
- `initial` — sets to default (0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Stagger multiple element animations
- Delay hover effects

**Example:**
```css
.button {
  transition-delay: 0.1s;
}

.staggered:nth-child(2) {
  transition-delay: 0.1s;
}
```

---

## transition

**Syntax:** `transition: <property> <duration> <timing-function> <delay>`

Shorthand — combines property, duration, timing, and delay.

**Values:**
- `all 0.3s ease` — all properties, 0.3s, ease
- `background-color 0.2s ease-in-out` — specific property
- `opacity 0.5s linear 0.1s` — with delay
- `none` — no transitions (default)
- `inherit` — inherits from parent
- `initial` — sets to default (all 0s ease 0s)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify transition declarations
- Create complex animations

**Example:**
```css
.button {
  transition: background-color 0.2s ease, transform 0.1s ease;
}

.card {
  transition: all 0.3s ease;
}
```