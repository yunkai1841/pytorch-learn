# Save and load models
PyTorchで学習したモデルはファイルに保存できる。

## Save
```python
torch.save(model.state_dict(), PATH)
```

## Load
```python
model = TheModelClass(*args, **kwargs)
model.load_state_dict(torch.load(PATH))
model.eval()
```
