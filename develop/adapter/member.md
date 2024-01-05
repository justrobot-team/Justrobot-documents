# 适配器类的全部成员

## 属性

| 名称 | 类型 |含义 |
| -- | -- | -- |
| name | str | 适配器名称 |
| id | str | 平台 id |
| version | str | 适配器版本 |
| [cfg](./develop/adapter/attribute.md#cfg)  | dict | 配置信息 |
| [bot](./develop/adapter/attribute.md#bot) | object | 机器人上下文实例 |
| [log](./develop/adapter/attribute.md#log) | object | 日志实例 |
| [basemessage](./develop/adapter/attribute.md#basemessage) | object | 通用消息实例 |
| [client](./develop/adapter/attribute.md#client) | object | 适配器的功能实例 |

## 方法

| 名称 | 作用 |
| -- | -- |
| [pickUser](./develop/adapter/Pick.md#pickuser) | 获取成员实例 |
| [pickGroup](./develop/adapter/Pick.md#pickgroup) | 获取群聊实例 |
| [pickChannel](./develop/adapter/Pick.md#pickchannel) | 获取子频道实例 |
| [pickGuild](./develop/adapter/Pick.md#pickguild) | 获取服务器实例 |
| [isFriend]() | 判断用户是否为好友 |
| [load](./develop/adapter/func.md#load) | 用于适配器的加载 |
| [load_on](./develop/adapter/func.md#load_on) | 继承写法下用于返回实例本身的引用 |
| [_recv_msg](./develop/adapter/func.md#_recv_msg) | 接收消息的抽象逻辑 |
| [_send](./develop/adapter/func.md#_send) | 发送消息的抽象逻辑 |
| [_deal](./develop/adapter/func.md#_deal) | 创建消息实例并调用后端处理 |
| [reply](./develop/adapter/func.md#reply) | 根据传入的消息实例进行快速回复 |
| [run](./develop/adapter/func.md#run) | 适配器消息处理逻辑 |
| [get_user_list](./develop/adapter/func.md#get_user_list) | 获取用户列表 |
| [get_group_list](./develop/adapter/func.md#get_group_list) | 获取群聊列表 |
| [get_channel_list](./develop/adapter/func.md#get_channel_list) | 获取子频道列表 |
| [get_guild_list](./develop/adapter/func.md#get_guild_list) | 获取服务器列表 |
| [upgrade_user_list](./develop/adapter/func.md#upgrade_user_list) | 更新用户列表 |
| [upgrade_group_list](./develop/adapter/func.md#upgrade_group_list) | 更新群聊列表 |
| [upgrade_channel_list](./develop/adapter/func.md#upgrade_channel_list) | 更新子频道列表 |
| [upgrade_guild_list](./develop/adapter/func.md#upgrade_guild_list) | 更新服务器列表 |