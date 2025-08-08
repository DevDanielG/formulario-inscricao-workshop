# formulario-inscricao-workshop
Formulário web completo com HTML, CSS, JS, PHP e PostgreSQL para inscrição em workshop.

# Formulário de Inscrição - Workshop de Desenvolvimento Web

Este é um projeto fullstack que simula um formulário de **inscrição para um workshop fictício de desenvolvimento web**. Ele foi desenvolvido com **HTML, CSS e JavaScript** no frontend, **PHP** no backend e **PostgreSQL** para persistência dos dados.

## 🎯 Objetivo

Permitir que participantes se inscrevam no evento informando seus dados pessoais e preferências. Os dados são armazenados em um banco de dados PostgreSQL para posterior consulta pela organização.

## 🧩 Funcionalidades

- Formulário com campos:
  - Nome completo
  - Email
  - Telefone
  - Oficina desejada (Frontend, Backend, Fullstack)
  - Nível de experiência (Iniciante, Intermediário, Avançado)
  - Observações adicionais (campo livre)
- Validação básica no frontend
- Envio dos dados via POST
- Processamento e inserção dos dados via PHP
- Armazenamento em banco PostgreSQL

## 🛠️ Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript
- PHP 8+
- PostgreSQL

## 📁 Estrutura do Projeto

formulario-inscricao-workshop/
├── public/
│ ├── index.html # Formulário de inscrição
│ ├── style.css # Estilos do formulário
│ └── script.js # Validação básica
├── backend/
│ ├── db.php # Conexão com PostgreSQL
│ └── submit.php # Processamento dos dados do formulário
├── README.md
└── .gitignore

## ⚙️ Como Rodar Localmente

1. Clone o repositório:  
   ```bash
   git clone https://github.com/seu-usuario/formulario-inscricao-workshop.git
   cd formulario-inscricao-workshop

