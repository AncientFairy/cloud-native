# ENV 的坑
FROM alpine
LABEL maintainer="许大仙"
ENV msg="hello"
ENV msg2=${msg}
RUN echo ${msg}
RUN echo ${msg2}
# 如果运行期修改了 msg=666，那么 msg 和 msg2 的值是 666 和 hello ,因为 ENV 在构建期就会被解析并持久化。
CMD ["/bin/sh","-c","echo $msg;echo $msg2;"]