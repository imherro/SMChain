
## SMChain

* A Block Chain Using SM National Secret Algorithms

### Compiler Environment
---

* Alibaba Cloud or Huawei cloud host and ubuntu16.04.5 64-bit operating system

* docker ce >= 18.06.1-ce

* docker-compose >= 1.22.0

* golang >= go1.12.2

### Compilation step
---

* Execute commands in the $GOPATH directory：mkdir $GOPATH/src/github.com/hyperledger

* cd $GOPATH/src/github.com/hyperledger

* git clone the source code


* cd $GOPATH/src/github.com/hyperledger/SMChain

  ```
  make docker

  make native
  ```
(**Note**, make docker will report an error at the end, but it does not affect the use)
