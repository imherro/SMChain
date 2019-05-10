
## SMChain

* A Block Chain Using SM National Secret Algorithms

### Compiler Environment
---

* Alibaba Cloud or Huawei cloud host and ubuntu16.04.5 64-bit operating system

* docker ce >= 18.06.1-ce

* docker-compose >= 1.22.0

* golang >= go1.12.2

* brook >= 20190401

### Compilation step
---

* Execute commands in the $GOPATH directory：mkdir $GOPATH/src/github.com/hyperledger

* cd $GOPATH/src/github.com/hyperledger

* git clone the source code

* Start agent tool brook:

  ```
  brook client -l 127.0.0.1:8080 -i 127.0.0.1 -s server_address:port -p password --http
  ```

* Set the proxy environment variable as follows: (If the host can directly access golang.org skip this step)

  ```
  export http_proxy=http://${proxy ip}:${proxy prot}

  export https_proxy=http://${proxy ip}:${proxy port}
  ```

* cd $GOPATH/src/github.com/hyperledger/SMChain

  ```
  make docker

  make native
  ```
(**Note**, make docker will report an error at the end, but it does not affect the use)
