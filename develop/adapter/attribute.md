# 适配器类的属性详细介绍
## cfg
* 类型: dict
* 含义: 配置信息
* 键值对格式:
 ```python
 {
    适配器名称(str): 适配器配置信息(dict),
    # ...
 }
 ```
* 适配器配置信息格式:

| 键 | 值 | 含义 |
| -- | -- | -- |
| use_tree | bool | 是否启用关系树 |
| enable_translator | list | 关系树中启用的转译器 |
| enable_direct_plugin | list | 关系树中启用的直通插件 |
| enable_plugin | list | 关系树中启用的插件 |

* 若有自定义配置需求优先在适配器项目内添加自定义配置文件

## bot
* 类型: object
* 含义: 机器人上下文实例
* [全部属性](../interface/botAttr.md#属性)
* [全部方法](../interface/botAttr.md#方法)

## log
* 类型：object
* 含义: 打印日志信息
* [用法说明和示例](../interface/logFunc.md#日志用法说明)

## basemessage
* 类型: object
* 含义: 通用消息实例
* [全部属性](../message/basemessage.md#属性)
* [全部方法](../message/basemessage.md#方法)

## client
* 类型: object
* 含义: 适配器功能实例
* [全部属性](../interface/clientAttr.md#属性)
* [全部方法](../interface/clientAttr.md#方法)