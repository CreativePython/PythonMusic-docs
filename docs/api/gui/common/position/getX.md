# getX()

Return the object's horizontal position.

This is where the object's left edge would be if it were not rotated, so it stays the same as the object rotates.  For the horizontal position of the upright box around the rotated object, use [getBoundingX()](getBoundingX.md).

If the object is a [Display](../../display/index.md), this returns the display's horizontal position on the screen.

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getX()
```

## Returns

`return x`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal position of the top-left corner, in pixels. |
