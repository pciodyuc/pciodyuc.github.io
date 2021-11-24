##### Create environment and activate

```
conda create --name siamban python=3.7
source activate siamban
```

##### Install numpy/pytorch/opencv

```shell
conda install numpy
conda install pytorch=1.3.1 torchvision cudatoolkit=10.1 -c pytorch
# 或者 (pip3 这个好用)
pip3 install torch torchvision torchaudio
pip install opencv-python
pip install ipython
pip install parameter-sherpa

```

##### 查看torch是不是可用

```python
import torch 
print(torch.__version__)
print(torch.version.cuda)
print(torch.cuda.is_available())
```



##### Install other requirements

```python
pip install pyyaml yacs tqdm colorama matplotlib cython tensorboard future mpi4py optuna
# mpi4py的安装依赖于apt-get install libopenmpi-dev
```

##### Build extensions

```
python setup.py build_ext --inplace
```

##### 移除环境

```
conda remove -n your_env_name(虚拟环境名称) --all
```

