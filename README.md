# Frequency learning  
This library allows to work with images in frequency domain and after that return to the spatial domain.

Available conversions in the frequency spectrum:
- LinearFourier2d
- GeneralFourier2d

## Usage
Example:
```
import torch
import torch.nn as nn

from freqlearning import LinearFourier2d
from freqlearning import GeneralFourier2d


input_image = torch.randn(1, 256, 256) # input shape (1, 256, 256)

model = MyModel()
#gafl_layer = LinearFourier2d((1, 256, 256))
gafl_layer = GeneralFourier2d((1, 256, 256))

gafl_model = nn.Sequential(
    gafl_layer,
    model
)
```

### PyPI version:

$ pip install freqlearning

Latest version from source:

$ pip install git+https://github.com/YaroslavBespalov/freqlearning/freqlearning

### Requirements
Installing requirements by pip:
```
pip3 install --upgrade -r ./requirements.txt
```

### Contributors
- Yaroslav Bespalov & Viktor Shipitsin.
