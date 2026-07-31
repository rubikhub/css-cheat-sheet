# Advanced Math Functions

> 11 functions

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

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

**[View Example](../examples/advanced/23-advanced-math-functions/index.html)**

← **Previous Topic:** [Typography 2024+](../advanced/22-typography-2024.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Web Components & Shadow DOM](../advanced/24-components-and-shadow-dom.md) →
