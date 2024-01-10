# Dynex 开发工具本地测试
Dynex 是世界上第一个基于 DynexSolve 芯片算法的神经形态超级计算区块链，这是一种解决现实世界问题的有用工作量证明 (PoUW) 方法。 Dynex SDK用于在Dynex平台上进行交互和计算。 使用此存储库在 Dynex SDK 中启用“mainnet=False”功能。 它允许在 Dynex 神经形态计算云上进行计算之前在本地计算机上对 Qubo/Ising 计算问题进行采样。 主要用于在产生成本之前进行原型设计和代码测试。

# 从源代码构建并安装

使用以下命令构建二进制文件并将其复制到 Python 程序所在目录中的文件夹“``/testnet``”中：

```
git clone https://github.com/DynexCN/dynexsdk_testnet.git
./build.sh
cp dynex-testnet-bnb <PATH-OF-YOUR-SDK-PROGRAM>/testnet
```

# 使用

要在本地机器上启用采样，请指定参数“mainnet=False”：

```
model = dynex.BQM(bqm, logging=True);
sampler = dynex.DynexSampler(model,  mainnet=False);
sampleset = sampler.sample(num_reads=20000, annealing_time = 200, debugging=True);
```

