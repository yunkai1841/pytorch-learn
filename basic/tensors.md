# Tensors
PyTorchではTensorを使ってデータを表現する。Tensorは多次元配列で、PyTorchのTensorはNumPyのndarrayと似ていますが、GPU上で動作させることができるという点が異なる。Tensorは、PyTorchのTensorクラスのインスタンス。

```python
data = [[1, 2],[3, 4]]
x_data = torch.tensor(data)

np_array = np.array(data)
x_np = torch.from_numpy(np_array)
```

`ones`や`zeros`などのメソッドを使って、特定の値で初期化されたTensorを作ることもできる。

```python
shape = (2,3,)
rand_tensor = torch.rand(shape)
ones_tensor = torch.ones(shape)
zeros_tensor = torch.zeros(shape)
```

操作方法はNumPyとほぼ同じである。
```python
tensor @ tensor.T # 積
tensor * tensor # 内積
```

また、NumPyに変換して操作することもできる。
```python
tensor.numpy() # Bridge to NumPy
torch.from_numpy(np_array) # Bridge to PyTorch
```

## 属性
- `shape`: Tensorの形状を表すタプル
- `dtype`: Tensorのデータ型
- `device`: Tensorがどのデバイスにあるかを表す文字列