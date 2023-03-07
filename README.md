#Prerequisite:
aws-cli/2.9.12 
Python/3.9.11
Terraform v1.3.9
go version go1.20.1 linux/amd64

#Steps:
Assuming that you have everything but Go lang setup .. 
Follow the steps here: https://go.dev/doc/install and install go version go1.20.1 linux/amd64

#check that Go setup is ok
cd terratest/examples-go/hello
go mod init github.com/aytov/terratest/examples-go/hello
go mod tidy
go run .

#run the terratests
cd terratest/terratest/test
go mod init github.com/aytov/terratest/terratest/test
go mod tidy
go test -v -timeout 30m
