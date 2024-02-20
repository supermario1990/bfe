# 1.启动bfe服务
./bfe -c ../config -l ../log
# 2.启动upstream_demo
go run upstream_demo/main.go
# 3.测试反向代理
curl -H "Host: example.org" 127.0.0.1:8989/echo