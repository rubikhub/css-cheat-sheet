# Form Pseudo-classes — Advanced

> 2 pseudo-classes

Direction and language pseudo-classes for forms.

---

## :dir()

**Syntax:** `:dir(ltr)` | `:dir(rtl)`

Selects elements based on text directionality.

**Values:**
- `:dir(ltr)` — left-to-right text
- `:dir(rtl)` — right-to-left text
- `input:dir(rtl)` — input with right-to-left text

**Use Cases:**
- Align text by reading direction
- Style inputs for RTL languages

**Example:**
```css
:dir(ltr) {
  text-align: left;
  padding-left: 1rem;
}

:dir(rtl) {
  text-align: right;
  padding-right: 1rem;
}
```

---

## :lang()

**Syntax:** `:lang(en)` | `:lang(en, fr, de)`

Selects elements based on their language.

**Values:**
- `:lang(en)` — English text
- `:lang(fr)` — French text
- `:lang(ar)` — Arabic text
- `:lang(en, fr, de)` — text in multiple languages

**Use Cases:**
- Apply per-language typography
- Set quotes and direction by language

**Example:**
```css
:lang(en) {
  quotes: "\201C" "\201D";
}

:lang(ar) {
  direction: rtl;
}
```

---

**[View Example](../examples/advanced/12-form-pseudo-classes-advanced/index.html)**

← **Previous Topic:** [Advanced State Pseudo-classes](../advanced/11-state-pseudo-classes-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Cutting-edge Pseudo-elements](../advanced/13-pseudo-elements-cutting-edge.md) →
