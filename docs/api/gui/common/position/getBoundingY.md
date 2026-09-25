# getBoundingY()

Return the vertical position of the object's bounding box.

The bounding box is the smallest upright box that surrounds the object, so it moves as the object rotates.  For the object's own vertical position before rotation, use [getY()](getY.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingY()
```

## Returns

`return y`

| Value | Type | Description |
|---|---|---|
| y | `int or float` | The vertical position of the bounding box's top-left corner, in pixels. |
