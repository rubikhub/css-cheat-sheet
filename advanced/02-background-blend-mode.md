# Background Blend Mode

Controls how multiple background layers blend together.

---

## background-blend-mode
**Type:** keyword | **Initial:** normal

Determines how each background layer blends with the layers below it.

```css
/* Single value */
background-blend-mode: multiply;
background-blend-mode: screen;
background-blend-mode: overlay;
background-blend-mode: darken;
background-blend-mode: lighten;
background-blend-mode: color-dodge;
background-blend-mode: color-burn;
background-blend-mode: hard-light;
background-blend-mode: soft-light;
background-blend-mode: difference;
background-blend-mode: exclusion;
background-blend-mode: hue;
background-blend-mode: saturation;
background-blend-mode: color;
background-blend-mode: luminosity;
background-blend-mode: normal;

/* Global values */
background-blend-mode: inherit;
background-blend-mode: initial;
```

```html
<div class="blend-multiply">multiply</div>
<div class="blend-screen">screen</div>
<div class="blend-overlay">overlay</div>
```

```css
.blend-multiply {
  height: 55px;
  border-radius: 6px;
  background: linear-gradient(#ff6b6b, #4d96ff),
              linear-gradient(45deg, #ffd93d, #6bcb77);
  background-blend-mode: multiply;
}

.blend-screen {
  height: 55px;
  border-radius: 6px;
  background: linear-gradient(#ff6b6b, #4d96ff),
              linear-gradient(45deg, #ffd93d, #6bcb77);
  background-blend-mode: screen;
}

.blend-overlay {
  height: 55px;
  border-radius: 6px;
  background: linear-gradient(#ff6b6b, #4d96ff),
              linear-gradient(45deg, #ffd93d, #6bcb77);
  background-blend-mode: overlay;
}
```


---

[Example](../examples/advanced/02-background-blend-mode/index.html)

← **Previous Topic:** [Typography — OpenType & Variable Font Features](../advanced/01-typography-ot-features.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Image & Caret Color](../advanced/03-border-image-and-caret.md) →
