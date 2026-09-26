# getY()

Return the object's vertical position.

This is where the object's top edge would be if it were not rotated, so it stays the same as the object rotates.  For the vertical position of the upright box around the rotated object, use [getBoundingY()](getBoundingY.md).

If the object is a [Display](../../display/index.md), this returns the display's vertical position on the screen.

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getY()
```

## Returns

`return y`

| Value | Type | Description |
|---|---|---|
| y | `int or float` | The vertical position of the top-left corner, in pixels. |
