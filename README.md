# Protobuf Example Tutorial

go-lang [.proto](https://protobuf.dev/getting-started/gotutorial/)
python [.proto](https://protobuf.dev/getting-started/pythontutorial/)

```bash
➜ mkdir proto-buf-example && cd proto-buf-example
➜ vim addressbook.proto

# python write to file
➜ protoc ./addressbook.proto --python_out=$(pwd)
➜ python3 -m pip install  protobuf
➜ PROTOCOL_BUFFERS_PYTHON_IMPLEMENTATION=python python3 add_person.py address_book_file

# go read from file
➜ export GO111MODULE=on
➜ protoc ./addressbook.proto --go_out=$(pwd)
➜ cd github.com/protocolbuffers/protobuf/examples/go/tutorialpb
➜ go mod init github.com/protocolbuffers/protobuf/examples/go/tutorialpb 
➜ go mod tidy
➜ cd proto-buf-example
➜ go build listpeople.go
➜ proto-buf-example git:(main) ✗ ./listpeople address_book_file
Person ID: 1
  Name: Himanshu
  E-mail address: h123@123.com
  Work phone #: 111-111-111-11
```