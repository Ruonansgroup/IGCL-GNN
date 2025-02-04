# Information-based Gradient Enhanced Causal Learning Graph Neural Network for Out-of-Distribution Fault Diagnosis of Complex Industrial Processes

## 实验环境

请按照此要求设置环境。通常，您可能需要运行以下命令：

```shell
conda create -n IGCL_GNN python=3.9
conda activate IGCL_GNN
conda install pytorch cudatoolkit=11.6 -c pytorch
conda install opencv scikit-learn networkx pandas tqdm matplotlib seaborn
pip install torch==1.12.1
pip install torch-scatter==2.1.0 -f https://pytorch-geometric.com/whl/torch-1.12.1+cu116.html
pip install torch-sparse==0.6.16 -f https://pytorch-geometric.com/whl/torch-1.12.1+cu116.html
pip install torch-cluster==1.6.0 -f https://pytorch-geometric.com/whl/torch-1.12.1+cu116.html
pip install torch-spline-conv==1.2.1 -f https://pytorch-geometric.com/whl/torch-1.12.1+cu116.html
pip install torch-geometric==2.4.0
```

## 数据集下载

**三相流动设施数据：** 克兰菲尔德大学的三相流动设施（TFF）设计用于控制加压系统，并测量水流量、油流量和空气流量。该设施中共有24个传感器，用于测量系统不同关键位置的压力、流速、密度和温度。

**下载地址：**

[A Benchmark Case for Statistical Process Monitoring - Cranfield Multiphase Flow Facility - File Exchange - MATLAB Central (mathworks.com)](https://www.mathworks.com/matlabcentral/fileexchange/50938-a-benchmark-case-for-statistical-process-monitoring-cranfield-multiphase-flow-facility)

## 运行方式

对模型进行训练和测试，执行以下指令：

```shell
python main_real.py --model CausalGAT --dataset TFF --layers 3 --epochs 100 --folds 10 --lr 0.001 --n 0.5 --e 0.5 --train_model mgda 
```
