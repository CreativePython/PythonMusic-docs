# setFont()

Set the area's [Font](../font/index.md).

## Parameters

Once an object `area` has been created, you can use the following functions:

```python
area.setFont(font)
```

```python
area.setFont(font, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `font` | `Font` | _required_ | The new font, for example `Font("Serif", Font.ITALIC, 16)`. |
| `resize` | `bool` | `True` | `True` to refit the area to its columns and rows of text in the new font, or `False` to keep its current size. |
