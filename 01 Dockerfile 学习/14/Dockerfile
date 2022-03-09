FROM alpine

ENV variable=baidu.com

CMD [ "/bin/sh","-c","ping ${variable}" ]

# ENTRYPOINT ping baidu.com + CMD 怎么写都没有用，容器启动的时候都是以 ENTRYPOINT 的完整命令为基准

# java -jar xxx.jar --spring.profile.active=dev --server.port=8888
# CMD [ "-jar","xxx.jar","--spring.profile.active=dev","--server.port=8888"]
# ENTRYPOINT [ "java" ]

