# getBoundingCenter()

Return the center point of the object's bounding box.

The object rotates about its center, so this is always the same as [getCenter()](getCenter.md).

**NOTE:** This function isn't available to [Displays](../../display/index.md).

## Parameters

Once an object `item` has been created, you can use the following function:

```python
item.getBoundingCenter()
```

## Returns

`return centerX, centerY`

| Value | Type | Description |
|---|---|---|
| centerX | `int or float` | The horizontal position of the bounding box's center, in pixels. |
| centerY | `int or float` | The vertical position of the bounding box's center, in pixels. |
