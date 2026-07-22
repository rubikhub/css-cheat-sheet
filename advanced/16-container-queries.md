# Container Queries

Responsive design based on container size instead of viewport.

---

## container-type
**Type:** keyword | **Initial:** normal

Declares an element as a containment context.

```css
/* Inline size only (most common) */
.card-wrapper {
  container-type: inline-size;
}

/* Both dimensions */
.sidebar {
  container-type: size;
}

/* Block size only */
.column {
  container-type: block-size;
}

/* Global values */
container-type: inherit;
container-type: initial;
```

---

## container-name
**Type:** name | **Initial:** none

Names a container for targeted queries.

```css
.sidebar {
  container-type: inline-size;
  container-name: sidebar;
}

.card {
  container-type: inline-size;
  container-name: card;
}
```

---

## @container
**Type:** at-rule

Applies styles based on container dimensions or style state.

```css
/* Size-based query */
@container (min-width: 500px) {
  .card {
    display: grid;
    grid-template-columns: 200px 1fr;
  }
}

/* Named container */
@container sidebar (max-width: 300px) {
  .nav { font-size: 0.8rem; }
}

/* Style queries */
@container style(--theme: dark) {
  .card { background: #1a1a1a; color: white; }
}
```

```html
<div class="card-wrapper">
  <div class="card">
    <img src="photo.jpg" alt="Photo">
    <div class="card-body">
      <h3>Title</h3>
      <p>Description</p>
    </div>
  </div>
</div>
```

```css
.card-wrapper {
  container-type: inline-size;
  container-name: card;
}

.card {
  display: flex;
  flex-direction: column;
}

@container card (min-width: 500px) {
  .card {
    display: grid;
    grid-template-columns: 200px 1fr;
  }
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
