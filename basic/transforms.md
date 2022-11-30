# Data transforms

## ToTensor
PIL ImageやNumPyのndarrayをTensorに変換する。

```python
import torch
from torchvision import datasets
from torchvision.transforms import ToTensor

training_data = datasets.FashionMNIST(
    root="data",
    train=True,
    download=True,
    transform=ToTensor()
)
```

## Lambda transform
ラムダ式を使って独自の変換を定義する。

```python
import torch
from torchvision import datasets
from torchvision.transforms import Lambda

to_tensor = Lambda(lambda x: torch.tensor(x))

training_data = datasets.FashionMNIST(
    root="data",
    train=True,
    download=True,
    transform=to_tensor
)
```
