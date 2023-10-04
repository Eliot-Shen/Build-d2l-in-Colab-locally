# Build-d2l-in-Colab-locally
**本教程旨在协助读者在google drive本地安装d2l包,以便在colab中直接调用,无需每次在线下载.** \
笔者查阅了Google和Bing上为数不多的教程,要么语焉不详,要么去头去尾,要么代码出错,因而笔者抽空自写一份省时正确的教程,为后继者铺路. 
## Step 1
通过下面这个链接下载pytorch版的d2l包到本地 \
[d2l-pytorch-version](https://github.com/ShusenTang/Dive-into-DL-PyTorch) \
再从本地将整个文件夹上传至Google Drive  
## Step 2
点进文件夹,找到code子目录,再点进去找到d2lzh_pytorch子目录,其中有一个utils.py文件,将其改名为d2lzh_pytorch.py并复制移动到code目录下. \
如下图所示,但这里因为嫌名字过长,我将主文件夹名Dive-into-DL-PyTorch-master改为了d2l,请不要困惑.
![图示](https://github.com/Eliot-Shen/build-d2l-in-Colab-locally/blob/main/1.png)
## Step 3
接下来打开你要使用d2l包的ipynb文件,在开头插入下面的代码就可以本地运行d2l包了! \
弹出的申请挂用google drive的窗口都填'允许'即可 \
path那行代码的具体路径视个人而定,如果没有改过文件夹名就是下面的代码
"""
from google.colab import drive
drive.mount('/content/drive')
import os
path = "/content/drive/MyDrive/Dive-into-DL-PyTorch-master/code"
os.chdir(path)
!ls
import d2lzh_pytorch as d2l
"""
