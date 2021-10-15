# 配置

## 新建一个配置

返回一个默认配置

```golang
package main

import "github.com/go-tower/tower

func main() {
    conf = tower.NewConfig()
    bs := tower.NewBootStrap(conf)
}
```

## 配置字段

```golang
type Config struct {
	Name             string // server name
	IP               string // server listen ip
	IPVersion        string // ip version
	Port             int    // server listen port
	MaxPacketSize    uint32 // server accept max packet size
	MaxConn          int    // server accept max connection count
	WorkerPoolSize   uint32 // work pool
	MaxWorkerTaskLen uint32 // 业务工作Worker对应负责的任务队列最大任务存储数量
	MaxMsgChanLen    uint32 // SendBuffMsg发送消息的缓冲最大长度
}
```

- `name`: 服务名
- `IP`: 监听的 IP
- `IPVersion`: IP 版本 目前只支持 IPv4
- `Port`: 监听的端口
- `MaxPacketSize`: 最大的包大小
- `MaxConn`: 最大的连接数量数量
- `WorkerPoolSize`:
- `MaxWorkerTaskLen`:
- `MaxMsgChanLen`:
