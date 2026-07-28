# Advanced State Pseudo-classes

Media-state and temporal pseudo-classes for advanced interaction.

---

## :target-within
**Type:** pseudo-class

Selects an element that is a target container (contains the targeted element).

```css
:target-within {
  background: #fffde7;
}
```

---

## :current
**Type:** pseudo-class

Selects the element representing the current item in a navigation or document.

```css
:current {
  font-weight: bold;
}
```

---

## :past
**Type:** pseudo-class

Selects elements that occur before the current time element.

```css
:past {
  opacity: 0.5;
}
```

---

## :future
**Type:** pseudo-class

Selects elements that occur after the current time element.

```css
:future {
  color: gray;
}
```

---

## Media Playback Pseudo-classes

### :playing
```css
video:playing {
  border: 2px solid green;
}

/* Apply when media is playing */
audio:playing + .status {
  color: green;
}
```

### :paused
```css
video:paused {
  border: 2px solid orange;
}
```

### :running
```css
/* Element with running animation */
.box:running {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}
```

### :stopped
```css
video:stopped {
  opacity: 0.5;
}
```

```html
<video src="video.mp4" controls></video>
```

```css
video:playing {
  border: 3px solid #2ecc71;
}

video:paused {
  border: 3px solid #f39c12;
}
```


---

[Example](../examples/advanced/12-state-pseudo-classes-advanced/index.html)

← **Previous Topic:** [:has() — The Parent Selector](../advanced/11-has-selector.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Form Pseudo-classes — Advanced](../advanced/13-form-pseudo-classes-advanced.md) →
