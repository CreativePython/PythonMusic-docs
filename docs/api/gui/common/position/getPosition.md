# getPosition()

Return the object's position, the top-left corner of its box before rotation.

The object rotates about its center, so this is where its top-left corner would be if it were not rotated.  For the upright box around the rotated object, use [getBoundingPosition()](getBoundingPosition.md).

If the object is a [Display](../../display/index.md), this returns the display's position on the screen.

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getPosition()
```

## Returns

`return x, y`

| Value | Type | Description |
|---|---|---|
| x | `int or float` | The horizontal position of the top-left corner, in pixels. |
| y | `int or float` | The vertical position of the top-left corner, in pixels. |
