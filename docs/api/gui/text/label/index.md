# Label

Create a label that shows a line of text.

A label starts out just big enough for its text.  If you give it another size (with [setSize()](../../common/size/setSize.md), or with `resize=False` in [setText()](setText.md) or [setFont()](setFont.md)), the text lines up inside it by the label's alignment, centered top to bottom, and any text that does not fit is cut off.

## Creating a Label

You can create a Label using the following functions:

```python
Label(text)
```

```python
Label(text, alignment, textColor, backgroundColor, font, visibility)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `text` | `str` | _required_ | The text to show. |
| `alignment` | `int` | `LEFT` | How the text lines up, one of `LEFT`, `CENTER`, or `RIGHT`. |
| `textColor` | `Color` | `Color.BLACK` | The text color. |
| `backgroundColor` | `Color` | `Color.CLEAR` | The color behind the text. Defaults to transparent. |
| `font` | `Font` | `None` | The font, for example `Font("Serif", Font.ITALIC, 16)`. If omitted, the default font (Arial, size 13) is used. |
| `visibility` | `int` | `100` | How visible the label is, from 0 (invisible) to 100 (fully visible). |

For example,

```python
label = Label("Hello World!")
```

Once created, you can add it to a [Display](../../display/index.md) using the Display's [add()](../../display/add.md) function.

## Functions

Once a Label has been created, the following functions are available:

| Function | Description |
|---|---|
| [`getText()`](getText.md) | Return the label's text. |
| [`setText(text)`](setText.md) | Set the label's text. |
| [`getAlignment()`](getAlignment.md) | Return how the label's text lines up. |
| [`setAlignment(alignment)`](setAlignment.md) | Set how the label's text lines up. |
| [`getFont()`](getFont.md) | Return the label's font. |
| [`setFont(font)`](setFont.md) | Set the label's font. |
| [`getColor()`](../../common/color/getColor.md) | Return the label's background color. |
| [`setColor(color)`](../../common/color/setColor.md) | Set the label's background color. |
| [`getTextColor()`](getTextColor.md) | Return the label's text color. |
| [`setTextColor(color)`](setTextColor.md) | Set the label's text color. |
| [`getBackgroundColor()`](getBackgroundColor.md) | Return the label's background color.  Same as `getColor()`. |
| [`setBackgroundColor(color)`](setBackgroundColor.md) | Set the label's background color.  Same as `setColor()`. |

Additionally, the following common functions are available:

- [Position](../../common/index.md#position-functions)
- [Size](../../common/index.md#size-functions)
- [Rotation](../../common/index.md#rotation-functions)
- [Visibility](../../common/index.md#visibility-functions)
- [Color](../../common/index.md#color-functions)
- [Information](../../common/index.md#information-functions)
- [Hit Testing](../../common/index.md#hit-testing-functions)
- [Events](../../common/index.md#event-functions)
