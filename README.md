# Formulário de Inscrição - Workshop de Desenvolvimento Web

Este é um projeto **full-stack** que simula um formulário de inscrição para um workshop fictício, utilizando uma arquitetura de aplicação web moderna. O desenvolvimento separa o **front-end** do **back-end** para garantir escalabilidade e uma melhor experiência do usuário.

* **Front-end:** Construído com **HTML, CSS e JavaScript**. A lógica de interação e a comunicação com o servidor são realizadas de forma assíncrona.
* **Back-end:** Desenvolvido em **PHP** para atuar como uma **API REST** que recebe, processa e armazena os dados em um banco **PostgreSQL**.

---

## 🎯 Objetivo

Permitir que os participantes se inscrevam no evento através de uma interface fluida. Os dados são enviados do navegador para o servidor sem a necessidade de recarregar a página, o que garante um processo de inscrição eficiente e ágil.

---

## 🧩 Funcionalidades

* Formulário com campos:
    * Nome completo
    * Email
    * Telefone
    * Oficina desejada (Frontend, Backend, Fullstack)
    * Nível de experiência (Iniciante, Intermediário, Avançado)
    * Observações adicionais (campo livre)
* **Validação em tempo real** no front-end para uma melhor usabilidade.
* **Envio de dados assíncrono** (sem recarregar a página) via JavaScript (Fetch API).
* API em PHP para validação e inserção dos dados em banco.
* Armazenamento em banco **PostgreSQL**.

---

## 🛠️ Tecnologias Utilizadas

* HTML5
* CSS3
* JavaScript
* PHP 8+
* PostgreSQL

---

📁 Estrutura do Projeto

formulario-inscricao-workshop/ 
├── frontend/
│   ├── index.html # Estrutura do formulário
│   ├── style.css # Estilos e design
│   └── script.js # Lógica de validação e comunicação assíncrona com a API 
├── backend/ 
│   ├── db.php # Conexão com o banco de dados PostgreSQL 
│   └── submit.php # API que processa e insere os dados no banco 
├── README.md 
└── .gitignore
---

## ⚙️ Como Rodar Localmente

1.  Clone o repositório:
    ```bash
    git clone [https://github.com/seu-usuario/formulario-inscricao-workshop.git](https://github.com/seu-usuario/formulario-inscricao-workshop.git)
    cd formulario-inscricao-workshop
    ```
2.  **Configuração do Banco de Dados (PostgreSQL):**
    * Crie um banco de dados com o nome `[nome-do-banco]`.
    * Execute o script SQL a seguir para criar a tabela de inscrições:
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
3.  **Configuração do Servidor Local (PHP):**
    * Certifique-se de ter um servidor local como **XAMPP, WAMP ou MAMP** instalado.
    * Configure a conexão com o banco de dados editando o arquivo `backend/db.php`. Preencha as seguintes informações:
        ```php
        <?php
        $host = "localhost";
        $dbname = "[nome-do-banco]";
        $user = "[seu-usuario-do-banco]";
        $password = "[sua-senha-do-banco]";
        
        try {
            $conn = new PDO("pgsql:host=$host;dbname=$dbname", $user, $password);
            $conn->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);
        } catch (PDOException $e) {
            die("Erro de conexão: " . $e->getMessage());
        }
        ?>
        ```
4.  **Inicie o Servidor:**
    * Coloque a pasta do projeto no diretório do seu servidor local (`htdocs` para XAMPP, `www` para WAMP, etc.).
    * Inicie o servidor e acesse o projeto pelo seu navegador em `http://localhost/[nome-da-pasta]`.
