# Text Decoration

> 6 properties

Decorative lines and underlines — line, style, color, thickness, and offset.

---

## text-decoration

**Syntax:** `text-decoration: none | <line> <style> <color>`

Line decoration — underline, overline, or line-through with style and color.

**Values:**
- `none` — no decoration (default)
- `underline` — line under text
- `overline` — line above text
- `line-through` — line through text
- `underline wavy red` — shorthand with style and color
- `underline dotted` — shorthand with style
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style link underlines
- Add emphasis with strike-through

**Example:**
```css
a {
  text-decoration: underline wavy #0066cc;
}
```

---

## text-decoration-line

**Syntax:** `text-decoration-line: none | underline | overline | line-through`

Which lines to decorate — underline, overline, line-through.

**Values:**
- `none` — no decoration (default)
- `underline` — line under text
- `overline` — line above text
- `line-through` — line through text
- `underline overline` — multiple lines
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add underlines to links
- Combine lines for emphasis

**Example:**
```css
a {
  text-decoration-line: underline;
}

del {
  text-decoration-line: line-through;
}
```

---

## text-decoration-style

**Syntax:** `text-decoration-style: solid | double | dotted | dashed | wavy`

Decoration style — solid, dashed, dotted, double, wavy.

**Values:**
- `solid` — solid line (default)
- `dashed` — dashed line
- `dotted` — dotted line
- `double` — double line
- `wavy` — wavy line
- `inherit` — inherits from parent
- `initial` — sets to default (solid)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add wavy underlines for warnings
- Style link underlines

**Example:**
```css
.warning {
  text-decoration-line: underline;
  text-decoration-style: wavy;
  text-decoration-color: #d32f2f;
}
```

---

## text-decoration-color

**Syntax:** `text-decoration-color: <color>`

Decoration color — independent of text color.

**Values:**
- `currentColor` — matches text color (default)
- `red` — named color
- `#a3a3a3` — hex color
- `inherit` — inherits from parent
- `initial` — sets to default (currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Highlight links with colored underlines
- Match decoration to brand colors

**Example:**
```css
a {
  text-decoration: underline;
  text-decoration-color: #0066cc;
}
```

---

## text-decoration-thickness

**Syntax:** `text-decoration-thickness: auto | from-font | <length> | <percentage>`

Thickness of the decoration line — precise control over underline weight.

**Values:**
- `auto` — browser-determined thickness (default)
- `from-font` — use the font's specified thickness
- `1px` — thin line
- `3px` — thick line
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make underlines thinner or bolder
- Keep underline weight consistent

**Example:**
```css
a {
  text-decoration: underline;
  text-decoration-thickness: 2px;
}
```

---

## text-underline-offset

**Syntax:** `text-underline-offset: auto | from-font | <length> | <percentage>`

Distance from baseline to underline — adjusts underline position.

**Values:**
- `auto` — default position (default)
- `from-font` — use the font's specified offset
- `1px` — close to text
- `4px` — small gap
- `8px` — far from text
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add breathing room under underlined links
- Align underlines with descenders

**Example:**
```css
a {
  text-decoration: underline;
  text-underline-offset: 4px;
}
```

---

**[View Example](../examples/intermediate/06-text-decoration/index.html)**

← **Previous Topic:** [Typography Advanced](../intermediate/05-typography-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Text Layout & Wrapping](../intermediate/07-text-layout.md) →

