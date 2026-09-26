# getBoundingHeight()

Return the height of the object's bounding box.

The bounding box is the smallest upright box that surrounds the object, so it grows as the object rotates.  For the object's own height before rotation, use [getHeight()](getHeight.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingHeight()
```

## Returns

`return height`

| Value | Type | Description |
|---|---|---|
| height | `int or float` | The bounding box's height, in pixels. |
