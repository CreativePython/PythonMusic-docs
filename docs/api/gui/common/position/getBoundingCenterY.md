# getBoundingCenterY()

Return the vertical center of the object's bounding box.

The object rotates about its center, so this is always the same as [getCenterY()](getCenterY.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingCenterY()
```

## Returns

`return y`

| Value | Type | Description |
|---|---|---|
| y | `int or float` | The vertical center of the bounding box, in pixels. |
