# Quick Start

## Intall dep

```shell
go get -u github.com/go-tower/tower
```

## Start a simple server

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

// Output
[Tower] 2021/10/19 03:54:35 Server listener at IP: 0.0.0.0, Port 8999, is starting
[Tower] 2021/10/19 03:54:35 Start server Tower success, now listening...
```

Server will listen on port `8999` in default.
