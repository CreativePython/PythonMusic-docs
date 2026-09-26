# setText()

Set the label's text.

## Parameters

Once an object `label` has been created, you can use the following functions:

```python
label.setText(text)
```

```python
label.setText(text, resize)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `text` | `str` | _required_ | The new text. |
| `resize` | `bool` | `True` | `True` to resize the label to fit the new text, or `False` to keep its current size (text that does not fit is cut off). |
