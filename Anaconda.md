# Anaconda

### 配置环境

1.jupyter在网页运行，运行时内核（黑窗口）不能关闭。

2.计算机用户名为英文才可以兼容jupyter。

![微信图片_20230424175509](C:\Users\lxc\Desktop\微信图片_20230424175509.jpg)

https://www.bilibili.com/video/BV1eN4y157vj/?spm_id_from=333.788.recommend_more_video.0&vd_source=bee013e22d10b6d2e417a16b33fbc3f5修改用户名

 [Python深度学习(1)：安装Anaconda与PyTorch库（GPU版本）.pdf](..\Python深度学习(1)：安装Anaconda与PyTorch库（GPU版本）.pdf) 

### 熟悉Jupyter环境

1.序号：运行的顺序，如’In[2]，表示第二个运行的语句‘。

2.删除：剪刀是表面删除，实际上仍存在，只是不显示。

​               Kernel（内核） —重启并清空所有输出，内核被清空了。

​               Kernel（内核） —重启并运行所有代码块，上述操作加上重新运行。

### 虚拟环境的基础命令

（1）Prompt 清屏 

`#清屏` 

`cls` 

（2）base 环境下的操作

列出所有的虚拟环境

conda env list

创建名为“环境名”的虚拟环境，并指定 Python 解释器的版本

conda create -n 环境名 python=3.9

删除名为“环境名”的虚拟环境

conda remove -n 环境名 --all

进入名为“环境名”的虚拟环境

`conda activate 环境名`

（3）虚拟环境内的操作 （pip 安装若失败，在【pip intsall 库==版本】后加【 -i https://pypi.tuna.tsinghua.edu.cn/simple 】即可） 

列出当前环境下的所有库 

`conda list`

 安装 NumPy 库，并指定版本 1.12.5 

pip install numpy==1.21.5 -i https://pypi.tuna.tsinghua.edu.cn/simple

 安装 Pandas 库，并指定版本 1.2.4

 `pip install Pandas==1.2.4 -i https://pypi.tuna.tsinghua.edu.cn/simple` 

 安装 Matplotlib 库，并指定版本 3.5.1

pip install Matplotlib==3.5.1 -i https://pypi.tuna.tsinghua.edu.cn/simple

 查看当前环境下某个库的版本（以 numpy 为例） 

`pip show numpy` 

运行虚拟环境

conda activate

退出虚拟环境 

`conda deactivate`

### 虚拟环境与 Jupyter 内核相连

请在 Prompt 的虚拟环境下操作下列命令

  列出 Jupyter 的内核列表 

jupyter kernelspec list 

安装 ipykernel 

pip install -i https://pypi.tuna.tsinghua.edu.cn/simple ipykernel 

 将虚拟环境导入 Jupyter 的 kernel 中 

python -m ipykernel install --user --name=环境名 

删除虚拟环境的 kernel 内核 

jupyter kernelspec remove 环境名                