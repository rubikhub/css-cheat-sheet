# Border Radius

> 4 properties

Rounded corners — shorthand, individual corners, and logical radii.

---

## border-radius

**Syntax:** `border-radius: <length> | <percentage>`

Rounded corners — curves the border-box corners.

**Values:**
- `10px` — rounded corners
- `50%` — fully rounded, circle or pill shape
- `0` — square corners
- `10px 20px` — two-value radii
- `10px 20px 30px` — three-value radii
- `10px 20px 30px 40px` — all four corners
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round button and card corners
- Create circular or pill-shaped elements

**Example:**
```css
.button {
  border-radius: 8px;
}

.avatar {
  border-radius: 50%;
}
```

---

## border-top-left-radius / top-right-radius

**Syntax:** `border-<corner>-radius: <length> | <percentage>`

Individual corner — radius for a specific corner.

**Values:**
- `10px` — rounded corner
- `50%` — fully rounded corner
- `10px 20px` — horizontal and vertical radii
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round individual corners of a card
- Create asymmetric shapes

**Example:**
```css
.card {
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}
```

---

## border-bottom-left-radius / bottom-right-radius

**Syntax:** `border-<corner>-radius: <length> | <percentage>`

Individual corner — radius for a specific corner.

**Values:**
- `10px` — rounded corner
- `50%` — fully rounded corner
- `10px 20px` — horizontal and vertical radii
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round bottom corners of a card
- Create pill or squircle shapes

**Example:**
```css
.pill {
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
}
```

---

## border-start-radius / border-end-radius

**Syntax:** `border-start-start-radius: <length> | <percentage>` (also `border-start-end-radius`, `border-end-start-radius`, `border-end-end-radius`)

Logical corner radius — maps to physical corners based on writing direction.

**Values:**
- `border-start-start-radius: 16px` — first logical corner
- `border-start-end-radius: 0` — no rounding
- `border-end-start-radius: 0` — no rounding
- `border-end-end-radius: 16px` — last logical corner
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round corners based on writing direction
- Support RTL layouts with logical properties

**Example:**
```css
.card {
  border-start-start-radius: 16px;
  border-end-end-radius: 16px;
}
```

---

**[View Example](../examples/intermediate/10-border-radius/index.html)**

← **Previous Topic:** [Outline](../intermediate/09-outline.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Box Shadows](../intermediate/11-box-shadow.md) →

