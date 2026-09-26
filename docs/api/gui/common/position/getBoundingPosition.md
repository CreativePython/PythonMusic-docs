# getBoundingPosition()

Return the top-left corner of the object's bounding box.

The bounding box is the smallest upright box that surrounds the object, so it moves as the object rotates.  For the object's own position before rotation, use [getPosition()](getPosition.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingPosition()
```

## Returns

`return x, y`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal position of the bounding box's top-left corner, in pixels. |
| y | `int or float` | The vertical position of the bounding box's top-left corner, in pixels. |
