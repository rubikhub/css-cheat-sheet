# Advanced Math Functions

> 19 functions

CSS functions for complex calculations, rounding, and trigonometry.

---

## Basic Functions

---

## calc()

**Syntax:** `calc(<expression>)`

Performs calculations at computed-value time.

**Values:**
- `calc(100% - 2rem)` — subtract lengths
- `calc(1rem + 0.5vw)` — combine units
- `calc(calc(10px * 2) + calc(1rem / 2))` — nested calc
- `calc(100% / 3)` — divide values

**Use Cases:**
- Create fluid sizing calculations
- Combine fixed and relative units

**Example:**
```css
.element {
  width: calc(100% - 2rem);
  font-size: calc(1rem + 0.5vw);
}
```

---

## clamp()

**Syntax:** `clamp(<min>, <preferred>, <max>)`

Constrains a value between a minimum and maximum.

**Values:**
- `clamp(1rem, 2vw + 0.5rem, 2.5rem)` — responsive font-size
- `clamp(300px, 80%, 1200px)` — fluid width
- `clamp(0.5rem, 2vw, 2rem)` — fluid padding

**Use Cases:**
- Fluid typography
- Responsive sizing with bounds

**Example:**
```css
h1 {
  font-size: clamp(1rem, 2vw + 0.5rem, 2.5rem);
}
```

---

## min() / max()

**Syntax:** `min(<values...>)` | `max(<values...>)`

Returns the smaller or larger of a set of values.

**Values:**
- `min(100%, 600px)` — never wider than 600px
- `min(2rem, 5vw)` — responsive padding
- `max(1rem, 2vw)` — at least 1rem
- `max(300px, 50%)` — at least 300px

**Use Cases:**
- Cap widths responsively
- Set minimum sizes with max()

**Example:**
```css
.element {
  width: min(100%, 600px);
  font-size: max(1rem, 2vw);
}
```

---

## Rounding

---

## round()

**Syntax:** `round(<strategy>, <value>, <interval>)`

Rounds a value to a rounding interval.

**Values:**
- `round(100px, 10px)` — nearest multiple of 10px
- `round(up, 100px, 10px)` — round up
- `round(down, 100px, 10px)` — round down
- `round(nearest, 100px, 10px)` — round to nearest
- `round(to-zero, 100px, 10px)` — round toward zero

**Use Cases:**
- Snap sizes to a grid
- Round to consistent spacing steps

**Example:**
```css
.element {
  width: round(up, 100px, 10px);
}
```

---

## rem()

**Syntax:** `rem(<dividend>, <divisor>)`

Returns the remainder of a division.

**Values:**
- `rem(10px, 3px)` — remainder is 1px
- `rem(var(--index), 3)` — cycles through 0 to 2
- `rem(-10px, 3px)` — negative remainder follows the dividend

**Use Cases:**
- Cycle values with a repeating pattern
- Stagger styles by index

**Example:**
```css
:root {
  --index-offset: rem(var(--index), 3);
}
```

---

## mod()

**Syntax:** `mod(<dividend>, <divisor>)`

Returns the modulus of a division, always positive.

**Values:**
- `mod(10px, 3px)` — remainder is 1px
- `mod(-10px, 3px)` — remainder is 2px
- `mod(7, 4)` — remainder is 3

**Use Cases:**
- Get a positive remainder
- Cycle values predictably

**Example:**
```css
:root {
  --index-mod: mod(var(--index), 3);
}
```

---

## Trigonometric

---

## sin() / cos() / tan()

**Syntax:** `sin(<angle>)` | `cos(<angle>)` | `tan(<angle>)`

Trigonometric functions for angle calculations.

**Values:**
- `sin(45deg)` — 0.707
- `cos(45deg)` — 0.707
- `tan(45deg)` — 1
- `calc(100px * sin(45deg))` — combined with calc

**Use Cases:**
- Calculate circular motion offsets
- Position elements along a circle

**Example:**
```css
@keyframes spin {
  from {
    transform: rotate(0deg) translateX(50px) rotate(0deg);
  }
  to {
    transform: rotate(360deg) translateX(50px) rotate(-360deg);
  }
}
```

---

## asin() / acos() / atan() / atan2()

**Syntax:** `asin(<number>)` | `acos(<number>)` | `atan(<number>)` | `atan2(<y>, <x>)`

Inverse trigonometric functions.

**Values:**
- `asin(0.5)` — 30 degrees
- `acos(0.5)` — 60 degrees
- `atan(1)` — 45 degrees
- `atan2(var(--y), var(--x))` — full-circle angle from coordinates

**Use Cases:**
- Compute angles from ratios
- Derive rotation from coordinates

**Example:**
```css
:root {
  --angle: atan2(var(--y), var(--x));
}
```

---

## Exponential & Sign

---

## pow() / sqrt() / exp() / log()

**Syntax:** `pow(<base>, <exponent>)` | `sqrt(<number>)` | `exp(<number>)` | `log(<number>, <base>)`

Exponential and logarithmic functions.

**Values:**
- `pow(2, 10)` — 1024
- `sqrt(16)` — 4
- `exp(1)` — e (about 2.718)
- `log(100)` — natural log, about 4.6
- `log(100, 10)` — base-10 log, 2

**Use Cases:**
- Scale values exponentially
- Reverse exponentiation

