# CSS Counters — Complex Patterns

Advanced counter usage for numbering and list styling.

---

## counter-set
**Type:** counter | none | **Initial:** none

Sets the value of a named counter directly.

```css
counter-set: myCounter 0;
counter-set: myCounter 5;
counter-set: none;

/* Multiple counters */
counter-set: a 0 b 0;

/* Global values */
counter-set: inherit;
counter-set: initial;
```

---

## Complex Counter Patterns

### Nested Counters
```css
ol {
  counter-reset: section;
  list-style-type: none;
}

ol li {
  counter-increment: section;
}

ol li::before {
  content: counter(section) ". ";
}

/* Nested list with sub-counters */
ol ol {
  counter-reset: subsection;
}

ol ol li {
  counter-increment: subsection;
}

ol ol li::before {
  content: counter(section) "." counter(subsection) " ";
}
```

### Counter with custom formatting
```css
/* Roman numerals */
counter-reset: roman;
list-style-type: upper-roman;

/* Letters */
counter-reset: alpha;
list-style-type: lower-alpha;
```

### Counters for chapter numbering
```css
body {
  counter-reset: chapter figure;
}

h2 {
  counter-increment: chapter;
  counter-reset: figure;
}

h2::before {
  content: "Chapter " counter(chapter) ": ";
}

figure::before {
  counter-increment: figure;
  content: "Figure " counter(chapter) "." counter(figure) " — ";
}
```

### Counters for ordered output
```css
.log {
  counter-reset: entry;
}

.log-entry::before {
  counter-increment: entry;
  content: counter(entry, decimal-leading-zero) ". ";
}
```


---

[Example](../examples/advanced/09-css-counters-complex/index.html)

← **Previous Topic:** [Advanced Visual Effects](../advanced/08-advanced-effects.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scroll Snap & Touch Interaction](../advanced/10-scroll-snap.md) →
