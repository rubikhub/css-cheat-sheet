# CSS Counters — Complex Patterns

> 4 properties

Advanced counter usage for numbering and list styling.

---

## counter-set

**Syntax:** `counter-set: <name> <value> | none`

Sets the value of a named counter directly.

**Values:**
- `myCounter 0` — set counter to 0
- `myCounter 5` — set counter to 5
- `none` — no counter set (default)
- `a 0 b 0` — set multiple counters at once
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reset a counter to a specific value
- Set a counter without incrementing

**Example:**
```css
.article {
  counter-set: section 1;
}

.warning {
  counter-set: section 0;
}
```

---

## Complex Counter Patterns

---

## counter-reset

**Syntax:** `counter-reset: <name> <start> | none`

Creates or resets a named counter to a starting value.

**Values:**
- `section` — reset counter to 0
- `chapter figure` — reset multiple counters
- `myCounter 5` — start at 5
- `none` — no counter reset (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Restart numbering per container
- Initialize counters for chapters and figures

**Example:**
```css
ol {
  counter-reset: section;
  list-style-type: none;
}

body {
  counter-reset: chapter figure;
}
```

---

## counter-increment

**Syntax:** `counter-increment: <name> <step>`

Increments a named counter by a step value.

**Values:**
- `section` — increment by 1
- `figure` — increment by 1
- `myCounter 2` — increment by 2
- `none` — no counter increment (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Number list items automatically
- Advance chapter counters on headings

**Example:**
```css
ol li {
  counter-increment: section;
}

figure::before {
  counter-increment: figure;
}
```

---

## content: counter()

**Syntax:** `content: counter(<name>, <style>)`

Displays the value of a named counter as generated content.

**Values:**
- `counter(section)` — decimal number
- `counter(section) ". "` — number with punctuation
- `counter(entry, decimal-leading-zero)` — zero-padded number
- `counter(chapter) "." counter(figure)` — combined counters
- `counter(item, upper-roman)` — roman numeral style

**Use Cases:**
- Add automatic numbering before list items
- Generate chapter and figure numbers

**Example:**
```css
ol li::before {
  content: counter(section) ". ";
}

.log-entry::before {
  counter-increment: entry;
  content: counter(entry, decimal-leading-zero) ". ";
}
```

---

**[View Example](../examples/advanced/09-css-counters-complex/index.html)**

← **Previous Topic:** [Border Image & Caret Color](../advanced/08-border-image-and-caret.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Subgrid & Named Grid Lines](../advanced/10-subgrid.md) →
