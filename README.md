# 🚀 Projeto: AWS S3 Upload Logger  
### _(Lambda + CloudFormation + CloudWatch)_

---

## 📘 Descrição do Projeto
Este projeto implementa uma infraestrutura simples e automatizada usando **AWS CloudFormation**.  
Sempre que um arquivo é enviado ao **Amazon S3**, uma função **AWS Lambda** é acionada automaticamente e registra no **CloudWatch Logs** o nome do arquivo e o bucket de origem.

💡 Ideal para aprender o fluxo de **eventos S3 → Lambda** e os fundamentos de **Infraestrutura como Código (IaC)** com CloudFormation.

---

## 🧱 Arquitetura da Solução

```text
┌────────────┐       evento "ObjectCreated"        ┌──────────────┐
│   S3 Bucket│────────────────────────────────────▶│   Lambda     │
│ (Uploads)  │                                     │ (Python)     │
└────────────┘                                     └──────┬───────┘
                                                            │
                                                            ▼
                                                   CloudWatch Logs

## 🎯 Objetivo de Aprendizado

Ao concluir este projeto, você será capaz de:

- 🚀 Criar uma infraestrutura automatizada com **AWS CloudFormation**  
- ⚙️ Configurar eventos do **Amazon S3** para acionar funções **AWS Lambda**  
- 📊 Monitorar logs no **Amazon CloudWatch**  
- 🧩 Documentar e versionar projetos de **IaC (Infrastructure as Code)**  

---

## ⚙️ Tecnologias Utilizadas

| Categoria | Serviço / Ferramenta |
|------------|----------------------|
| **Infraestrutura como Código** | AWS CloudFormation |
| **Armazenamento de Objetos** | Amazon S3 |
| **Execução Serverless** | AWS Lambda |
| **Monitoramento e Logs** | Amazon CloudWatch |
| **Linguagem** | Python 3.12 |

---

## 🪄 Passo a Passo de Implantação

### 1️⃣ Criar o Stack no CloudFormation

1. Acesse o serviço **AWS CloudFormation**  
2. Clique em **Create stack → With new resources (standard)**  
3. Faça upload do arquivo `template_s3_logger_unique.yaml`  
4. Dê um nome à pilha, por exemplo:  
s3-logger-stack
5. Clique em **Next → Next → Create stack**  
6. Aguarde até o status ficar **CREATE_COMPLETE ✅**

---

### 2️⃣ Verificar os Recursos Criados

- Vá até o **Amazon S3** e veja o bucket criado automaticamente  
- Vá até o **AWS Lambda** e veja a função criada:
s3-upload-logger-s3-logger-stack


---

### 3️⃣ Testar o Funcionamento

1. Acesse o bucket criado no **S3**  
2. Clique em **Upload → Add files**  
3. Envie qualquer arquivo (ex: `teste.txt`)  
4. Aguarde alguns segundos — a função **Lambda** será acionada automaticamente.  

---

### 4️⃣ Verificar Logs no CloudWatch

1. Vá até **CloudWatch → Log groups**  
2. Localize o grupo de logs da função Lambda:



✅ Se essa linha aparecer, o projeto está funcionando perfeitamente!

---

## 🔒 Boas Práticas Adotadas

- 🚫 Bloqueio total de ACLs e políticas públicas no **S3**  
- 🧠 Política **IAM** mínima necessária para a **Lambda** (logs e leitura de S3)  
- 🔁 Geração automática de **nomes de buckets únicos** (sem conflito entre pilhas)  
- 🧩 Infraestrutura **100% versionável** via **CloudFormation**  

---

## 🧠 Aprendizados Principais

- 🔔 Uso de **eventos S3** para acionar **Lambda Functions**  
- ⚙️ Estrutura de templates **YAML** no **CloudFormation**  
- 🔐 Configuração de **permissões e papéis** via **IAM Role**  
- 📜 Monitoramento e troubleshooting via **CloudWatch Logs**  
- 🛡️ Melhores práticas de **segurança e automação na AWS**

---

## 🧩 Estrutura do Projeto




