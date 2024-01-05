# 基本开发指南
 > 开发一个拥有基本功能的适配器

## 进行引用
 * 从 /lib/adapters/adapter.py 导出标准 Adapter 类: 
 ```python
 from lib.adapters.adapter import Adapter as Default
 ```

## 开发工作
 * 请阅读 [适配器类成员](./develop/adapter/member.md) 了解适配器类的属性和方法
 * 根据项目实际情况重新定义对应属性和方法(不再给出示例)
 * 在__init__方法中创建适配器实例，并以字典的形式传入自定义属性和方法

 ```python
def __init__(self) -> None:
    self.Adapter = Default({
        'name': str,
        'id': str,
        'version': str,
        '_recv_msg': self._recv_msg,
        '_send': self._send,
        'reply': self.reply,
        'isFriend': self.isFriend
    })
 ```

## 基本编写示例

 ```python
 from lib.adapters.adapter import Adapter as Default


 class Adapter:
    def __init__(self) -> None:
        self.Adapter = Default({
            'name': str,
            'id': str,
            'version': str,
            '_recv_msg': self._recv_msg,
            '_send': self._send,
            'reply': self.reply,
            'isFriend': self.isFriend
        })

    # 接收消息的方法
    async def _recv_msg(self) -> dict:
        # ...

    # 发送消息的方法
    async def _send(
        self,
        e
    ) -> bool:
        # ...

    # 快速回复的方法
    async def reply(
        self,
        e
    ) -> bool:
        # ...

    # 判断是否为好友
    def isFriend(
        self,
        user
    ) -> bool:
        # ...
    
    # 返回创建的适配器实例
    def load_on(self):
        return self.Adapter
 ```