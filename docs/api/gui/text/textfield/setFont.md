# setFont()

Set the field's [Font](../font/index.md).

## Parameters

Once an object `field` has been created, you can use the following functions:

```python
field.setFont(font)
```

```python
field.setFont(font, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `font` | `Font` | _required_ | The new font, for example `Font("Serif", Font.ITALIC, 16)`. |
| `resize` | `bool` | `True` | `True` to refit the field to its columns of text in the new font, or `False` to keep its current size. |
