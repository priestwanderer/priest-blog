---
title: Anaconda 命令
data: 2025-03-21 13:00:00
headimg: '/images/component/Anaconda/Anaconda.png'
---

>**miniconda**  专为简化Python环境管理而设计的轻量级发行版。允许用户创建隔离的Python环境，每个环境可以拥有独立的库和依赖，从而避免不同项目间的依赖冲突。
**conda** 包管理器和环境管理器

<!-- more -->
---

## 前置条件

### 安装编辑器 **Visual Studio Code**

{% link Visual Studio Code::https://code.visualstudio.com/::/images/component/Anaconda/code-stable.png %}

### 搜索 **Anaconda Prompt** 

![2.png](/images/component/Anaconda/3cb1823cbc6ef88461433e19c0f8e9f.png)

### 右键选择 **以管理员身份运行**

![3.png](/images/component/Anaconda/fcb69a43d2f01d1b2bc9762d8efe03b.png)

---

## **创建新环境**

### 输入命令
将命令中的 "pytorch" 更换成自定义的环境名称
```
conda create -n pytorch python=3.12
```

![4.png](/images/component/Anaconda/b388fad49269a856aaaf3d9ef7bd9a8.png)

### 按照提示，输入 'y'

![5.png](/images/component/Anaconda/287f9221dead00d5d7e74a0ae5d2d11.png)

>下载完成后，会有命令指引切换成新环境，但是这里还是先进行两步查询操作。

## **查看环境清单**
```
conda env list
```
![6.png](/images/component/Anaconda/7e6db801978d018fdb3be22104f4989.png)

>可以看到，环境清单里已经有我们创建的新环境了。

## **查看当前版本cuda**
```
nvidia-smi 
```
![7.png](/images/component/Anaconda/91bb79989c4fb0f9ec0cfc2ea06cfff.png)

>以我的电脑为例，可以看到这里cuda版本是 12.7 

## **切入conda激活**
查找完毕 ,回归主线 (记得将 pytorch 改为自己定义的环境名称)
```
conda activate pytorch
```
![8.png](/images/component/Anaconda/b7c92cdbce92757e06719aab5ec3a2d.png)
>可以看到，这里已经从本地裸环境切换成我们创建的新环境了(为了隔离环境，避免不同项目间的依赖冲突)

## **进pytorch官网配置信息**

### 搜索pytorch官网
![9.png](/images/component/Anaconda/1cb295fa8b59fc18015387dd53f860a.png)

### 配置信息
>这里我们已知电脑cuda版本是 12.7 , 我们需要选择一个比自己电脑小的版本。

![10.png](/images/component/Anaconda/af71f97a4956152fba72fc5100fd10b.png)

### 复制 run this command 内的内容

![11.png](/images/component/Anaconda/700f1681335065149d82c70f0fce12d.png)

### 回到我们的小黑窗口，粘贴到命令行

![12.png](/images/component/Anaconda/e3379af690e496ad166286f663b614f.png)

## **在编辑器切换成新创建的环境**
### 将要运行的 python 文件在编辑器 vscode 中打开

>请看右下方，点击它进行环境切换

![13.png](/images/component/Anaconda/cf17868073e4fa0d817593fe756b43f.png)

### 点击将环境切换成 新创建的环境

![15.png](/images/component/Anaconda/603d62bf736cb549f699b10140bb818.png)

>至此，新环境安装并切换完成，可以在这个新环境下运行你的代码啦！

---
## **退出虚拟环境**
回到本机环境
```
conda deactivate
```
![16.png](/images/component/Anaconda/d9fb8353aaa475fd7960103c2fcf96a.png)

## **删除虚拟环境**
命令中的 "pytorch" 是自定义的环境名称
```
conda env remove -n pytorch
```
![17.png](/images/component/Anaconda/20167c4df6a41703f3822309eb7746a.png)