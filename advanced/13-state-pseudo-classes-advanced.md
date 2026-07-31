# Advanced State Pseudo-classes

> 8 pseudo-classes

Media-state and temporal pseudo-classes for advanced interaction.

---

## :target-within

**Syntax:** `:target-within`

Selects an element that is a target container (contains the targeted element).

**Values:**
- `:target-within` — element that contains the target
- `section:target-within` — section that contains the target

**Use Cases:**
- Highlight a parent when a nested item is targeted
- Style containers around anchored content

**Example:**
```css
:target-within {
  background: #fffde7;
}
```

---

## :current

**Syntax:** `:current`

Selects the element representing the current item in a navigation or document.

**Values:**
- `:current` — current item in the document
- `nav a:current` — current link in navigation

**Use Cases:**
- Highlight the current slide or section
- Style the active item in a navigation

**Example:**
```css
:current {
  font-weight: bold;
}
```

---

## :past

**Syntax:** `:past`

Selects elements that occur before the current time element.

**Values:**
- `:past` — content before the current element
- `li:past` — list items already passed

**Use Cases:**
- Dim content already read in transcripts
- Style previously viewed slides

**Example:**
```css
:past {
  opacity: 0.5;
}
```

---

## :future

**Syntax:** `:future`

Selects elements that occur after the current time element.

**Values:**
- `:future` — content after the current element
- `li:future` — list items yet to come

**Use Cases:**
- Style upcoming content in timed media
- Distinguish pending slides from the current one

**Example:**
```css
:future {
  color: gray;
}
```

---

## Media Playback Pseudo-classes

---

## :playing

**Syntax:** `:playing`

Selects media elements that are currently playing.

**Values:**
- `video:playing` — playing video
- `audio:playing + .status` — status label beside playing audio

**Use Cases:**
- Highlight playing media
- Show a now-playing indicator

**Example:**
```css
video:playing {
  border: 2px solid green;
}

audio:playing + .status {
  color: green;
}
```

---

## :paused

**Syntax:** `:paused`

Selects media elements that are paused.

**Values:**
- `video:paused` — paused video
- `audio:paused` — paused audio

**Use Cases:**
- Show a paused state visually
- Style playback controls by state

**Example:**
```css
video:paused {
  border: 2px solid orange;
}
```

---

## :running

**Syntax:** `:running`

Selects elements with running animations.

**Values:**
- `.box:running` — element with an active animation

**Use Cases:**
- Apply shadows to animating elements
- Detect active animations for styling

**Example:**
```css
.box:running {
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
}
```

---

## :stopped

**Syntax:** `:stopped`

Selects media elements or animations that have stopped.

**Values:**
- `video:stopped` — stopped video
- `audio:stopped` — stopped audio

**Use Cases:**
- Dim finished media
- Style the stopped playback state

**Example:**
```css
video:stopped {
  opacity: 0.5;
}
```

---

**[View Example](../examples/advanced/13-state-pseudo-classes-advanced/index.html)**

← **Previous Topic:** [Subgrid & Named Grid Lines](../advanced/12-subgrid.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Form Pseudo-classes — Advanced](../advanced/14-form-pseudo-classes-advanced.md) →

