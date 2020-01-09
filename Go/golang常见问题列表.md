### Go相关常见问题列表
* * *
##### 1. 在go-micro中使用protocol buffer时，.proto文件只生成model而不生成rpc

解决：需要安装几个插件：
1） protoc-gen-micro

```shell
go get -u github.com/micro/protoc-gen-micro
go install github.com/micro/protoc-gen-micro
```
2） protoc-gen-go

```shell
go get github.com/golang/protobuf/protoc-gen-go
go install github.com/golang/protobuf/protoc-gen-go
```
这些插件默认安装在GOPATH/bin目录下。在用protoc编译生成可以引用GOPATH变量，也可以显式指定插件的位置。
具体可以参考：[protoc-gen-micro](https://github.com/micro/protoc-gen-micro)

##### 