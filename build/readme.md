# 快速开始

## 配置环境
> 推荐使用 Linux 环境运行本项目
* 安装 [Git](https://git-scm.com/downloads) , [python3.^6](https://www.python.org/) 或 [anconda](https://www.anaconda.com/download) 等可以创建 python 虚拟环境的工具

* Anconda 配置环境: 安装完成后打开终端运行
  ```shell
  conda create --name justrobot python=3.8
  conda activate justrobot
  ```

## 下载相关项目
* 从[项目地址](https://github.com/justrobot-team/justrobot)克隆本项目
  `git clone https://github.com/justrobot-team/justrobot.git`
* 从[适配器地址](https://github.com/justrobot-team/justrobot-adapter)选择适配器安装
* (可选)从[转译器地址](https://github.com/justrobot-team/justrobot-translator)选择转译器安装
* 从[插件地址](https://github.com/justrobot-team/justrobot-plugin)选择插件安装
> 若有疑问可以参考 [详细安装指南](./build/install.md)

## 运行项目

1. 根据你的系统操作风格
   * cd 到项目文件夹
   * 打开项目文件夹，并在该目录下打开终端

2. 根据你使用的是 python 还是 conda
  * python
    ```shell
    python bot.py
    ```
  * conda
    ```shell
    conda activate justrobot
    python bot.py
    ```