# Advanced Math Functions

Complex calculations and statistical functions.

---

## calc()
**Type:** function

Performs calculations at computed-value time.

```css
/* Basic */
width: calc(100% - 2rem);
font-size: calc(1rem + 0.5vw);

/* Nested */
padding: calc(calc(10px * 2) + calc(1rem / 2));
```

---

## clamp()
**Type:** function

Constrains a value between a minimum and maximum.

```css
/* clamp(min, preferred, max) */
font-size: clamp(1rem, 2vw + 0.5rem, 2.5rem);
width: clamp(300px, 80%, 1200px);
padding: clamp(0.5rem, 2vw, 2rem);
```

---

## min() / max()
**Type:** function

Returns the smaller or larger of values.

```css
/* min() */
width: min(100%, 600px);
padding: min(2rem, 5vw);

/* max() */
font-size: max(1rem, 2vw);
width: max(300px, 50%);
```

---

## round()
**Type:** function

Rounds a number.

```css
/* round(value, roundingInterval) */
width: round(100px, 10px); /* 100px */

/* round-to-zero, up, down, nearest */
width: round(up, 100px, 10px);
width: round(down, 100px, 10px);
width: round(nearest, 100px, 10px);
```

---

## rem()
**Type:** function

Returns the remainder (modulo).

```css
/* rem(dividend, divisor) */
value: rem(10px, 3px); /* 1px */

/* Useful for cycling */
column-width: rem(var(--index), 3);
```

---

## mod()
**Type:** function

Returns the modulus (always positive).

```css
/* mod(dividend, divisor) */
value: mod(10px, 3px); /* 1px */
value: mod(-10px, 3px); /* 2px */
```

---

## sin() / cos() / tan()
**Type:** trigonometric functions

```css
/* Trigonometric calculations */
offset-x: calc(100px * sin(45deg));
offset-y: calc(100px * cos(45deg));

/* Circular motion */
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
**Type:** inverse trigonometric functions

```css
/* Inverse trig */
angle: asin(0.5);
angle: acos(0.5);
angle: atan(1);

/* atan2 for full circle */
angle: atan2(var(--y), var(--x));
```

---

## pow() / sqrt() / exp() / log()
**Type:** exponential and logarithmic functions

```css
/* Power */
value: pow(2, 10); /* 1024 */

/* Square root */
value: sqrt(16); /* 4 */

/* Exponential */
value: exp(1); /* e */

/* Logarithmic */
value: log(100); /* ~4.6 */
```

---

## abs() / sign()
**Type:** sign-related functions

```css
/* Absolute value */
offset: abs(-100px); /* 100px */

/* Sign */
direction: sign(-50px); /* -1 */
```

---

## hypot()
**Type:** function

Returns the hypotenuse.

```css
/* hypot(a, b, ...) */
distance: hypot(3px, 4px); /* 5px */
```

```css
/* Complex layout calculation */
.grid-item {
  --gap: 1rem;
  --columns: 4;
  width: calc((100% - var(--gap) * (var(--columns) - 1)) / var(--columns));
}

/* Responsive font with complex math */
h1 {
  font-size: clamp(
    max(1.5rem, 2vw),
    min(3rem, 4vw),
    4rem
  );
}

/* Animated circle */
@keyframes orbit {
  from {
    transform: rotate(0deg) translateX(100px) rotate(0deg);
  }
  to {
    transform: rotate(360deg) translateX(100px) rotate(-360deg);
  }
}
```
