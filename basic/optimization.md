# Optimizing model parameters

モデルの学習では、勾配降下法を用いてパラメータを最適化する。

## Hyperparameters
- Number of epochs: 1 epoch = トレーニングデータを1周する
- Batch size: 一度に学習するデータ数
- learning rate: 一度にパラメータを更新する量

## 各epochの学習の流れ
1. トレーニング
   - パラメータを更新し、収束させようとする。
2. 検証・テスト
   - テストデータを用いて、モデルの性能を評価する。

### 損失関数
- モデルの性能を評価する関数
- 正解ラベルと予測ラベルの差を計算する
- これを最小化したい
- 例
  - `nn.MSELoss()`: 平均二乗誤差
  - `nn.NLLLoss()`: 負の対数尤度
  - `nn.CrossEntropyLoss()`: クロスエントロピー

### 最適化アルゴリズム
- パラメータを更新するアルゴリズム
- 例
  - [`torch.optim`](https://pytorch.org/docs/stable/optim.html)`.SGD()`: 確率的勾配降下法

```python
optimizer = torch.optim.SGD(model.parameters(), lr=1e-3, momentum=0.9)
```