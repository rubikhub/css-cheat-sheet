# Background Blend Mode

> 1 property

Controls how multiple background layers blend together.

---

## background-blend-mode

**Syntax:** `background-blend-mode: normal | multiply | screen | overlay | darken | lighten | color-dodge | color-burn | hard-light | soft-light | difference | exclusion | hue | saturation | color | luminosity`

Determines how each background layer blends with the layers below it.

**Values:**
- `normal` — no blending (default)
- `multiply` — darkens by multiplying colors
- `screen` — lightens by inverting and multiplying
- `overlay` — combines multiply and screen
- `darken` — keeps the darker color of each layer
- `lighten` — keeps the lighter color of each layer
- `color-dodge` — brightens the bottom layer
- `color-burn` — darkens the bottom layer
- `hard-light` — strong contrast blend
- `soft-light` — soft glow blend
- `difference` — subtracts the darker from the lighter color
- `exclusion` — similar to difference with less contrast
- `hue` — uses hue of the top layer
- `saturation` — uses saturation of the top layer
- `color` — uses hue and saturation of the top layer
- `luminosity` — uses luminosity of the top layer
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Blend multiple background layers together
- Create texture and gradient photo effects

**Example:**
```css
.blend {
  background: linear-gradient(#ff6b6b, #4d96ff),
              linear-gradient(45deg, #ffd93d, #6bcb77);
  background-blend-mode: multiply;
}
```

---

**[View Example](../examples/advanced/05-background-blend-mode/index.html)**

← **Previous Topic:** [Advanced Color Functions](../advanced/04-color-functions-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography — OpenType & Variable Font Features](../advanced/06-typography-ot-features.md) →
