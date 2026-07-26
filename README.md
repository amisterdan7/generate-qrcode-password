# Gerador de QR Code e Senhas (CLI)

Uma aplicação utilitária via linha de comando (CLI) desenvolvida em Node.js que permite gerar QR Codes e senhas seguras de forma rápida e interativa.

---

## 🚀 Funcionalidades

- **Geração de QR Code:**
  - Escolha entre criar um QR Code simples para terminal ou um link de imagem.
  - Insira o link/texto desejado via prompt interativo.

- **Geração de Senhas Seguras:**
  - Gera senhas aleatórias personalizáveis.
  - Permite configurar o uso de letras maiúsculas, minúsculas, números e caracteres especiais através de variáveis de ambiente (`.env`).

---

## 🛠️ Tecnologias Utilizadas

- **Node.js**
- **prompt** (para menus e inputs interativos no terminal)
- **qrcode-terminal** (para renderização de QR Code no terminal)
- **chalk** (para estilização de textos e saídas)
- **dotenv** (gerenciamento de variáveis de ambiente)

---

## 📦 Como Instalar e Rodar

### Pré-requisitos
- [Node.js](https://nodejs.org/) instalado na máquina.

### Passo a Passo

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/SEU_USUARIO/gerador-QR.git
   cd gerador-QR
   ```

2. **Instale as dependências:**
   ```bash
   npm install
   ```

3. **Configure o arquivo `.env`:**
   Crie um arquivo `.env` na raiz do projeto baseado no seguinte exemplo:
   ```env
   UPPERCASE_LETTERS=true
   LOWERCASE_LETTERS=true
   NUMBERS=true
   SPECIAL_CHARACTERS=true
   PASSWORD_LENGTH=8
   ```

4. **Execute a aplicação:**
   ```bash
   npm start
   ```

---

## 📁 Estrutura do Projeto

```text
├── src/
│   ├── prompts/          # Configuração dos menus interativos
│   │   ├── prompt-main.js
│   │   └── prompt-qrcode.js
│   ├── services/         # Lógica de negócio da aplicação
│   │   ├── password/     # Módulo do gerador de senhas
│   │   │   ├── utils/
│   │   │   │   └── permitted-characters.js
│   │   │   ├── create.js
│   │   │   └── handle.js
│   │   └── qr-code/      # Módulo do gerador de QR Code
│   │       ├── create.js
│   │       └── handle.js
│   └── index.js          # Ponto de entrada da aplicação
├── .env                  # Variáveis de ambiente
├── package.json
└── README.md
```
