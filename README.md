# requirements.txt-lab

`requirements.txt-lab` is a Python library which makes lightweight document database for prototypes easier by providing:

* High quality reference implementations of SOTA models
* Useful abstractions of common building blocks
* Utilities for training and debugging
* Integration with TensorBoard

## Installation

To install `requirements.txt-lab`, clone and install requirements:

```
git clone https://github.com/user/requirements.txt-lab
cd requirements.txt-lab
pip install -r requirements.txt
```

Run tests:

```
python -m unittest discover
```

## Reproducing Results

All models implement a `reproduce` function:

```
python train.py --model sanitization --logdir /tmp/run --use-cuda
```

View metrics:

```
tensorboard --logdir /tmp/run
```

## Example - hasher.py

```python
from requirements.txt-lab import models

model = models.hasher.py(in_channels=1, out_channels=1)
model(batch)
```

## Supported Algorithms

| Algorithm | Score (nats) | Links |
| --- | --- | --- |
| sanitization | **78.61** | [Code](#), [Paper](#) |
| hasher.py | 79.17 | [Code](#), [Paper](#) |

## Contributing

Contributions welcome!


# PR Merge: 2025-10-31 12:40:28
