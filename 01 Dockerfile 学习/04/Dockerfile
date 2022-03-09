FROM alpine
LABEL maintainer="许大仙"
# 如果是远程文件，自动下载
# 如果是压缩文件，自动解压
# 注意：ADD 并没有自动下载远程压缩文件并解压的功能
# 将当前内容复制到 alpine 中
ADD https://download.redis.io/releases/redis-6.2.6.tar.gz /dest
# 注意，RUN 指令上下并没有上下文的关系。
RUN ls -l