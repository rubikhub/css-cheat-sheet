# Lists Basics

> 4 properties

Styling for ordered and unordered lists.

---

## Lists

---

## list-style-type

**Syntax:** `list-style-type: disc | circle | square | decimal | none | <string>`

Bullet/number style — controls the marker appearance.

**Values:**
- `disc` — filled circle (default)
- `circle` — hollow circle
- `square` — filled square
- `decimal` — numbers (1, 2, 3)
- `decimal-leading-zero` — zero-padded (01, 02, 03)
- `lower-roman` — lowercase roman (i, ii, iii)
- `upper-roman` — uppercase roman (I, II, III)
- `lower-alpha` — lowercase letters (a, b, c)
- `upper-alpha` — uppercase letters (A, B, C)
- `none` — no marker
- `inherit` — inherits from parent
- `initial` — sets to default (disc)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create numbered steps
- Remove default bullets

**Example:**
```css
ol {
  list-style-type: decimal;
}

.steps {
  list-style-type: decimal-leading-zero;
}

.no-bullets {
  list-style-type: none;
}
```

---

## list-style-position

**Syntax:** `list-style-position: inside | outside`

Marker placement — inside or outside the content flow.

**Values:**
- `outside` — marker outside content (default)
- `inside` — marker inside content
- `inherit` — inherits from parent
- `initial` — sets to default (outside)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Indent markers inside content
- Create tight list layouts

**Example:**
```css
ul {
  list-style-position: inside;
}
```

---

## list-style-image

**Syntax:** `list-style-image: none | <image>`

Custom marker image — replaces default bullets with images.

**Values:**
- `none` — use default marker (default)
- `url('bullet.png')` — custom image
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Use custom icons as bullets
- Brand list markers

**Example:**
```css
ul {
  list-style-image: url('checkmark.png');
}
```

---

## list-style

**Syntax:** `list-style: <type> <position> <image>`

Shorthand — combines type, position, and image.

**Values:**
- `disc inside` — type position
- `decimal url('bullet.png')` — type image
- `none` — no styling
- `inherit` — inherits from parent
- `initial` — sets to default (disc outside none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify list declarations
- Set multiple list properties at once

**Example:**
```css
ul {
  list-style: square inside;
}

.steps {
  list-style: decimal-leading-zero outside;
}
```

---

**[View Example](../examples/beginner/11-lists-basics/index.html)**

← **Previous Topic:** [Border Basics](../beginner/10-border-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Tables Basics](../beginner/12-tables-basics.md) →

