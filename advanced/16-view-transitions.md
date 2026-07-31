# View Transitions

> 6 features

Cross-document and in-page view transitions — pseudo-elements and the enabling at-rule.

---

## ::view-transition

**Syntax:** `::view-transition`

The root pseudo-element wrapping the entire view transition.

**Values:**
- `::view-transition` — the root transition container

**Use Cases:**
- Style the transition overlay
- Set fixed positioning for the snapshot layer

**Example:**
```css
::view-transition {
  position: fixed;
  inset: 0;
}
```

---

## ::view-transition-group()

**Syntax:** `::view-transition-group(<name>)`

Targets a specific view transition group by name.

**Values:**
- `::view-transition-group(hero)` — the hero element's group
- `::view-transition-group(page)` — the page's group

**Use Cases:**
- Animate different groups at different speeds
- Control the layout of transition snapshots

**Example:**
```css
::view-transition-group(hero) {
  animation-duration: 0.5s;
}

::view-transition-group(page) {
  animation-duration: 0.3s;
}
```

---

## ::view-transition-image-pair()

**Syntax:** `::view-transition-image-pair(<name>)`

Targets the before/after image pair of a transition.

**Values:**
- `::view-transition-image-pair(hero)` — the old and new state pair

**Use Cases:**
- Blend or mask the old and new snapshots
- Customize how states layer during a transition

**Example:**
```css
::view-transition-image-pair(hero) {
  mix-blend-mode: normal;
}
```

---

## ::view-transition-old()

**Syntax:** `::view-transition-old(<name>)`

Targets the old (outgoing) state of a view transition.

**Values:**
- `::view-transition-old(hero)` — the outgoing hero snapshot

**Use Cases:**
- Create exit animations
- Fade out the old page state

**Example:**
```css
::view-transition-old(hero) {
  animation: fade-out 0.3s ease;
}
```

---

## ::view-transition-new()

**Syntax:** `::view-transition-new(<name>)`

Targets the new (incoming) state of a view transition.

**Values:**
- `::view-transition-new(hero)` — the incoming hero snapshot

**Use Cases:**
- Create entrance animations
- Fade in the new page state

**Example:**
```css
::view-transition-new(hero) {
  animation: fade-in 0.3s ease;
}
```

---

## @view-transition

**Syntax:** `@view-transition { navigation: auto; }`

Enables view transitions for navigation.

**Values:**
- `navigation: auto` — enable transitions for navigation
- `navigation: same-document` — same-document navigation only
- `navigation: none` — disable transitions

**Use Cases:**
- Enable cross-document view transitions
- Opt into animated page navigations

**Example:**
```css
@view-transition {
  navigation: auto;
}
```

---

**[View Example](../examples/advanced/16-view-transitions/index.html)**

← **Previous Topic:** [Cutting-edge Pseudo-elements](../advanced/15-pseudo-elements-cutting-edge.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scrollbar Styling](../advanced/17-scrollbar-styling.md) →

