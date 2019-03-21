# easy-receptive-fields-pytorch
Minimal API for receptive field calculation in PyTorch


# Requirements
- PyTorch >= 0.4
- Python 3
- MatPlotLib (optional)

# Example
```
>>> import torch.nn as nn
>>> from receptivefield import receptivefield

>>> net = nn.Sequential(
  nn.Conv2d(in_channels=3, out_channels=32, stride=2, kernel_size=3),
  nn.ReLU(),
  nn.Conv2d(in_channels=32, out_channels=10, kernel_size=3),
)

>>> print(receptivefield(net, (1, 3, 32, 48)))

ReceptiveField(
  offset=Vector(x=0, y=0),
  stride=Vector(x=2, y=2),
  rfsize=Size(w=7, h=7),
  outputsize=Size(w=21, h=13),
  inputsize=Size(w=48, h=32)
)
```

# Screenshot

![Screenshot](/screenshot.png?raw=true)

# Author

[João F. Henriques](http://www.robots.ox.ac.uk/~joao/)

