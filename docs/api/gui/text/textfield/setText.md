# setText()

Set the text in the field.

By default the field keeps its size, since its text often changes while in use.

## Parameters

Once an object `field` has been created, you can use the following functions:

```python
field.setText(text)
```

```python
field.setText(text, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `text` | `str` | _required_ | The new contents of the field. |
| `resize` | `bool` | `False` | `True` to resize the field to fit the new text, or `False` to keep its current size. |
