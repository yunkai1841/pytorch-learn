# インストール方法

[インストール方法（公式）](https://pytorch.org/get-started/locally/)

## Requirements

- Anaconda3

Anacondaで新しい仮想環境を作っておきます。

```bash
conda create -n ptc python=3.9
conda activate ptc
```

## GPUあり

```bash
conda install pytorch torchvision torchaudio pytorch-cuda=11.7 -c pytorch -c nvidia
```

## CPUのみ

```bash
conda install pytorch torchvision torchaudio cpuonly -c pytorch
```