**Example:**
```css
:root {
  --value: pow(2, 10);
}
```

---

## abs() / sign()

**Syntax:** `abs(<number>)` | `sign(<number>)`

Sign-related functions for absolute value and direction.

**Values:**
- `abs(-100px)` — 100px
- `abs(100px)` — 100px
- `sign(-50px)` — -1
- `sign(50px)` — 1
- `sign(0)` — 0

**Use Cases:**
- Normalize directions
- Remove negative signs from offsets

**Example:**
```css
:root {
  --offset: abs(-100px);
}
```

---

## hypot()

**Syntax:** `hypot(<numbers...>)`

Returns the hypotenuse of a set of values.

**Values:**
- `hypot(3px, 4px)` — 5px
- `hypot(5px, 12px)` — 13px
- `hypot(3px, 4px, 12px)` — 13px across three axes

**Use Cases:**
- Compute distances from offsets
- Measure multi-axis lengths

**Example:**
```css
:root {
  --distance: hypot(3px, 4px);
}
```

---

## calc-size()

**Syntax:** `calc-size(<basis>, <calculation>)`

Performs calculations based on intrinsic sizes such as auto.

**Values:**
- `calc-size(auto, size * 0.5)` — half of the intrinsic size
- `calc-size(min-content, size + 2rem)` — add to min-content
- `size` refers to the basis value in the calculation

**Use Cases:**
- Animate between auto and numeric sizes

**Example:**
```css
.menu {
  height: calc-size(auto, size);
  transition: height 0.3s;
}
```

---

## Conditional Functions

---

## if()

**Syntax:** `if(<condition>: <value>; <condition>: <value>; <else>)`

Returns the first value whose condition is true (2025+).

**Values:**
- `if(style(--variant: dark): black; white)` — dark-mode value
- `if(media(width >= 600px): 2fr; 1fr)` — media-condition value
- `if(supports(display: grid): grid; block)` — support check
- The final argument is the fallback

**Use Cases:**
- Replace media-query/value duplication
- Conditional values inline in a single declaration

**Example:**
```css
.card {
  background: if(
    style(--theme: dark): #222;
    #fff
  );
}
```

---

## random()

**Syntax:** `random()` | `random(<min>, <max>)` | `random(--seed)`

Generates a pseudo-random value, optionally in a range (2026).

**Values:**
- `random()` — a random number between 0 and 1
- `random(10px, 40px)` — random length in a range
- `random(0deg, 360deg)` — random angle
- `random(--seed, 0.5, 1)` — seeded randomness

**Use Cases:**
- Vary animation delays and durations
- Scatter decorative elements naturally

**Example:**
```css
.star {
  animation-delay: random(-2s, 0s);
  left: random(0%, 100%);
}
```

---

## random-item()

**Syntax:** `random-item(<values...>)`

Picks one value at random from a list (2026).

**Values:**
- `random-item(red, blue, green)` — a random color
- `random-item(10px, 20px, 30px)` — a random length
- `random-item(--seed, a, b, c)` — seeded choice

**Use Cases:**
- Random background colors per instance
- Random shapes and decorations

**Example:**
```css
.emoji {
  content: random-item("🎈", "🎉", "🎊");
}
```

---

## Tree Counting

---

## sibling-index()

**Syntax:** `sibling-index()`

Returns the index of an element among its siblings (2025+).

**Values:**
- `sibling-index()` — 1-based position among siblings
- Returns `0` for a lone child
- Works inside any property accepting a number

**Use Cases:**
- Compute rotations or offsets per sibling
- Build nth-item-like effects with math

**Example:**
```css
.card {
  transform: rotate(calc(sibling-index() * 5deg));
}
```

---

## sibling-count()

**Syntax:** `sibling-count()`

Returns the number of siblings of an element (2025+).

**Values:**
- `sibling-count()` — total sibling count
- Returns `0` for a lone child

**Use Cases:**
- Size items by how many siblings exist
- Toggle layouts for single vs many items

**Example:**
```css
.item {
  width: calc(100% / sibling-count());
}
```

---

## Value Functions

---

## toggle()

**Syntax:** `toggle(<values...>)`

Cycles through values for successive elements (custom toggles, 2026).

**Values:**
- `toggle(1rem, 2rem)` — alternate between two values
- `toggle(red, blue, green)` — cycle three values
- Cycles per element instance, in document order

**Use Cases:**
- Alternate stripe backgrounds across rows
- Cycle item sizes or colors

**Example:**
```css
tr {
  background: toggle(#fff, #f5f5f5);
}
```

---

## attr() — typed values

**Syntax:** `attr(<attr-name> type(<type>), <fallback>)`

Reads HTML attributes with a typed value (2025+).

**Values:**
- `attr(data-width type(<length>), 0)` — a length attribute
- `attr(data-color type(<color>), black)` — a color attribute
- `attr(data-count type(<integer>), 0)` — an integer attribute

**Use Cases:**
- Move presentational data into HTML attributes
- Avoid inline style hacks for widths and colors

**Example:**
```css
.bar {
  width: attr(data-width type(<length>), 0);
}
```

---

**[View Example](../examples/advanced/28-advanced-math-functions/index.html)**

← **Previous Topic:** [Scroll State Queries](../advanced/27-scroll-state.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Multi-column Layout](../advanced/29-multi-column-layout.md) →

