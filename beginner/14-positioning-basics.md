# Positioning Basics

> 5 properties

Positioning and stacking — relative, absolute, fixed, sticky, z-index, and floats.

---

## position

**Syntax:** `position: static | relative | absolute | fixed | sticky`

Positions element relative to context — static, relative, absolute, fixed, or sticky.

**Values:**
- `static` — default, follows normal flow
- `relative` — positioned relative to its normal position
- `absolute` — positioned relative to nearest positioned ancestor
- `fixed` — positioned relative to viewport
- `sticky` — toggles between relative and fixed on scroll
- `inherit` — inherits from parent
- `initial` — sets to default (static)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create modals and overlays with `position: fixed`
- Build sticky navigation headers

**Example:**
```css
.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 8px;
  right: 8px;
}
```

---

## top / right / bottom / left

**Syntax:** `top: <length> | <percentage> | auto`

Offsets from edges — pushes element from the edge of its positioning context.

**Values:**
- `auto` — no offset (default)
- `10px` — pixel offset
- `2em` — em-based offset
- `50%` — percentage of containing block
- `0` — flush with edge
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position elements absolutely within a container
- Center elements with top/left 50% and transforms

**Example:**
```css
.element {
  position: absolute;
  top: 10px;
  left: 10px;
}
```

---

## z-index

**Syntax:** `z-index: <integer> | auto`

Controls stacking order — higher values appear in front of lower values on positioned elements.

**Values:**
- `auto` — default stacking order
- `1` — low stacking order
- `9999` — high stacking order
- `-1` — behind other elements
- `0` — base stacking level
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Layer overlapping elements in modals or dropdowns
- Bring elements in front of pseudo-elements

**Example:**
```css
.overlay {
  z-index: 10;
}

.content {
  z-index: 1;
}
```

---

## float

**Syntax:** `float: none | left | right | inline-start | inline-end`

Floats element to side — wraps text around floated elements in document flow.

**Values:**
- `none` — element is not floated (default)
- `left` — element floats to the left
- `right` — element floats to the right
- `inline-start` — floats to start of inline direction
- `inline-end` — floats to end of inline direction
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Wrap text around images in articles
- Create multi-column layouts (legacy)

**Example:**
```css
.image {
  float: left;
  margin-right: 10px;
}
```

---

## clear

**Syntax:** `clear: none | left | right | both | inline-start | inline-end`

Prevents float overlap — pushes element below floated elements on specified sides.

**Values:**
- `none` — allows floats on both sides (default)
- `left` — clears left floats
- `right` — clears right floats
- `both` — clears both left and right floats
- `inline-start` — clears start-side floats
- `inline-end` — clears end-side floats
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent elements from wrapping around floats
- Clear floats after a floated sidebar

**Example:**
```css
.clearfix {
  clear: both;
}
```

---

**[View Example](../examples/beginner/14-positioning-basics/index.html)**

← **Previous Topic:** [Display Basics](../beginner/13-display-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Flexbox Basics](../beginner/15-flexbox-basics.md) →

