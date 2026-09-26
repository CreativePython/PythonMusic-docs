# getBoundingCenterX()

Return the horizontal center of the object's bounding box.

The object rotates about its center, so this is always the same as [getCenterX()](getCenterX.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingCenterX()
```

## Returns

`return x`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal center of the bounding box, in pixels. |
