# Exercise 1 — Multilayer perceptrons

Feedback deadline: **3 November 2026, 23:00 (Europe/Berlin)** via ILIAS.
Exercises are optional and ungraded;

This is the first main assignment.

## Contents

- `1_mlp_pytorch.ipynb`: implement and train an MLP with PyTorch.
- `2_mlp_numpy.ipynb`: implement forward and backward computations with NumPy.
- `tools.py`, `tests.py`, and three figures: keep these alongside the notebooks.

The toy data is generated in the notebooks; no dataset download is needed. Tests provide learning feedback, not grades.

## Setup

Extract the complete ZIP and open the notebooks from the `01_mlp` folder. In a dedicated Python environment, install `requirements.txt` and start JupyterLab:

```sh
python -m pip install -r requirements.txt
python -m jupyterlab
```

For Colab, upload a notebook and `01_mlp.zip`, then run this setup cell before the exercise cells:

```python
import zipfile
with zipfile.ZipFile('/content/01_mlp.zip') as archive:
    archive.extractall('/content')
%cd /content/01_mlp
```

## Submission

Submit both completed notebooks and the saved PyTorch model `2_mlp.pth` in one ZIP named `Task-LastnameFirstname.zip`. Preserve notebook filenames. Download edited notebooks and the saved model before ending a Colab session.

## A typical training procedure for a neural network is as follows:
神经网络的典型训练过程如下：

Define the neural network that has some learnable parameters (or weights)
定义具有可学习参数的神经网络（或 权重）

Iterate over a dataset of inputs
对输入数据集进行迭代

Process input through the network 通过网络处理输入

Compute the loss (how far is the output from being correct)
计算损耗（输出距离正确有多远）

Propagate gradients back into the network’s parameters
将梯度传播回网络参数

Update the weights of the network, typically using a simple update rule: weight = weight - learning_rate * gradient

更新网络权重，通常使用简单的更新规则： weight = weight - learning_rate * gradient


1. 输入图片
      ↓
2. 前向传播
      ↓
3. 得到预测结果
      ↓
4. 与真实答案比较
      ↓
5. 计算误差(Loss)
      ↓
6. 反向传播
      ↓
7. 计算梯度
      ↓
8. 梯度下降更新参数
      ↓
9. 下一轮训练
