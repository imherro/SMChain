
## Hyperledger Fabric国密版

* 支持国密算法的Hyperledger Fabric,其中Hyperledger Fabric的版本为1.4.0

### 编译环境
---

* 阿里云或华为云云主机及ubuntu16.04.5 64-bit操作系统

* docker ce >= 18.06.1-ce

* docker-compose >= 1.22.0

* golang >= go1.12.2

* brook >= 20190401

### 编译步骤
---

* 在$GOPATH目录下执行命令：mkdir $GOPATH/src/github.com/hyperledger

* cd $GOPATH/src/github.com/hyperledger

* git clone http://47.93.63.191:81/bqjc/fabric-gm

* 启动代理工具brook:

  ```
  brook client -l 127.0.0.1:8080 -i 127.0.0.1 -s server_address:port -p password --http
  ```

* 设置代理环境变量如下:（如果主机可直接访问golang.org跳过此步骤）

  ```
  export http_proxy=http://${proxy ip}:${proxy prot}

  export https_proxy=http://${proxy ip}:${proxy port}
  ```

* cd $GOPATH/src/github.com/hyperledger/fabric-gm

  ```
  make docker

  make native
  ```
  (**注意**，make docker的时候最后会报错，不影响使用)
