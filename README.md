# lambda-eventbridge-ec2-automation

**Automação com AWS Lambda, IAM e EventBridge**

Este projeto foi realizado como parte de um laboratório prático na Escola da Nuvem, dentro da trilha de preparação para a certificação AWS Developer, com o objetivo de automatizar o encerramento de instâncias EC2 utilizando AWS Lambda, IAM e EventBridge.

**Prints do Lab**
![image](https://github.com/user-attachments/assets/bbc3a08b-998b-4035-9ff9-060e6f251547)
![image](https://github.com/user-attachments/assets/b1c04fa7-3626-4ac9-9728-6bf97a88d134)
![image](https://github.com/user-attachments/assets/78a89ed7-0ac1-446f-8b9c-d7c8743029d7)

**Objetivo do Lab**

Automatizar o encerramento de instâncias EC2 na AWS por meio de uma função Lambda escrita em Python, acionada por um evento personalizado do Amazon EventBridge.

**Serviços Utilizados**

- *AWS Lambda*

- *IAM*

- *Amazon EventBridge*

- *EC2*


**Etapas**

*Criar política IAM com permissão para terminar instâncias EC2*

*Criar função Lambda com código em Python*

*Associar política/role à função Lambda*

*Criar regra no EventBridge para execução automática*

**Política IAM**
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

**Aprendizados:**

- *Como aplicar o princípio do menor privilégio com políticas IAM.*

- *Integração entre Lambda, EventBridge e EC2.*

- *Escrita e deploy de função Lambda com Python.*

- *Automação de tarefas administrativas com segurança e eficiência.*

**In English**

Automation with AWS Lambda, IAM and EventBridge

This project was developed as part of a hands-on lab at Escola da Nuvem, in the AWS Developer certification track. It aims to automate EC2 instance termination using AWS Lambda, IAM, and EventBridge.

**Lab Goal**

Automate the termination of EC2 instances in AWS using a Python-based Lambda function, triggered by a custom EventBridge event.

**Services Used**

- *AWS Lambda*

- *IAM*

- *Amazon EventBridge*

- *EC2*

**Steps**

*Create an IAM policy allowing EC2 termination*

*Create a Lambda function using Python*

*Attach IAM role to Lambda function*

*Create EventBridge rule for automatic execution*

**IAM Policy**
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

**Learnings:**
- *How to apply the principle of least privilege with IAM policies.*

- *Integration between Lambda, EventBridge, and EC2.*

- *Writing and deploying a Lambda function with Python.*

- *Automating administrative tasks with security and efficiency.*









