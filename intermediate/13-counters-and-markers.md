# Counters & Markers

> 5 properties

Automatic numbering with CSS counters and custom list marker styles.

---

## Counters

---

## counter-reset

**Syntax:** `counter-reset: <name> <integer> | none`

Counter reset — creates or resets a named CSS counter to a value.

**Values:**
- `none` — no counter reset
- `myCounter` — create counter at 0
- `myCounter 0` — create counter at 0
- `myCounter 10` — create counter at 10
- `myCounter -1` — create counter at -1
- `myCounter 0 anotherCounter 0` — reset multiple counters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Start numbered content at a specific value
- Manage multiple counters at once

**Example:**
```css
.section {
  counter-reset: chapter 0;
}
```

---

## counter-increment

**Syntax:** `counter-increment: <name> <integer> | none`

Counter increment — increases a named CSS counter by a value.

**Values:**
- `none` — no increment
- `myCounter` — increment by 1
- `myCounter 1` — increment by 1
- `myCounter 2` — increment by 2
- `myCounter -1` — decrement by 1
- `myCounter 0.5` — increment by 0.5
- `myCounter anotherCounter` — increment multiple counters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Number list items automatically
- Step by values other than one

**Example:**
```css
ol li {
  counter-increment: item;
}
```

---

## counter()

**Syntax:** `content: counter(<name>) | counter(<name>, <list-style-type>)`

Displays the current value of a named counter in generated content.

**Values:**
- `counter(myCounter)` — plain decimal value
- `counter(myCounter, decimal)` — decimal value
- `counter(myCounter, decimal-leading-zero)` — zero-padded numbers
- `counter(myCounter, lower-roman)` — lowercase roman numerals
- `counter(myCounter, upper-roman)` — uppercase roman numerals
- `counter(myCounter, lower-alpha)` — lowercase letters
- `counter(myCounter, upper-alpha)` — uppercase letters
- `counter(parent) "." counter(child)` — combined nested counters

**Use Cases:**
- Show automatic numbering in generated content
- Format numbers with roman or alphabetic styles

**Example:**
```css
ol li::before {
  counter-increment: item;
  content: counter(item, upper-roman) ". ";
}
```

---

## counters()

**Syntax:** `content: counters(<name>, <separator>) | counters(<name>, <separator>, <list-style-type>)`

Displays all nested counters with the same name, joined by a separator.

**Values:**
- `counters(myCounter, ".")` — nested values joined by dots
- `counters(myCounter, " > ")` — nested values joined by arrows
- `counters(myCounter, " - ")` — nested values joined by dashes
- `counters(myCounter, "", decimal)` — empty separator with a counter style
- `counters(section, ".")` — numbered section tree

**Use Cases:**
- Number nested lists or sections
- Build outline-style numbering

**Example:**
```css
ol li::before {
  counter-increment: section;
  content: counters(section, ".") " ";
}
```

---

## Markers

---

## list-style-type

**Syntax:** `list-style-type: disc | circle | square | none | decimal | lower-roman | upper-roman | <string>`

Marker type — specifies the marker style for list items.

**Values:**
- `disc` — filled circle (default)
- `circle` — hollow circle
- `square` — filled square
- `none` — no marker
- `decimal` — 1, 2, 3...
- `decimal-leading-zero` — 01, 02, 03...
- `lower-roman` — i, ii, iii...
- `upper-roman` — I, II, III...
- `lower-alpha` — a, b, c...
- `upper-alpha` — A, B, C...
- `lower-greek` — greek letters
- `lower-latin` — lowercase latin letters
- `upper-latin` — uppercase latin letters
- `disclosure-open` — expanded disclosure triangle
- `disclosure-closed` — collapsed disclosure triangle
- `hebrew` — hebrew numerals
- `cjk-ideographic` — CJK numerals
- `hiragana` — hiragana characters
- `katakana` — katakana characters
- `"→"` — custom string marker
- `inherit` — inherits from parent
- `initial` — sets to default (disc)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style ordered and unordered lists
- Use custom string markers

**Example:**
```css
ul {
  list-style-type: square;
}

ol {
  list-style-type: lower-roman;
}
```

---

**[View Example](../examples/intermediate/13-counters-and-markers/index.html)**

← **Previous Topic:** [Grid Advanced](../intermediate/12-grid-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Filter & Clip Path](../intermediate/14-filter-and-clip-path.md) →
