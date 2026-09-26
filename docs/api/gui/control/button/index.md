# Button

Create a clickable button that can be pressed by the user.

Pressing a Button calls a function, specified when the button is created.

## Creating a Button

You can create a Button using the following functions:

```python
Button()
```

```python
Button(text, action, color, textColor, font, rotation, visibility)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `text` | `str` | `''` | The text shown on the button. |
| `action` | `function` | `None` | The function to call each time the button is pressed; it receives no parameters. |
| `color` | `Color` | `Color.WHITE` | The button's background color. |
| `textColor` | `Color` | `Color.BLACK` | The text color. |
| `font` | `Font` | `None` | The font, for example `Font("Serif", Font.ITALIC, 16)`. If omitted, the default font (Arial, size 13) is used. |
| `rotation` | `int or float` | `0` | How far to turn the button, in degrees, counter-clockwise. |
| `visibility` | `int` | `100` | How visible the button is, from 0 (invisible) to 100 (fully visible). |

For example,

```python
button = Button("Play music", playMusic)
```

where `playMusic` is a function with zero parameters.  This function will be called automatically when the user presses this button.

Once created, you can add it to a [Display](../../display/index.md) using the Display's [add()](../../display/add.md) function.

## Functions

Once a Button has been created, the following functions are available:

| Function | Description |
|---|---|
| [`getText()`](getText.md) | Return the button's text. |
| [`setText(text)`](setText.md) | Set the button's text. |
| [`getColor()`](../../common/color/getColor.md) | Return the button's background color. |
| [`setColor(color)`](../../common/color/setColor.md) | Set the button's background color. |
| [`getTextColor()`](getTextColor.md) | Return the button's text color. |
| [`setTextColor(color)`](setTextColor.md) | Set the button's text color. |
| [`getFont()`](getFont.md) | Return the button's font. |
| [`setFont(font)`](setFont.md) | Set the button's font. |

Additionally, the following common functions are available:

- [Position](../../common/index.md#position-functions)
- [Size](../../common/index.md#size-functions)
- [Rotation](../../common/index.md#rotation-functions)
- [Visibility](../../common/index.md#visibility-functions)
- [Information](../../common/index.md#information-functions)
- [Hit Testing](../../common/index.md#hit-testing-functions)
- [Events](../../common/index.md#event-functions)
