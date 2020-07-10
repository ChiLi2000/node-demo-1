# nodejs-test


## 启动应用

`node server.js 8888`

或者

`node server 8888`

## 添加路由

1. 编辑 server.js 文件，添加 if else
2. 重新运行 node server.js 8888

## 后台部署应用
1. git clone https://github.com/ChiLi2000/node-demo-1.git
2. cd node-demo-1
3. touch log
4. 启动命令：node server.js 8888 > log 2>&1 & 把启动命令做成 start 文件
5. 添加执行权限 chmod +x ./start
6. 运行 sh ./start 得到一个进程号 pid
- tail log 看 log 内容
- kill -9 pid 可以关掉进程
10. killall node 可以关掉所有 node 进程



## 如何重启应用
1. ssh frank@实例ip
2. cd node-demo-1
3. git pull
4. killall node（因为忘了进程号，实际上可以记下来）
5. sh ./start