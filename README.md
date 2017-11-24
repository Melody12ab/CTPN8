# 文本检测
基于CTPN实现:

    Z. Tian, W. Huang, T. He, P. He and Y. Qiao: Detecting Text in Natural Image with
    Connectionist Text Proposal Network, ECCV, 2016.

[在线示例](http://textdet.com)


# 兼容CUDA8.0版本
1 . 将caffe更新到最新版本，保留了官方库中没有的文件。

2 . 进行了一些小的修改，使其兼容最新版caffe

```{bash}
test on ubuntu16.04

git clone --recursive https://github.com/Melody12ab/CTPN8.git
...参见官方步骤进行编译安装caffe
# 回到根目录，编译cython代码
make
# 下载训练好的模型
wget http://textdet.com/downloads/ctpn_trained_model.caffemodel -P models/
# 运行测试代码
python ./tools/demo.py
```

# 硬件要求
首先需要GPU，至少6G内存，强烈推荐使用CUDNN。（如果对速度没要求，也可以在CPU上使用。）

# 软件要求
- Python2.7
- Cython
- ALL WHAT CAFFE Deponds ON.
- OpenCV3

# License
The codes are released under the MIT License.
