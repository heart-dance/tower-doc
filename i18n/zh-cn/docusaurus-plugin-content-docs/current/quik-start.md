# 快速开始

## 安装依赖

```shell
go get -u github.com/go-tower/tower
```

## 启动一个服务

```go
package main

import (
    "fmt"
    "github.com/go-tower/tower"
)

func main() {
    SockServer := tower.NewBootStrap(nil)
    SockServer.Listen()
}

// Output
[Tower] 2021/10/19 03:54:35 Server listener at IP: 0.0.0.0, Port 8999, is starting
[Tower] 2021/10/19 03:54:35 Start server Tower success, now listening...
```

服务启动会默认监听 9000 端口
