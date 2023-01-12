** AWS CLI e CloudShell**

>Linha de comandos da AWS

1. Opção alternativa à utilização do console
2. Utiliza comandos no shell da linha de comando
3. Executa comandos equivalentes ao do console com o mínimo de configuração
4. Utiliza Shell do Linux, Prompt ou Powershell do Windows, remotamente via SSH (putty)
5. Faz chamadas de API
6. Versão 2: recomendada (na época)

> Configurando o CLI

1. Cadastro na AWS
2. Conta de usuário no IAM
3. Chave ID, Access Key e Secret Key (credenciais)
4. Versão do CLI instalado
5. Configuração com credenciais do usuário criado do IAM
6. Instalação do CLI no Linux/Windows
7. comando aws configure com import csv, String JSON ou YML
8. Interagindo com o CLI: 

$aws configure -- profile saulo
$key ID: Posso colocar a access key
$Secret Key: Posso colocar meu secret key
$us-east-1; json
$aws S3 ls --profile saulo: Lista os buckets do S3
Posso setar a região através do comando:
$aws set region
Formato:
$aws <command><subcommands>[options and parameters]
$aws EC2 describe-instances
$aws --help
$aws create-security-group --group-name SGNAME
$aws iam create-user --username USERNAME

>Criando uma instância EC2 pelo CLI:

$aws EC2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.micro --key-name MEUPARDECHAVE --security-group-ids SG-xxxxx

>Criando VPC e subnets

$aws EC2 create-vpc --cidr-block 10.0.0.0/16
$aws EC2 create-subnet --vpc-id vpc-xxxxxx --cidr-block 10.0.1.0/24

>Criando tabela de roteamento

$aws EC2 create-internet-gateway
$aws EC2 attach-internet-gateway --gateway-id igw-xxxxxx --vpc-id vpc-xxxxx
$aws EC2 create-route-table
$aws EC2 associate-route-table --route-table-id rt-xxxxx --vpc-id vpc-xxxxx
$aws EC2 create-route --route-table-id rt-xxxxx --destination-cidr-block 0.0.0.0/0 --gateway-id igw-xxxxx

>Adicionando tags a recursos existentes

$aws create-tags ARN --tags TAG

>CloudShell

1. Iniciado dentro do console
2. Comandos do CLI já pré-configurados
3. Ambiente com base no AmazonLinux2
4. Ampla gama de ferramentas de desenvolvimento
5. Limite de armazenamento persistente de 1Gb restrito à Home do usuário