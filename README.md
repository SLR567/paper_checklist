# slurm集群食用指南

## 澳门大学IOTSC超算集群

### 登录集群
```bash
ssh yc37974@10.113.182.11
```
### 使用 jupyter notebook
```
#一个窗口（已登录）
jupyter notebook --no-browser --port=8890
#另一个窗口（未登录）
ssh -N -f -L localhost:8888:localhost:8890 yc37974@10.113.182.11
```

### 在vscode命令行使用（交互式运行任务）
```
srun -p h800_batch -N 1 -n 1 --gres=gpu:1 --cpus-per-task=1 --nodelist=dgx-h800-01 --pty /bin/bash
```
