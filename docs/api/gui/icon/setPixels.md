# setPixels()

Set the pixels of the image from a grid of colors.

The pixels are arranged as a list of rows, each row a list of pixels, each pixel a list of red, green, blue, and (optional) alpha values. The grid's top-left pixel goes at the image's top-left, [0][0].  The grid may be smaller than the image, in which case only that top-left part of the image changes.

## Parameters

Once an object `icon` has been created, you can use the following function:

```python
icon.setPixels(pixels)
```

| Parameter | Type | Default | Description |
|---|---|---|---|
| `pixels` | `list[list[list[int]]]` | _required_ | The new pixels, by row then column, each as [red, green, blue].<br>You may add a fourth alpha value as [red, green, blue, alpha].  If omitted, the pixel is fully opaque. |
