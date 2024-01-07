# 常见问题收集
## 部分通性问题
* ModuleNotFoundError: No module named xxx
  没有配置依赖或者没有激活虚拟环境
* `WARNING: Retrying (Retry(total=x, connect=None, read=None, redirect=None, status=None)) after connection broken by 'SSLError(SSLZeroReturnError(6, 'TLS/SSL connection has been closed (EOF) (_ssl.c:1131)'))': xxxxxx/xxxx`
  把代理或梯子关了
* Could not fetch URL ...
  软件源 URL 无效
* TimeoutError: [Errno 110] Connection timed out
  连接超时，检查网络
* Could not find an index that is compatible with the requested artifact xxxxx
  索引失败，可能是没有网络连接

## Linux 特性问题
* `fatal error: <xxxx.h>: No such file or directory`
  头文件缺失，更新或安装 build-essential
* 未找到依赖包
  ```shell
    ERROR: Could not find a version that satisfies the requirement xxx (from versions: xxx)
    ERROR: No matching distribution found for xxx
  ```
  python 依赖包安装错误，尝试更换软件源，若换源后仍无效则可能为项目之间依赖冲突
* Package xxxxx not found
  缺少相关系统软件包，使用 Linux 软件包管理器安装即可
* Command 'gcc' failed with exit status 1
  编译失败，观察错误所在依赖包并自行根据搜索结果排查

## Windows 特性问题
* ModuleNotFoundError: No module named xxx
  没有配置依赖或者没有激活虚拟环境
* error: Microsoft Visual C++ xxxx is required
  缺少编译环境，从[Visual Studio](https://visualstudio.microsoft.com/zh-hans) 下载 Visual Studio 并安装编译环境
* `Command "C:\****\Microsoft Visual Studio\****\cl.exe" failed with exit status 2`
  可能是编译器有问题，重新配置编译环境等
* `fatal error: <xxxx.h>: No such file or directory`
  缺少头文件，编译环境没装完整，打开 Visual Studio 安装工具选择相关软件包
  勾选上 C++ (v143)通用 Windows 平台工具、Windows 11 SDK

## MacOS 特性问题
  > 别看我，我没相关经验，建议去问万能的搜索工具

## Termux 特性问题
  * 同 [Linux](#Linux)