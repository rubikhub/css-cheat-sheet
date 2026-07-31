# Container Queries

> 3 properties

Responsive design based on container size instead of viewport.

---

## container-type

**Syntax:** `container-type: inline-size | size | block-size | normal`

Declares an element as a containment context.

**Values:**
- `inline-size` — inline size containment only (most common)
- `size` — containment on both dimensions
- `block-size` — block size containment only
- `normal` — no containment (default)
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create size-based responsiveness
- Build self-contained card layouts

**Example:**
```css
.card-wrapper {
  container-type: inline-size;
}

.sidebar {
  container-type: size;
}
```

---

## container-name

**Syntax:** `container-name: <name> | none`

Names a container for targeted queries.

**Values:**
- `sidebar` — named container for sidebar queries
- `card` — named container for card queries
- `none` — no container name (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Target a specific container with @container
- Support multiple container types on one page

**Example:**
```css
.sidebar {
  container-type: inline-size;
  container-name: sidebar;
}
```

---

## @container

**Syntax:** `@container (<condition>) { ... }` | `@container <name> (<condition>) { ... }`

Applies styles based on container dimensions or style state.

**Values:**
- `@container (min-width: 500px)` — size-based query
- `@container sidebar (max-width: 300px)` — query a named container
- `@container style(--theme: dark)` — style query

**Use Cases:**
- Adapt components to their container width
- Apply styles based on container state

**Example:**
```css
@container (min-width: 500px) {
  .card {
    display: grid;
    grid-template-columns: 200px 1fr;
  }
}

@container style(--theme: dark) {
  .card { background: #1a1a1a; color: white; }
}
```

---

## Container Query Units

| Unit | Description |
|------|-------------|
| `cqw` | 1% of container width |
| `cqh` | 1% of container height |
| `cqi` | 1% of container inline size |
| `cqb` | 1% of container block size |
| `cqmin` | Smaller of cqi and cqb |
| `cqmax` | Larger of cqi and cqb |

```css
.card-title {
  font-size: clamp(1rem, 3cqi, 1.5rem);
}
```

---

**[View Example](../examples/advanced/16-container-queries/index.html)**

← **Previous Topic:** [CSS At-Rules — Advanced](../advanced/15-at-rules.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Selectors 2024+](../advanced/17-selectors-2024.md) →
