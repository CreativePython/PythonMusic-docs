# setText()

Select the item with the given text.

This works just like the user picking the item: it becomes the selected item and the list's function is called with it.  To find out which item is selected, use [getText()](getText.md).

## Parameters

Once an object `dropdown` has been created, you can use the following function:

```python
dropdown.setText(text)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `text` | `str` | _required_ | The item to select. It must be one of the list's items. |
