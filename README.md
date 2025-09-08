

```markdown
# Formulário de Inscrição - Workshop de Desenvolvimento Web

Este é um projeto **full-stack** que simula um formulário de inscrição para um workshop fictício, utilizando uma arquitetura de aplicação web moderna. O desenvolvimento separa o **front-end** do **back-end** para garantir escalabilidade e uma melhor experiência do usuário.

- **Front-end:** Construído com **HTML**, **CSS** e **JavaScript**. A lógica de interação e a comunicação com o servidor são realizadas de forma assíncrona.
- **Back-end:** Desenvolvido em **Node.js** para atuar como uma **API REST** que recebe, processa e armazena os dados em um banco **PostgreSQL**.

### 🎯 Objetivo

Permitir que os participantes se inscrevam no evento através de uma interface fluida. Os dados são enviados do navegador para o servidor sem a necessidade de recarregar a página, o que garante um processo de inscrição eficiente e ágil.

### 🧩 Funcionalidades

- **Formulário com campos:**
  - Nome completo
  - E-mail
  - Telefone
  - Oficina desejada (Frontend, Backend, Fullstack)
  - Nível de experiência (Iniciante, Intermediário, Avançado)
  - Observações adicionais (campo livre)
- Validação em tempo real no front-end para uma melhor usabilidade.
- Envio de dados assíncrono (sem recarregar a página) via JavaScript (Fetch API).
- API em Node.js para validação e inserção de dados no banco.
- Armazenamento no banco PostgreSQL.

### 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- Node.js (com Express.js)
- PostgreSQL

### 📁 Estrutura do Projeto

```

formulario-inscricao-workshop/
├── frontend/
│   ├── index.html \# Estrutura do formulário
│   ├── style.css \# Estilos e design
│   └── script.js \# Lógica de validação e comunicação assíncrona com a API
├── backend/
│   ├── .env \# Variáveis de ambiente
│   ├── node\_modules/ \# Módulos instalados
│   ├── package.json \# Metadados do projeto e dependências
│   ├── package-lock.json \# Gerencia as versões das dependências
│   └── server.js \# Servidor Node.js (API)
├── README.md
└── .gitignore

````

### ⚙️ Como Rodar Localmente

**1. Clone o repositório:**
```bash
git clone [https://github.com/DevDanielG/formulario-inscricao-workshop.git](https://github.com/DevDanielG/formulario-inscricao-workshop.git)
cd formulario-inscricao-workshop
````

**2. Configuração do Banco de Dados (PostgreSQL):**

  - Crie um banco de dados.
  - Execute o script SQL a seguir para criar a tabela de inscrições:

<!-- end list -->

```sql
CREATE TABLE inscricoes (
    id SERIAL PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL UNIQUE,
    telefone VARCHAR(20),
    oficina VARCHAR(50),
    experiencia VARCHAR(50),
    observacoes TEXT,
    data_inscricao TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

**3. Configuração do Back-end (Node.js):**

  - Crie um arquivo chamado `.env` na pasta `backend/` e adicione as suas credenciais do banco de dados:

<!-- end list -->

```
DB_USER=seu_usuario_do_banco
DB_HOST=localhost
DB_DATABASE=nome_do_seu_banco
DB_PASSWORD=sua_senha_do_banco
DB_PORT=5432
PORT=3000
```

  - Dentro da pasta `backend`, instale as dependências:

<!-- end list -->

```bash
cd backend
npm install express pg dotenv
```

  - Inicie o servidor Node.js:

<!-- end list -->

```bash
node server.js
```

**4. Configuração do Front-end (HTML/CSS/JS):**

  - Abra a pasta `frontend/` no seu navegador. A forma mais fácil é usando a extensão **Live Server** do VS Code.
  - Se preferir, abra o arquivo `index.html` diretamente no seu navegador.

<!-- end list -->

```
```
