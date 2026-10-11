# getScreenSize()

Return the width and height of the largest [Display](display/index.md) that fits on the screen.

The size leaves room for a display's title bar, and for system-reserved parts of the screen, such as a menu bar, dock, or taskbar.

Set `includeReserved` to True to get the complete screen size instead, including the system-reserved parts.

If there are multiple screens, this returns the primary screen's size.

## Parameters

```python
getScreenSize()
```

```python
getScreenSize(includeReserved)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `includeReserved` | `bool` | `False` | Whether to return the size of the entire screen (True) or of the largest Display that fits on the screen (False).  |

## Returns

`return width, height`

| Value | Type | Description |
|---|---|---|
| width | `int` | The width, in pixels. |
| height | `int` | The height, in pixels. |

For example,

```python
width, height = getScreenSize()
display = Display("Full Screen", width, height)
```