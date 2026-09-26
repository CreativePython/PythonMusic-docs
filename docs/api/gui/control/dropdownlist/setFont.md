# setFont()

Set the list's [Font](../../text/font/index.md).

## Parameters

Once an object `dropdown` has been created, you can use the following functions:

```python
dropdown.setFont(font)
```

```python
dropdown.setFont(font, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `font` | `Font` | _required_ | The new font, for example `Font("Serif", Font.ITALIC, 16)`. |
| `resize` | `bool` | `True` | `True` to refit the list to its longest item in the new font, or `False` to keep its current size. |
