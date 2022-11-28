# Peer 2 Peer Blockchain Tutorial
```shell
go mod init blockchain-tutorial
```
```shell
go mod download
```
### Getting started

1，在中选执行以下命令：
 - 使用此命令，带有 `-secio`选项，则p2p连接的时候，也要带上
```shell
go run main.go -secio -l 10000
```
or
- 使用此命令，不带 `-secio`选项，则p2p连接的时候，不用带上此选项
```shell
go run main.go -l 10000
```
```shell
➜  p2p git:(me) go run main.go -l 10000       
2022/11/28 15:00:42 I am /ip4/127.0.0.1/tcp/10000/p2p/QmSUfGgEEcuS8STDSX18VPUgfU6ZuLxidBYwDUpp6MLgiD
2022/11/28 15:00:42 Now run "go run main.go -l 10001 -d /ip4/127.0.0.1/tcp/10000/p2p/QmSUfGgEEcuS8STDSX18VPUgfU6ZuLxidBYwDUpp6MLgiD" on a different terminal
2022/11/28 15:00:42 listening for connections
2022/11/28 15:01:14 Got a new stream!
```

2，根据上面的说明，复制上述命令执行后输出的新命令，并在一个新的终端执行：

```shell
go run main.go -l 10001 -d /ip4/127.0.0.1/tcp/10000/p2p/QmSUfGgEEcuS8STDSX18VPUgfU6ZuLxidBYwDUpp6MLgiD
```
3，根据上面的说明，复制上述命令执行后输出的新命令，并在一个新的终端执行：
```shell
go run main.go -l 10002 -d /ip4/127.0.0.1/tcp/10001/p2p/QmNWtjv6y3p5aSG8SWhq1Czpkcoqmz3hRBfcTnPDWZNxF5
```
Type a BPM into any of your terminals and watch your blockchain be broadcast to all terminals!
4，在任意一个终端输入一个 `BPM`值，其实就是一个整型数值，观察所有终端的，区块被广播到所有终端。
