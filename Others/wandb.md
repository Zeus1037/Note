## 介绍

Wandb（全称为Weights and Biases）是一个用于跟踪、可视化和协作机器学习项目的在线工具。它提供了许多功能，包括实时的指标跟踪、超参数调整、模型的可视化等。



## 使用教程：

1.   在[wandb官网](https://wandb.ai/home)注册账户
2.   在项目下安装wandb依赖:

```bash
pip install wandb
```

3.   在本地登录wandb账户并输入自己的API Key (在官网复制)

```bash
wandb login
```

4.   在自己的代码中调用wandb

     这里给出demo.py

```python
import wandb
import random

# start a new wandb run to track this script
wandb.init(
    # set the wandb project where this run will be logged
    project="my-awesome-project",
    
	# project下的run的name
    name="name",

    # track hyperparameters and run metadata
    config={
    	"learning_rate": 0.02,
    	"architecture": "CNN",
    	"dataset": "CIFAR-100",
    	"epochs": 10,
    }
)

# simulate training
epochs = 10
offset = random.random() / 5
for epoch in range(2, epochs):
    acc = 1 - 2 ** -epoch - random.random() / epoch - offset
    loss = 2 ** -epoch + random.random() / epoch + offset

    # log metrics to wandb
    wandb.log({"acc": acc, "loss": loss})
    # wandb.log({"train/acc": acc, "train/loss": loss})    # 存储在名为“train”的section下

# [optional] finish the wandb run, necessary in notebooks
wandb.finish()
```



## 问题解决：

#### 1. wandb数据不更新，显示crashed，但服务器进程仍在运行

**原因**：网络不稳定，导致服务器wandb挂起

**==解决方案==**：在服务器进程结束后，在进程工作目录下wandb文件夹，以及存储在本地对应该次进程的wandb文件（假设本地的wandb文件名为 run-20230105_104214-3fjeioj8），在终端运行以下命令即可同步到线上的wandb：

```bash
cd wandb
wandb sync run-20230105_104214-3fjeioj8
```

