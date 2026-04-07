# 🤖 Chatbot Telegram com N8N - Consulta de Temperatura

## 📌 Descrição do Projeto

Este projeto consiste no desenvolvimento de um chatbot integrado ao Telegram utilizando a plataforma N8N. O objetivo do bot é receber o nome de uma cidade do Brasil, consultar a API do OpenWeather e retornar ao usuário a temperatura atual.

O fluxo do chatbot realiza as seguintes etapas:

* Captura da mensagem enviada pelo usuário no Telegram
* Tratamento e normalização do texto (remoção de acentos, padronização e limpeza de espaços)
* Consulta à API do OpenWeather
* Validação da resposta da API
* Retorno da temperatura ou mensagem de erro ao usuário

---

## ⚙️ Tecnologias Utilizadas

* N8N (Automação de workflows)
* Telegram Bot API
* OpenWeather API

---

## 📥 Como importar o workflow no N8N

1. Acesse o N8N
2. No menu principal, clique em **Import**
3. Selecione o arquivo:

   ```
   workflow-chatbot-telegram.json
   ```
4. O workflow será carregado automaticamente na sua instância

---

## 🔑 Configuração das Credenciais

### 📲 Telegram

1. Acesse o Telegram e procure por **@BotFather**

2. Siga a documentação abaixo e execute o passo a passo:
   
   * Link **https://docs.n8n.io/integrations/builtin/credentials/telegram/?utm_source=n8n_app&utm_medium=credential_settings&utm_campaign=create_new_credentials_modal** 

3. Copie o token gerado

4. No N8N:

   * Crie um nó Telegram Trigger:
     
     <img width="386" height="365" alt="image" src="https://github.com/user-attachments/assets/a03acec6-b7c2-4098-9e78-923e913d8bdb" />
     
   * Insira o token, conforme mostra a imagem abaixo:
     
     <img width="1180" height="415" alt="image" src="https://github.com/user-attachments/assets/dde4baf2-11d7-40ab-a636-f636bf1590d0" />


   * Clique em salvar e o telegram será conectado ao N8N 

---

### 🌤️ OpenWeather

1. Acesse:
   https://openweathermap.org/api
2. Crie uma conta gratuita
3. Gere sua API Key
4. O endpoint e a API KEY precisam ser inseridos em um nó http:


<img width="403" height="822" alt="image" src="https://github.com/user-attachments/assets/861c1074-8fdc-43a8-817f-becf44cbaa73" />


* Por questões de segurança a API KEY foi riscada

---


## ▶️ Como Executar o Chatbot

1. Ative o workflow no N8N (botão **Active**)
2. Acesse o Telegram
3. Envie uma mensagem para o bot

---

### 📍 Exemplo de Entrada:

```
São Paulo,SP
```

---

### ✅ Resposta Esperada:

```
🌤️ A temperatura em São Paulo é de 27°C
```

---

### ✅ Exemplo:

<img width="752" height="588" alt="image" src="https://github.com/user-attachments/assets/ca659737-3ad7-4e31-ac79-0018ad38b976" />


### ❌ Exemplo de Erro:

Caso o usuário envie uma cidade inválida:

```
❌ Cidade não encontrada. Use o formato Cidade,UF,BR (ex.: São Paulo,SP,BR).
```
