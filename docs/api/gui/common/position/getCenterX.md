# getCenterX()

Return the object's horizontal center.

The object rotates about its center, so this is always the same as [getBoundingCenterX()](getBoundingCenterX.md).

If the object is a [Display](../../display/index.md), this returns the horizontal center of the display's canvas.

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getCenterX()
```

## Returns

`return x`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal center, in pixels. |
