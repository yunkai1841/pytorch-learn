# Datasets and dataloaders

## Build in datasets
PyTorchの各モジュールにビルドインされたデータセットを利用することができる。
- [`torchvision.datasets`][imgdatasets]: 画像データセット
- [`torchtext.datasets`][textdatasets]: テキストデータセット
- [`torchaudio.datasets`][audiodatasets]: 音声データセット

```python
import torch
from torch.utils.data import Dataset
from torchvision import datasets
from torchvision.transforms import ToTensor
import matplotlib.pyplot as plt


training_data = datasets.FashionMNIST(
    root="data", # データを保存するディレクトリ
    train=True, # 訓練データ or テストデータ
    download=True, # データが存在しない場合にダウンロードするかどうか
    transform=ToTensor() # データをTensorに変換する
)

test_data = datasets.FashionMNIST(
    root="data",
    train=False,
    download=True,
    transform=ToTensor()
)
```



[imgdatasets]: https://pytorch.org/vision/stable/datasets.html
[textdatasets]: https://pytorch.org/text/stable/datasets.html
[audiodatasets]: https://pytorch.org/audio/stable/datasets.html