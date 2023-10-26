# MMCV docker 使用过程
黄区桌面连 370-x4 服务器
```
ssh duzekun@10.100.146.29
```

从 370-X4 服务器连 mmcv docker
```
docker stop dzk_mmcv
docker rm dzk_mmcv
sh /projs/platform/duzekun/mmcv_dzk/docker/mmcv_docker.sh
```

进入 mmcv 文件夹
```
cd /projs/platform/duzekun/mmcv_dzk/mmcv/
source /torch/venv3/pytorch/bin/activate
```

编译前准备
```
rm -rf build
rm -rf mmcv_*
pip uninstall mmcv-full
```

编译
```
python setup.py install > temp_build_log 2>&1
```

检查编译是否错误
```
grep 'error:' temp_build_log 
```

测试前
```
pip uninstall attrs && pip install attrs==19.1.0
```

测试代码

```
pytest tests/test_ops/test_spconv.py
pytest tests/test_ops/test_focal_loss.py

python tests/test_ops/test_spconv.py

```