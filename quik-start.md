# 快速开始

## 安装依赖

```
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
    SockServer := tower.NewBootStrap(&tower.Config{})
    SockServer.AddRoute(0, func(ctx *tower.Context) {
        fmt.Println("hello world")
    })
    SockServer.Listen()
}
```

服务启动会默认监听 9000 端口
