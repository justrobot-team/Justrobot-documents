# 方法详细说明

## 与内核交互

### load
* 含义:
  加载时调用以初始化适配器实例
* 参数

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| bot | object | [机器人上下文实例](./develop/interface/botAttr.md) |
| cfg | dict | [配置信息](./develop/adapter/attribute.md#cfg) |

* 返回值 
  None

### load_on
* 含义:
  加载时调用获得适配器功能实例
* 参数
  None

* 返回值

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| client | object | [适配器功能实例](./develop/interface/clientAttr.md) |

### run
* 含义:
  内核调用来启动适配器运行
* 参数
  None
* 返回值
  None

### _deal
* 含义:
  用于适配器调用构建消息实例并触发消息处理流程
* 参数

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| _message | dict | 存有消息内容的字典 |

* 返回
  None
* _message 格式说明:

| 键 | 值 | 说明 |
| -- | -- | -- |
| seq | str | 消息序列号 |
| notice | str | 消息类型 |
| msg | str | 消息文本内容|
| file | byte/url | 文件内容/URL |
| user | str | 用户 id |
| time | str | 当前时间 |


## 消息处理

### _recv_msg
* 含义:
  接收消息的抽象逻辑
* 参数
  None
* 返回值

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| _message | dict | [存有消息内容的字典](#_deal) |

### _send
* 含义:
  发送消息的抽象逻辑
* 参数

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| e | object | 标准消息实例 |

* 返回值
  bool : 是否成功

## 插件交互

### reply
* 含义:
  发送消息的通用方法
* 参数

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| e | object | 标准消息实例 |

* 返回值
  bool : 是否成功

### get_user_list
* 含义:
  获取用户列表
* 参数
  None

* 返回值
  
| 名称 | 类型 | 含义 |
| -- | -- | -- |
| user_list | list | 用户列表 |

* 用户列表说明:
  格式为
  ```python
  [
    [ 适配器名称, 用户 id ],
    # ...
  ]
  ```

### get_group_list
* 含义:
  获取群聊列表
* 参数
  None

* 返回值
  
| 名称 | 类型 | 含义 |
| -- | -- | -- |
| group_list | list | 群聊列表 |

* 群聊列表说明:
  格式为
  ```python
  [
    [ 适配器名称, 群聊 id ],
    # ...
  ]
  ```

### get_channel_list
* 含义:
  获取子频道列表
* 参数
  None

* 返回值
  
| 名称 | 类型 | 含义 |
| -- | -- | -- |
| channel_list | list | 子频道列表 |

* 子频道列表说明:
  格式为
  ```python
  [
    [ 适配器名称, 服务器 id, 子频道 id ],
    # ...
  ]
  ```

### get_guild_list
* 含义:
  获取服务器列表
* 参数
  None

* 返回值
  
| 名称 | 类型 | 含义 |
| -- | -- | -- |
| guild_list | list | 服务器列表 |

* 服务器列表说明:
  格式为
  ```python
  [
    [ 适配器名称, 服务器 id ],
    # ...
  ]
  ```

## 更新数据

### upgrade_user_list
* 含义:
  更新用户列表
* 无参数和返回值

### upgrade_group_list
* 含义:
  更新群聊列表
* 无参数和返回值

### upgrade_channel_list
* 含义:
  更新子频道列表
* 无参数和返回值

### upgrade_guild_list
* 含义:
  更新服务器列表
* 无参数和返回值