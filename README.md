# simple-EC2.tf

TerraformでAWS上にEC2を立ち上げるサンプルです。  
基本的な構成要素は以下の通りです。  

* VPC
* Subnet
* Internet Gateway
* Route Table
* Security Group
* EC2

![成果物](./docs/img/fruit.gif)  

## 環境情報

| Name | Version |
| ---- | ---- |
| terraform | v1.3.7 |
| AWS CLI | 2.9.17 |

## 実行方法

`terraform.tfvars.example`をコピーして`terraform.tfvars`を作成し、適切な値を設定してください。  

```shell
terraform init
terraform plan
terraform apply
```

## その他イロイロ

ファイアウォールルールは以下の通りです。  

* インバウンド通信はSSH(22)・HTTP(80)・HTTPS(443)のみ許可
* SSHは自分のIPアドレスのみ許可
* アウトバウンド通信は全て許可
