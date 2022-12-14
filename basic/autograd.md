# Autograd
ニューラルネットワークを学習させるとき、逆伝播アルゴリズムでは、ネットワークのパラメータに対する損失関数の勾配を計算する。これは、ネットワークのパラメータを更新するために必要である。PyTorchでは、`autograd`パッケージがこの自動微分の計算を行う。`autograd`パッケージは、Tensorのすべての演算に対して勾配を自動的に計算する。このパッケージは、ネットワークの学習を定義するために、`Tensor`の演算を記録することで動作する。この記録を用いて、最終的な勾配を計算するために、`backward()`メソッドを呼び出すことができる。この`backward()`メソッドは、勾配を計算するために、`Tensor`の`grad_fn`属性を辿ることで動作する。`Tensor`がユーザーによって作成された場合、`grad_fn`は`None`である。

`Tensor`の勾配を計算するために、`requires_grad`属性を`True`に設定する。計算が終了した後に、`backward()`メソッドを呼び出すことで、勾配を自動的に計算することができる。この勾配は、`Tensor`の`grad`属性に蓄積される。勾配の蓄積を防ぐために、`Tensor`の`grad`属性を明示的にリセットする必要がある。`autograd`パッケージは、勾配の計算を記録するために、`forward`の計算グラフを構築する。このグラフは、Tensorの`grad_fn`属性を辿ることで、復元することができる。このグラフは、Tensorの`requires_grad`属性が`True`である場合にのみ、構築される。

## 勾配計算
`backward()`を実行すれば、勾配を自動計算できる。
