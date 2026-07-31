# View Transitions

> 12 features

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

## view-transition-name

**Syntax:** `view-transition-name: none | <custom-ident>`

Assigns an element to a named view transition group.

**Values:**
- `none` — element takes no part in transitions (default)
- `hero` — name a group to animate separately

**Use Cases:**
- Morph a shared element between pages
- Control per-element transition snapshots

**Example:**
```css
.page-hero {
  view-transition-name: hero;
}
```

---

## view-transition-class

**Syntax:** `view-transition-class: none | <custom-ident>*`

Applies the same styles to multiple view transition groups.

**Values:**
- `card` — group several elements under one class
- `none` — no class (default)

**Use Cases:**
- Animate all cards with one rule
- Avoid repeating group-name selectors

**Example:**
```css
.card {
  view-transition-name: card-1;
  view-transition-class: card;
}

::view-transition-group(.card) {
  animation-duration: 0.4s;
}
```

---

## :active-view-transition

**Syntax:** `:active-view-transition`

Selects the root of a view transition while it is running.

**Values:**
- `:active-view-transition` — the running transition root
- `:active-view-transition::view-transition-group(*)>::view-transition-image-pair(*)` — style active snapshots

**Use Cases:**
- Detect a running transition in CSS
- Style the root while the transition plays

**Example:**
```css
:active-view-transition {
  cursor: progress;
}
```

---

## :active-view-transition-type()

**Syntax:** `:active-view-transition-type(<types>)`

Selects a running view transition of a specific type.

**Values:**
- `:active-view-transition-type(back)` — the back-navigation transition
- `:active-view-transition-type(forward)` — the forward transition

**Use Cases:**
- Direction-aware transition styling
- Differentiate back vs forward navigations

**Example:**
```css
:active-view-transition-type(back)::view-transition-old(root) {
  animation-name: slide-out-right;
}
```

---

## Nested & Group View Transitions

**Syntax:** `view-transition-name` on nested elements + `::view-transition-group(<name>)`

Creates multiple nested groups so child and parent animations compose.

**Values:**
- Name child elements separately from the page root
- Animate the child group inside the parent snapshot

**Use Cases:**
- Morph one element into another across layouts
- Keep internal groups animating during a page transition

**Example:**
```css
.card {
  view-transition-name: card;
}

.card img {
  view-transition-name: card-image;
}
```

---

## Cross-document View Transitions

**Syntax:** `@view-transition { navigation: auto; }`

Transitions animate between whole documents during same-origin navigation.

**Values:**
- `navigation: auto` — enable transitions for navigation
- `navigation: same-document` — same-document navigations only
- `navigation: none` — disable
- Combined with `view-transition-name` on shared elements

**Use Cases:**
- Animate shared hero elements between pages
- Add smooth page-to-page transitions

**Example:**
```css
@view-transition {
  navigation: auto;
}

.page-title {
  view-transition-name: title;
}
```

---

**[View Example](../examples/advanced/16-view-transitions/index.html)**

← **Previous Topic:** [Cutting-edge Pseudo-elements](../advanced/15-pseudo-elements-cutting-edge.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scrollbar Styling](../advanced/17-scrollbar-styling.md) →

