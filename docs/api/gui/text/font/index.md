# Font

Represent a text font with a name, style, and size.

Use a Font to change how text looks on a [Label](../label/index.md), [TextField](../textfield/index.md), [TextArea](../textarea/index.md), [Button](../../control/button/index.md), [CheckBox](../../control/checkbox/index.md), or [DropDownList](../../control/dropdownlist/index.md), or in text drawn with a Display's [drawLabel()](../../display/drawLabel.md).

A font's size is in pixels, so a given size looks the same on every kind of object and on every computer.  Text you do not give a font to uses Arial at size 13.

## Creating a Font

You can create a Font using the following functions:

```python
Font(name)
```

```python
Font(name, style, size)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `name` | `str` | _required_ | The font name, for example "Serif", "Dialog", or "TimesRoman". |
| `style` | `tuple` | `PLAIN` | The text style, one of `Font.PLAIN`, `Font.BOLD`, `Font.ITALIC`, or `Font.BOLDITALIC`. |
| `size` | `int` | `-1` | The size, in pixels. If left as the default, size 13 is used. |

For example,

```python
font = Font("Arial", Font.ITALIC, 16)
```

Once created, you can use it with the setFont() function from a [Label](../label/index.md), [TextField](../textfield/index.md), [TextArea](../textarea/index.md), [Button](../../control/button/index.md), [CheckBox](../../control/checkbox/index.md), or [DropDownList](../../control/dropdownlist/index.md) object.

## Functions

Once a Font has been created, the following functions are available:

| Function | Description |
|---|---|
| [`getName()`](getName.md) | Return the font's name. |
| [`setName(name)`](setName.md) | Set the font's name. |
| [`getStyle()`](getStyle.md) | Return the font's style. |
| [`setStyle(style)`](setStyle.md) | Set the font's style. |
| [`getSize()`](getSize.md) | Return the font's size. |
| [`setSize(size)`](setSize.md) | Set the font's size. |
