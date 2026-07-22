# Nesting
---
## Container Properties
### CSS Nesting
**Type/Initial:** feature | (none)

**Description:** Native CSS nesting allows nesting selectors inside other selectors.

**CSS:**
```css
/* Basic nesting */
.card {
  padding: 1rem;
  background: white;

  & .title {
    font-size: 1.2rem;
    font-weight: bold;
  }

  & .content {
    margin-top: 0.5rem;
  }
}

/* Nesting with & */
.nav {
  display: flex;
  gap: 1rem;

  & a {
    text-decoration: none;
    color: blue;

    &:hover {
      color: red;
    }

    &.active {
      font-weight: bold;
    }
  }
}

/* Nesting pseudo-classes */
.button {
  padding: 0.5rem 1rem;
  background: blue;
  color: white;

  &:hover {
    background: darkblue;
  }

  &:active {
    transform: scale(0.95);
  }

  &:disabled {
    background: gray;
  }
}

/* Nesting media queries */
.container {
  max-width: 1200px;
  margin: 0 auto;

  @media (max-width: 768px) {
    padding: 1rem;
  }
}

/* Nesting compound selectors */
.link {
  color: blue;

  &.visited {
    color: purple;
  }

  &.external::after {
    content: " ↗";
  }
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    parent
    <div class="db style-c">
      nested child
    </div>
  </div>
  <div class="db style-d">
    another parent
    <div class="db style-e">
      another nested child
    </div>
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 1rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 2px solid blue;
}
.style-c {
  background: #f5f5f5;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  margin-top: 0.5rem;
  border-left: 3px solid green;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 2px solid blue;
}
.style-e {
  background: #f5f5f5;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  margin-top: 0.5rem;
  border-left: 3px solid green;
}
```