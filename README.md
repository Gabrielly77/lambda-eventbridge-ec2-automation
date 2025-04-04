# lambda-eventbridge-ec2-automation

Automação com AWS Lambda, IAM e EventBridge

Este projeto foi realizado como parte de um laboratório prático na Escola da Nuvem, dentro da trilha de preparação para a certificação AWS Developer, com o objetivo de automatizar o encerramento de instâncias EC2 utilizando AWS Lambda, IAM e EventBridge.

Objetivo do Lab

Automatizar o encerramento de instâncias EC2 na AWS por meio de uma função Lambda escrita em Python, acionada por um evento personalizado do Amazon EventBridge.

Serviços Utilizados

-AWS Lambda

-IAM

-Amazon EventBridge

-EC2


Etapas

Criar política IAM com permissão para terminar instâncias EC2

Criar função Lambda com código em Python

Associar política/role à função Lambda

Criar regra no EventBridge para execução automática

Política IAM
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogStream",
        "logs:CreateLogGroup",
        "logs:PutLogEvents",
        "ec2:DescribeInstances",
        "ec2:TerminateInstances",
        "ec2:DescribeRegions"
      ],
      "Resource": "*"
    }
  ]
}

In English

Automation with AWS Lambda, IAM and EventBridge

This project was developed as part of a hands-on lab at Escola da Nuvem, in the AWS Developer certification track. It aims to automate EC2 instance termination using AWS Lambda, IAM, and EventBridge.

Date

April 04, 2025

Lab Goal

Automate the termination of EC2 instances in AWS using a Python-based Lambda function, triggered by a custom EventBridge event.

Services Used

-AWS Lambda

-IAM

-Amazon EventBridge

-EC2

Steps

Create an IAM policy allowing EC2 termination

Create a Lambda function using Python

Attach IAM role to Lambda function

Create EventBridge rule for automatic execution

IAM Policy
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "logs:CreateLogStream",
        "logs:CreateLogGroup",
        "logs:PutLogEvents",
        "ec2:DescribeInstances",
        "ec2:TerminateInstances",
        "ec2:DescribeRegions"
      ],
      "Resource": "*"
    }
  ]
}

Prints do Lab
https://files.oaiusercontent.com/file-QQYNKfNStJGKJTCrsMNX3S?se=2025-04-04T14%3A14%3A36Z&sp=r&sv=2024-08-04&sr=b&rscc=max-age%3D299%2C%20immutable%2C%20private&rscd=attachment%3B%20filename%3DCaptura%2520de%2520Tela%2520%25286503%2529.png&sig=49CVwMlhVG/pRRBPYemj9I594TrNocx7TcHIM62lrl0%3D



Aprendizados:
-Como aplicar o princípio do menor privilégio com políticas IAM.

-Integração entre Lambda, EventBridge e EC2.

-Escrita e deploy de função Lambda com Python.

-Automação de tarefas administrativas com segurança e eficiência.

