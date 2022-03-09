FROM alpine

# ENTRYPOINT 入口（真正的门）
ENTRYPOINT [ "ping" ]

# CMD（进门的时候需要带的口令）
# CMD 可以被修改，但是 ENTRYPOINT 不可以被修改
# 最终的用法：CMD 是给 ENTRYPOINT 提供参数的
CMD baidu.com

# 启动命令
# ENTRYPOINT ping + CMD baidu.com = 错误

# CMD 和 ENTRYPOINT 作为唯一入口，写多个，只有最后一个生效
# CMD ping baidu.com
# CMD ping 123.sogou.com