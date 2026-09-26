# getSize()

Return the object's width and height.

These are the object's own size before rotation, so they stay the same as it rotates.  For the size of the upright box around the rotated object, use [getBoundingSize()](getBoundingSize.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getSize()
```

## Returns

`return width, height`

| Value | Type | Description |
|---|---|---|
| width | `int or float` | The width, in pixels. |
| height | `int or float` | The height, in pixels. |
