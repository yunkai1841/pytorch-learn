# Build the neural network
ニューラルネットワークを構築するには、`torch.nn` パッケージを使用する。`nn` は、ニューラルネットワークを構築するための便利なツールを提供する。

## レイヤー

- `nn.Flatten` レイヤーは、入力を平坦化する。これは、`nn.Linear` レイヤーに入力するために必要。
- `nn.Linear` レイヤーは、線形変換を行う。`nn.Linear(in_features, out_features)` という形式で、`in_features` は入力の特徴量の数、`out_features` は出力の特徴量の数を表す。
- `nn.ReLU` レイヤーは、活性化関数として使用される。`nn.ReLU()` という形式で、引数はない。
- `nn.Sequential` レイヤーは、複数のレイヤーを順番に実行するために使用される。`nn.Sequential(*layers)` という形式で、`layers` はレイヤーのリスト。
- `nn.Softmax` レイヤーは、出力を確率に変換する。`nn.Softmax(dim)` という形式で、`dim` は確率を計算する次元を表す。