# display-ruler
Display test image useful for checking size, alignment and color order.

## Small rectangular displays
```python
import displayio

# Initialize the display in the display variable
ruler = displayio.OnDiskBitmap("/display-ruler.bmp")

t = displayio.TileGrid(ruler, pixel_shader=ruler.pixel_shader)

g = displayio.Group()
g.append(t)

display.show(g)

display.refresh()

while True:
    pass
```

## Large rectangular displays
```python
import displayio

# Initialize the display in the display variable
ruler = displayio.OnDiskBitmap("/display-ruler-720p.bmp")

t = displayio.TileGrid(ruler, pixel_shader=ruler.pixel_shader)

g = displayio.Group()
g.append(t)

display.show(g)

display.refresh()

while True:
    pass
```

## Round displays

```python
import displayio

# Initialize the display in the display variable
ruler = displayio.OnDiskBitmap("/round-display-ruler-720p.bmp")

t = displayio.TileGrid(ruler, pixel_shader=ruler.pixel_shader)
# Center the image
t.x -= (ruler.width - display.width) // 2
t.y -= (ruler.height - display.height) // 2

g = displayio.Group()
g.append(t)

display.show(g)

display.refresh()

while True:
    pass
```