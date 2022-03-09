FROM alpine
# 挂载 容器指定的文件夹，如果不存在，会自动创建。
# 指定了 VOLUME 指令后，即使启动容器的时候没有指定 -v 参数，也会自动进行匿名卷挂载。
VOLUME [ "/demo","/app" ]
CMD ping www.baidu.com