FROM alpine
RUN mkdir /demo && mkdir /app
RUN echo 111 > /demo/a.txt
RUN echo 222 > /app/b.txt
# 挂载 容器指定的文件夹，如果不存在，会自动创建。
# 指定了 VOLUME 指令后，即使启动容器的时候没有指定 -v 参数，也会自动进行匿名卷挂载。容器内的 /demo 和 /app ，需要在启动容器的时候，需要使用 -v 参数进行挂载。
# VOLUME 挂载出去的东西，容器改变也不会最终在 docker commit 的时候生效。
# -v 和 VOLUME 挂载出去的目录，主机变，容器里面也会发生变化，但是 
# ① docker commit 提交当前容器的所有变化为镜像，就会丢弃。
# ② VOLUME [ "/demo","/app" ] 容器会自动挂载，在之后对这些目录所操作的变化，也会丢弃
# ③ 挂载仅仅是为了将外边的数据同步到容器里面
# VOLUME 的最佳实践是写在 CMD 或 ENTRYPOINT 前面
VOLUME [ "/demo","/app" ]
# 下面的 2 个 RUN 指令没有生效，因为 VOLUME 指定的挂载目录是固化配置，当执行到 VOLUME 的时候就已经写入到容器中了，即使后面容器怎么变，也不会改变。
RUN echo 333 > /demo/a.txt
RUN echo 444 > /app/b.txt
CMD ping www.baidu.com


