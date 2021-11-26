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
```

Server will listen on port `9000` in default.
