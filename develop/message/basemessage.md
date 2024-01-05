# 通用消息实例

## 属性

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| adapter | str | 消息所属适配器 |
| translator | str | 消息所属转译器 |
| seq | str | 消息序列号 |
| notice | str | 消息类型 |
| msg | str | 消息文本内容 |
| file | byte | 消息文件内容 |
| user | object | 消息所属用户实例 |
| group | object | 消息所属群聊实例 |
| channel | object | 消息所属子频道实例 |
| guild | object | 消息所属服务器实例 |
| isBot | bool | 消息所属用户是否为机器人 |
| isFriend | bool | 与机器人是否为好友关系 |
| isPrivate | bool | 是否为私信环境 |
| isGroup | bool | 是否为群聊环境 |
| isGuild | bool | 是否为服务器环境 |
| isMaster | bool | 用户是否为机器人主人 |

## 方法

| 名称 | 含义 |
| -- | -- |
| load | 加载消息实例 |
| reply | 快速回复消息 |