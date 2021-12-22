# terraform_go
Build terraform with go

Terraform source code location
[https://github.com/hashicorp/terraform](https://github.com/hashicorp/terraform)

# build terraform from source

- clone the terraform repository
```
git clone https://github.com/hashicorp/terraform.git
```
- go the directory
```
cd terraform
```
- use ```go install``` to build the terraform version
```
go install
```
- test the terraform executable which should be found at ```${HOME}/go/bin/```
```
${HOME}/go/bin/terraform --version

vagrant@terraform-build:~/go/bin$ ${HOME}/go/bin/terraform --version
Terraform v1.1.0-dev
on linux_amd64
```

# build provider from source

- clone the aws plugin repository
```
git clone https://github.com/hashicorp/terraform-provider-aws.git
```
- go into the directory
```
cd terraform-provider-aws/
```
- install the necessary tools to build the provider
```
make tools
```
- build the provider
```
make build
```
- you know have a provider
```
${HOME}/go/bin/terraform-provider-aws
```