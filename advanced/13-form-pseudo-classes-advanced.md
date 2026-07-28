# Form Pseudo-classes — Advanced

Direction and language pseudo-classes for forms.

---

## :dir()
**Type:** pseudo-class

Selects elements based on text directionality.

```css
/* Left-to-right */
:dir(ltr) {
  text-align: left;
  padding-left: 1rem;
}

/* Right-to-left */
:dir(rtl) {
  text-align: right;
  padding-right: 1rem;
}

/* Specific element */
input:dir(rtl) {
  text-align: right;
}
```

---

## :lang()
**Type:** pseudo-class

Selects elements based on their language.

```css
/* English text */
:lang(en) {
  quotes: "\201C" "\201D";
}

/* French text */
:lang(fr) {
  quotes: "\00AB" "\00BB";
}

/* Arabic text */
:lang(ar) {
  direction: rtl;
  font-family: 'Arabic Font', serif;
}

/* Specific language ranges */
:lang(en, fr, de) {
  font-family: 'Latin Font', sans-serif;
}
```

```html
<p lang="en">"Hello world"</p>
<p lang="fr">"Bonjour le monde"</p>
<p lang="ar" dir="rtl">مرحبا بالعالم</p>
```

```css
:lang(en) {
  quotes: "\201C" "\201D";
}

:lang(fr) {
  quotes: "\00AB" "\00BB";
}

:lang(ar) {
  quotes: "\300E" "\300F";
  direction: rtl;
}
```


---

[Example](../examples/advanced/13-form-pseudo-classes-advanced/index.html)

← **Previous Topic:** [Advanced State Pseudo-classes](../advanced/12-state-pseudo-classes-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Cutting-edge Pseudo-elements](../advanced/14-pseudo-elements-cutting-edge.md) →
