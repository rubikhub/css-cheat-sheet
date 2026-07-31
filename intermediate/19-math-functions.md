# Math Functions

> 5 functions

Functions for performing mathematical calculations and creating dynamic, fluid values.

---

## Math Functions

---

## calc()

**Syntax:** `calc(<expression>)`

Function — performs mathematical calculations on values.

**Values:**
- `100% - 40px` — subtract a fixed width from a percentage
- `100vh - 80px` — subtract a fixed height from viewport height
- `1rem + 10px` — add rem and pixel values
- `2 * 1rem` — multiply a value
- `14px + 0.5vw` — combine fixed and viewport units
- `50% - 100px` — center by offsetting a percentage
- `100% - calc(2 * 20px)` — nested calculation

**Use Cases:**
- Subtract fixed offsets from percentage values
- Mix units that can't be combined directly
- Create fluid responsive sizing

**Example:**
```css
.container {
  width: calc(100% - 40px);
  font-size: calc(14px + 0.5vw);
}
```

---

## min()

**Syntax:** `min(<values>)`

Function — returns the smallest value from a list.

**Values:**
- `min(50%, 300px)` — cap a percentage at a fixed maximum
- `min(100vh, 600px)` — cap a viewport height
- `min(2vw, 16px)` — cap a viewport-based font size
- `min(2rem, 40px)` — cap a rem-based padding
- `min(90%, 800px)` — cap a fluid width
- `min(5%, 50px)` — cap a percentage margin

**Use Cases:**
- Cap content widths responsively
- Prevent values from exceeding a maximum

**Example:**
```css
.content {
  width: min(90%, 800px);
}

.text {
  font-size: min(2vw, 16px);
}
```

---

## max()

**Syntax:** `max(<values>)`

Function — returns the largest value from a list.

**Values:**
- `max(50%, 300px)` — enforce a minimum width
- `max(100vh, 600px)` — enforce a minimum height
- `max(1rem, 16px)` — enforce a minimum font size
- `max(2rem, 40px)` — enforce a minimum padding
- `max(80%, 600px)` — enforce a minimum width
- `max(5%, 50px)` — enforce a minimum margin

**Use Cases:**
- Enforce minimum sizes
- Ensure values never fall below a floor

**Example:**
```css
.sidebar {
  width: max(30%, 300px);
}
```

---

## clamp()

**Syntax:** `clamp(<min>, <preferred>, <max>)`

Function — clamps a value between a minimum and maximum.

**Values:**
- `clamp(12px, 2vw, 16px)` — fluid font size
- `clamp(300px, 50%, 800px)` — fluid width
- `clamp(0.5rem, 2vw, 2rem)` — fluid padding
- `clamp(1rem, 3vw, 3rem)` — fluid margin
- `clamp(200px, 50vh, 600px)` — fluid height
- `clamp(0.5rem, 1vw, 1rem)` — fluid gap

**Use Cases:**
- Create fully fluid responsive typography
- Set responsive sizes with built-in min/max

**Example:**
```css
h1 {
  font-size: clamp(12px, 2vw, 16px);
}

.button {
  padding: clamp(0.5rem, 2vw, 2rem);
}
```

---

## env()

**Syntax:** `env(<custom-ident>, <fallback>)`

Returns environment variables such as viewport safe-area insets.

**Values:**
- `env(safe-area-inset-top)` — top safe area
- `env(safe-area-inset-bottom)` — bottom safe area (home indicator)
- `env(safe-area-inset-left, 0px)` — left safe area with fallback
- `env(safe-area-inset-right, 12px)` — right safe area with fallback

**Use Cases:**
- Pad content for notched phones

**Example:**
```css
.shell {
  padding-bottom: env(safe-area-inset-bottom, 16px);
}
```

---

**[View Example](../examples/intermediate/19-math-functions/index.html)**

← **Previous Topic:** [Animation](../intermediate/18-animation.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Nesting](../intermediate/20-nesting.md) →
