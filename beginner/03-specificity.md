# Specificity

Specificity is the algorithm CSS uses to decide which selector wins when multiple rules target the same element.

> Source: [web.dev/learn/css/specificity](https://web.dev/learn/css/specificity)

---

## How Specificity Works

Specificity is a **three-part score** `(A, B, C)`:

```
(A, B, C)
 │  │  │
 │  │  └── Element/pseudo-element selectors (type)
 │  └──── Class/pseudo-class/attribute selectors
 └─────── ID selectors
```

The selector with the **highest A wins**. If A is tied, compare B. If B is tied, compare C. If all are tied, the last declaration wins.

---

## Specificity Scores by Selector Type

| Selector Type | Increments | Example | Score |
|---------------|-----------|---------|-------|
| Universal `*` | None | `*` | `(0,0,0)` |
| Element / pseudo-element | C | `div`, `::before` | `(0,0,1)` |
| Class / pseudo-class / attribute | B | `.btn`, `:hover`, `[type]` | `(0,1,0)` |
| ID | A | `#main` | `(1,0,0)` |

---

## Examples

```css
/* (0,0,1) */
p { color: red; }

/* (0,1,0) — WINS */
.intro { color: blue; }

/* (1,0,0) — WINS over everything above */
#hero { color: green; }
```

### Compound Selectors

```css
/* (0,0,1) */
a { color: red; }

/* (0,1,1) — WINS */
a.my-class { color: green; }

/* (0,2,1) */
a.my-class.another-class { color: blue; }

/* (0,3,1) */
a.my-class.another-class[href] { color: purple; }

/* (0,4,1) — WINS */
a.my-class.another-class[href]:hover { color: orange; }
```

---

## Common Pitfalls

### IDs are very specific

```css
/* (1,0,0) — hard to override */
#sidebar { width: 300px; }

/* (0,2,0) — still loses to ID */
.sidebar-widget .nav { width: 250px; }
```

### Chained classes add up

```css
/* (0,3,0) — very high for class selectors */
.card.primary.featured { border: 2px solid gold; }
```

---

## Boosting Specificity (Sparingly)

If you need to override a rule without using `!important`, you can repeat the class:

```css
/* Original */
.button { background: blue; }

/* Boosted to (0,2,0) */
.button.button { background: green; }
```

---

## Tie-Breaking

When two rules have **identical specificity**, the one declared **last** wins:

```css
/* (0,1,0) */
.first { color: red; }

/* (0,1,0) — WINS (last declaration) */
.second { color: blue; }
```

---

## Specificity vs Cascade

Specificity is just one stage of the cascade. Before specificity is even considered, the cascade checks:
1. Origin (user agent vs authored)
2. `!important` declarations

Inline styles (`style=""`) are resolved at a different cascade step, not through specificity.

---

## Quick Reference

| Selector | Specificity |
|----------|-------------|
| `*` | `(0,0,0)` |
| `p` | `(0,0,1)` |
| `.intro` | `(0,1,0)` |
| `#main` | `(1,0,0)` |
| `#main p.intro` | `(1,1,1)` |


---

**[View Example](../examples/beginner/03-specificity/index.html)**

← **Previous Topic:** [The Cascade](../beginner/02-the-cascade.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Inheritance](../beginner/04-inheritance.md) →
