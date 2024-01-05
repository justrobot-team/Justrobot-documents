# 机器人上下文实例

## 属性

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| uin | dict | 存有全部适配器的 id-特征属性 |
| client | dict | 存有全部适配器的 名称-功能实例 |
| log | object | 存有日志实例 |
| loop | task | 全部的异步任务 |
| adapter_name_list | list | 全部适配器的名称列表 |
| translator_name_list | list | 全部转译器的名称列表 |
| plugin_name_list | list | 全部插件的名称列表 |
| lang | str | 机器人日志等语言 |
| msg_recv | int | 消息接收计数 |
| msg_send | int | 消息发送计数 |

## 方法

| 名称 | 含义 |
| -- | -- |
| msg_recv_append | 消息接收计数递增 |
| msg_send_append | 消息发送计数递增 |
| isMaster | 判断是否为主人 |
| get_user_list | 获取全局用户列表 |
| get_group_list | 获取全局群聊列表 |
| get_channel_list | 获取全局子频道列表 |
| get_guild_list | 获取全局服务器列表 |
| pickUser | 获取用户实例 |
| pickGroup | 获取群聊实例 |
| pickChannel | 获取子频道实例 |
| pickGuild | 获取服务器实例 |
| set_user_list | 更新全局用户列表 |
| set_group_list | 更新全局群聊列表 |
| set_channel_list | 更新全局子频道列表 |
| set_guild_list | 更新全局服务区列表 |
| update_user_list | 同步全局用户列表 |
| update_group_list | 同步全局群聊列表 |
| update_channel_list | 同步全局子频道列表 |
| update_guild_list | 同步全局服务器列表 |