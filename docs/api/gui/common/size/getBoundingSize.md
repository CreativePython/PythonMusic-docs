# getBoundingSize()

Return the width and height of the object's bounding box.

The bounding box is the smallest upright box that surrounds the object, so it grows as the object rotates.  For the object's own size before rotation, use [getSize()](getSize.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingSize()
```

## Returns

`return width, height`

| Value | Type | Description |
|---|---|---|
| width | `int or float` | The bounding box's width, in pixels. |
| height | `int or float` | The bounding box's height, in pixels. |
