# 🛠️ AWS Step Functions + Amazon Bedrock — Assistente de Recomendação de Delivery

Este projeto demonstra como integrar **AWS Step Functions** com **Amazon Bedrock** para construir um fluxo de trabalho inteligente voltado à criação de um **assistente de recomendação de delivery**.

## ⚙️ Como funciona

A máquina de estados foi definida em JSON e visualmente no console da AWS, permitindo:

- Inicializar o processo de recomendação
- Verificar se há um prompt de entrada do usuário
- Invocar um modelo a qual está permitido para usar o Amazon Beadrock e personaliza-lo
- Finalizar o fluxo com sucesso

## 🎯 Objetivo

Criar uma solução escalável e modular que simula um assistente virtual capaz de sugerir opções de delivery com base nas preferências ou contexto fornecido pelo usuário.

## 🚀 Tecnologias utilizadas

- **AWS Step Functions**: para orquestração do fluxo de trabalho
- **Amazon Bedrock**: para integração com modelos de linguagem generativa
- **Titan Text Express v1**: modelo utilizado para gerar respostas baseadas em prompt

## 📦 Pré-requisitos

Antes de executar este projeto, certifique-se de ter:

- Uma conta AWS com permissões para usar Step Functions e Bedrock
- Permissão para invocar modelos via `arn:aws:states:::bedrock:invokeModel`
- AWS CLI configurado ou acesso ao console AWS
- Familiaridade com JSON e fluxos de trabalho serverless

## ▶️ Como rodar

1. Acesse o console do **AWS Step Functions**
2. Crie uma nova máquina de estados usando o modo visual (Workflow Studio)
3. Copie e cole a definição JSON do projeto
4. Execute o fluxo com um input contendo o campo `prompt`, por exemplo:

```json
{
  "input": {
    "prompt": "Quero sugestões de comida japonesa para entrega"
  }
}

