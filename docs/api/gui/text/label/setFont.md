# setFont()

Set the label's [Font](../font/index.md).

## Parameters

Once an object `label` has been created, you can use the following functions:

```python
label.setFont(font)
```

```python
label.setFont(font, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `font` | `Font` | _required_ | The new font, for example `Font("Serif", Font.ITALIC, 16)`. |
| `resize` | `bool` | `True` | `True` to resize the label to fit its text in the new font, or `False` to keep its current size (text that does not fit is cut off). |
