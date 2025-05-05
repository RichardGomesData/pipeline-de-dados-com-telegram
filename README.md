# Pipeline de Dados com Telegram

Este projeto demonstra como construir um pipeline completo de dados utilizando o Telegram como interface de entrada e serviços da AWS como infraestrutura de processamento e armazenamento.

![[architecture 1.png]]
## 📌 Objetivo

Automatizar o recebimento, o processamento e o enriquecimento de dados via Telegram, utilizando serviços em nuvem (AWS) para transformar dados brutos em informações prontos para consulta analítica.

## ⚙️ Tecnologias Utilizadas

- **Python**
- **Telegram Bot API**
- **AWS Lambda**
- **AWS S3**
- **AWS Athena**
- **AWS API Gateway**
- **AWS IAM**
- **Pandas / JSON**

## 🧩 Estrutura do Pipeline

1. **Chat (Telegram)**  
   Interface de entrada para envio de mensagens e dados.

2. **API (AWS API Gateway)**  
   Ponto de integração entre Telegram e o backend.

3. **Raw Process (AWS Lambda)**  
   Função Lambda que processa e armazena os dados brutos no S3.

4. **Raw Data (AWS S3)**  
   Armazenamento dos dados crus recebidos.

5. **Enriched Process (AWS Lambda)**  
   Segunda função Lambda que enriquece os dados.

6. **Enriched Data (AWS S3)**  
   Armazenamento dos dados enriquecidos, prontos para análise.

7. **Enriched Query (AWS Athena)**  
   Consulta dos dados através de SQL no Athena.

## 📊 Resultados Esperados

- Centralização e automação da ingestão de dados via Telegram.
- Armazenamento seguro e escalável em S3.
- Transformações eficientes usando Lambda.
- Consulta simples e rápida usando Athena.

## ▶️ Como Executar

1. Configure o bot no Telegram com o **BotFather**.
2. Implemente as funções Lambda no AWS com base nos scripts do notebook.
3. Configure os buckets no S3 e permissões no IAM.
4. Configure a API Gateway para receber os dados do Telegram.
5. Execute o notebook para testes e análises.

## 🧪 Requisitos

- Conta na AWS (com permissões para Lambda, S3, API Gateway, Athena)
- Python 3.8+
- Bibliotecas: `requests`, `json`, `pandas`, `boto3`

## 📁 Estrutura do Repositório

```
📦 pipeline-telegram-aws
├── Pipeline_de_Dados_com_Telegram_Richard.ipynb
├── architecture.png
├── README.md
└── requirements.txt
```

## 📎 Observações

Este projeto foi desenvolvido como parte de um estudo prático sobre automação de pipelines utilizando interfaces conversacionais e serviços gerenciados de nuvem.
