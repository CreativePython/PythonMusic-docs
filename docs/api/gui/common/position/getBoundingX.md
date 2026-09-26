# getBoundingX()

Return the horizontal position of the object's bounding box.

The bounding box is the smallest upright box that surrounds the object, so it moves as the object rotates.  For the object's own horizontal position before rotation, use [getX()](getX.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingX()
```

## Returns

`return x`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal position of the bounding box's top-left corner, in pixels. |
