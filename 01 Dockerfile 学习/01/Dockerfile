# 选择基础镜像
FROM alpine
# 维护者信息
LABEL maintainer="许大仙"
# ARG 指令定义了一个变量，用户可以在构建的时候使用 `--build-arg name=value` 传递，docker build 命令会将其传递给构建器。
# `--build-arg` 指定参数会覆盖 Dockerfile 中指定的同名参数。
# 如果用户指定了 `未在 Dockerfile 中定义的构建参数` ，则构建会输出 `警告` 。
# ARG 只在构建时期有效，运行时期无效。
# 不建议使用构建时变量来传递注入 github 密码、用户凭据等机密，因为构建时变量的值可以通过 docker history 来观察到。
# ARG 变量定义从 Dockerfile 定义的行开始生效。
ARG param="Hi Docker"

# 在构建时期会运行的指令（根据 Dockerfile 创建一个镜像的整个过程时期）
RUN echo 1111
RUN echo ${param}

# 在运行时候会运行的指令（根据之前创建的镜像启动一个容器，容器启动默认运行的命令）
# docker start 或 docker run
CMD ["/bin/sh","-c","echo 2222;echo $param"]
