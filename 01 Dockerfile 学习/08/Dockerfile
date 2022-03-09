FROM alpine
LABEL maintainer="许大仙"
# 创建用户和组
RUN addgroup -S test && adduser -S test -G test -h /home/test
# USER 只是帮准我们切换到指定的用户而已，这个用户必须事先建立好的，否则无法切换。USER 则是改变之后层的执行 RUN、CMD、以及 ENTRYPOINT 这类命令的身份。
USER test:test
# 通过 COPY 指定的 chown 功能改变复制文件的权限
COPY --chown=test:test *.txt /test/
# 注意：一旦声明了 USER 之后，USER 后面的 RUN、CMD、ENTRYPOINT 的身份就是 test ，而 a.txt 是主机生成的，身份是 root ，但是，因为使用了 COPY --chown=test:test ，所以文件的权限是 test
RUN cd /test && ls -l && echo 1111 > a.txt 