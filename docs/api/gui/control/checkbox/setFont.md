# setFont()

Set the checkbox's [Font](../../text/font/index.md).

## Parameters

Once an object `checkbox` has been created, you can use the following functions:

```python
checkbox.setFont(font)
```

```python
checkbox.setFont(font, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `font` | `Font` | _required_ | The new font, for example `Font("Serif", Font.ITALIC, 16)`. |
| `resize` | `bool` | `True` | `True` to refit the checkbox to its text in the new font, or `False` to keep its current size. |
