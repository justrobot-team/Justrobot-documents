# 适配器功能实例

## 属性

| 名称 | 类型 | 含义 |
| -- | -- | -- |
| adapter_name | str | 适配器名称 |
| adapter_version | str | 适配器版本 |
| adapter_id | str | 平台 id |
| msg_recv  | int | 消息接收计数 |
| msg_send | int | 消息发送计数 |

## 方法

| 名称 | 含义 |
| -- | -- |
| pickUser | 获取用户实例 |
| pickGroup | 获取群聊实例 |
| pickChannel | 获取子频道实例 |
| pickGuild | 获取服务器实例 |
| msg_recv_append | 消息接收计数递增 |
| msg_send_append | 消息发送计数递增 |
| get_user_list | 获取用户列表 |
| get_group_list | 获取群聊列表 |
| get_channel_list | 获取子频道列表 |
| get_guild_list | 获取服务器列表 |
| update_user_list | 更新用户列表 |
| update_group_list | 更新群聊列表 |
| update_channel_list | 更新子频道列表 |
| update_guild_list | 更新服务器列表 |