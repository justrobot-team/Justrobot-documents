# 日志用法说明

## 方法:

| 名称 | 含义 |
| -- | -- |
| debug | 打印 debug 级别日志 |
| info | 打印 info 级别日志 |
| warn | 打印 warn 级别日志 |
| error | 打印 error 级别日志 |
| fatal | 打印 fatal 级别日志 |

## 用法
1. 单语注释:
```python
self.log.info(msg)
```
2. 双语或多语注释:
```python
self.log.info({
   'zh' : msg_zh,
   'en' : msg_en,
   # ...
})
```