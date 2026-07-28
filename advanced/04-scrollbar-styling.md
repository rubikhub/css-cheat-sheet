# Scrollbar Styling

Customize scrollbar appearance and width.

---

## scrollbar-color
**Type:** color | **Initial:** auto

Sets the track and thumb colors of the scrollbar.

```css
/* Two colors: thumb, track */
scrollbar-color: #888 #f1f1f1;
scrollbar-color: #333 transparent;
scrollbar-color: currentColor transparent;

scrollbar-color: auto;

/* Global values */
scrollbar-color: inherit;
scrollbar-color: initial;
```

---

## scrollbar-width
**Type:** keyword | **Initial:** auto

Controls the thickness of the scrollbar.

```css
scrollbar-width: auto;
scrollbar-width: thin;
scrollbar-width: none;

/* Global values */
scrollbar-width: inherit;
scrollbar-width: initial;
```

```html
<div class="custom-scrollbar">
  <p>Long content...</p>
</div>
```

```css
.custom-scrollbar {
  height: 200px;
  overflow-y: scroll;
  scrollbar-color: #888 #f1f1f1;
  scrollbar-width: thin;
}
```


---

[Example](../examples/advanced/04-scrollbar-styling/index.html)

← **Previous Topic:** [Border Image & Caret Color](../advanced/03-border-image-and-caret.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Subgrid & Named Grid Lines](../advanced/05-subgrid.md) →
