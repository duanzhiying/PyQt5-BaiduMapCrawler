<img align="right" width="200" height="200" src="https://pic4.zhimg.com/v2-78d1472351272f41d8dd76a6d8a635c7_xll.jpg">

# 百度地图数据采集GUI工具
===========================================

[![image](https://img.shields.io/pypi/v/requests.svg)](https://pypi.org/project/requests/)
[![image](https://img.shields.io/pypi/l/requests.svg)](https://pypi.org/project/requests/)
![PyPI - Python Version](https://img.shields.io/pypi/pyversions/Django.svg)




## 功能和项目文档结构：
1.功能

* 根据关键词（街道、酒店或其他标志性建筑物等），查询指定区域周边的商户、酒店、交通位置等兴趣点信息  

* 将采集结果以表格形式在界面实时呈现

* 将采集结果导出为Excel文件  

2.项目结构
>
├── ChinaArea 全国省市数据  
│   ├── China_area.py  
│   └── __init__.py  
├── Crawler 采集程序  
│   ├── BaiduMapCrawler.py    
│   └── __init__.py  
├── main.py 主程序  
├── Mainwindow Ui界面文件  
│   ├── __init__.py  
│   └── Mainwindow.py  
├── qtpandas_1.0.4 修正后的qtpandas安装包   
├── README.md 项目文档说明  
├── requirements.txt 依赖库文件    
└── resource 资源文件  
    ├── image 界面加载图标以及程序运行截图  
    │   ├── run_main.gif   
    └── QSS  
        └── Mainwindow.qss  界面美化文件
>

## 准备工作

### 安装依赖库
* python 依赖库参考项目根目录 `requirements.txt`（可以直接使用pip install requirements.txt安装）

		numpy==1.13.3  
		openpyxl==2.4.9  
		pandas==0.20.3  
		PyQt5==5.9  
		python-dateutil==2.6.1  
		requests==2.18.4  
		sip==4.19.3  
		six==1.11.0  

### 安装依赖库过程中常见问题与解决方法

### 安装最新版本的qtpandas 

qtpandas在github上的最新版本代码有问题，需要修正  

请下载本项目下修正过的qtpandas代码安装

> 之前写这个小程序时给qtpandas提交了这个问题的issue,

> 2018年8月，收到qtpandas作者回复，已经修复这个bug.
可以直接在github上搜索qtpandas，然后 ```pip install .```安装，或者```python setup.py```
> 注意还是要下载到本地安装，不要直接使用`pip install qtpandas `安装。
> 
> 另外，也可以cd到本程序所在目录里的qtpandas_1.0.4中使用pip安装。
>对应目录：qtpandas_1.0.4


### 安装[PySide](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyside)

若在安装`pyside`过程中报错,手动下载相应python版本的[pyside](https://www.lfd.uci.edu/~gohlke/pythonlibs/#pyside)安装


	Complete output from command python setup.py egg_info:
	only these python versions are supported: [(2, 6), (2, 7), (3, 2), (3, 3), (3, 4)]


 
## 使用说明

1. 执行 python run.py，选择省、市，然后输入关键词，例：天津市 便利店

![Alt text](./resource/image/run_main.gif)  
 

2. 导出抓取结果为excel表格  


![Alt text](./resource/image/result_output.gif)  


3. 导出excel文件示例

![Alt text](./resource/image/result.png)  



## 联系我

你可以在这里找到我：[夜雨微寒的个人主页](https://xugongli.github.io/about/)

也可以在本界面的主窗口中,点击`关于我`，访问[我的主页](https://xugongli.github.io/about/)，或者给我留言。

![Alt text](./resource/image/about_me.gif)  


## License

[Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0.html).
