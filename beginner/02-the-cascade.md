# The Cascade

CSS stands for **Cascading** Stylesheets. The cascade is the algorithm that resolves conflicts when multiple CSS rules target the same element.

> Source: [web.dev/learn/css/the-cascade](https://web.dev/learn/css/the-cascade)

---

## How the Cascade Works

When two or more CSS rules match the same element with conflicting declarations, the cascade determines which one wins. It follows **4 stages** in order:

```
1. Position and Order of Appearance
2. Specificity
3. Origin
4. Importance
```

---

## Stage 1: Position & Order of Appearance

When two rules have the same specificity and origin, the **last one declared** wins.

```css
button {
  color: red;
}

button {
  color: blue;
}

/* Result: blue — because it comes last */
```

This applies to:
- Rules in the same stylesheet
- Rules in different `<style>` or `<link>` elements (later = wins)
- Declarations within the same rule (last one wins)

```css
.element {
  background: green;
  background: purple;
}

/* Result: purple — last declaration wins */
```

---

## Stage 2: Specificity

A scoring system that determines which selector is more specific. Higher specificity wins.

```css
/* Specificity: (0,0,1) */
p { color: red; }

/* Specificity: (0,1,0) — WINS */
.highlight { color: blue; }
```

The selector `.highlight` is more specific than `p`, so blue wins even though `p` comes first.

See the [Specificity](./19-specificity.md) lesson for full details.

---

## Stage 3: Origin

CSS comes from different sources. The cascade ranks them:

```
Least specific → Most specific:

1. User agent base styles (browser defaults)
2. Local user styles (OS settings, browser extensions)
3. Authored CSS (your stylesheet)
4. Authored !important
5. Local user !important
6. User agent !important
```

Example: A user's custom CSS with `!important` will override your authored styles without `!important`.

---

## Stage 4: Importance

Some declarations are weighted more heavily than others:

```
Least important → Most important:

1. Normal declarations
2. @animation declarations
3. !important declarations (following origin order)
4. @transition declarations
```

### Using `!important`

```css
/* Normal rule */
.button {
  color: blue;
}

/* !important overrides normal rules regardless of specificity */
.button-special {
  color: red !important;
}
```

**Caution:** Avoid `!important` when possible. It makes CSS harder to maintain and override.


---

## Quick Reference

| Stage | What It Resolves |
|-------|-----------------|
| Position | Which rule comes last |
| Specificity | Which selector is strongest |
| Origin | Where the CSS comes from |
| Importance | `!important`, `animation`, `transition` |

---

## Debugging

Browser DevTools shows all matching CSS rules, with losing rules crossed out. This helps you understand why a particular style is or isn't being applied.
