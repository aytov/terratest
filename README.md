#Prerequisite: <br>
aws-cli/2.9.12 <br>
Python/3.9.11<br>
Terraform v1.3.9<br>
go version go1.20.1 linux/amd64<br>

#Steps:<br>
Assuming that you have everything but Go lang setup .. <br>
Follow the steps here: https://go.dev/doc/install and install go version go1.20.1 linux/amd64<br>

#check that Go setup is ok<br>
cd terratest/examples-go/hello<br>
go mod init github.com/aytov/terratest/examples-go/hello<br>
go mod tidy<br>
go run .<br>

#run the terratests<br>
cd terratest/terratest/test<br>
go mod init github.com/aytov/terratest/terratest/test<br>
go mod tidy<br>
go test -v -timeout 30m<br>
