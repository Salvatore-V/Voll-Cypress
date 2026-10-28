# Voll Med - Automação de Testes E2E e API com Cypress

Este projeto consiste em uma suíte completa de testes automatizados (End-to-End e de API) desenvolvida utilizando **Cypress**, integrada a uma aplicação web em **React** e a um servidor backend em **Node.js/TypeScript** com base de dados SQLite.

---

## Tecnologias e Ferramentas Utilizadas

* **Testes Automatizados:** Cypress (E2E e API Testing)
* **Relatórios de Testes:** Mochawesome (com relatórios HTML detalhados em `cypress/results`)
* **Frontend:** React, TypeScript
* **Backend:** Node.js, Express, TypeScript, TypeORM, SQLite
* **Controle de Versão & CI:** Git, GitHub Actions (`.github/workflows/cypress.yml`)

---

## Estrutura do Projeto
vollmecypress-aula-5/
├── cypress/                # Suíte de testes automatizados com Cypress
│   ├── e2e/                # Cenários de teste (Login, Cadastro, Dashboard, API)
│   ├── fixtures/           # Massas de dados simuladas (clínicas, especialistas)
│   ├── results/            # Relatórios de execução (Mochawesome HTML)
│   └── support/            # Comandos personalizados e configurações globais
├── server/                 # API Backend (Node.js, TypeScript, TypeORM, SQLite)
└── web/                    # Aplicação Frontend (React e TypeScript) 


Principais Casos de Teste Implementados

A suíte de testes cobre fluxos críticos de negócio da aplicação médica, incluindo:

-Autenticação e Login: Validação de acessos via interface web e diretamente via rotas de API (login-api.cy.js, login-clinica.cy.js).
-Cadastro de Utilizadores: Testes automatizados garantindo o sucesso no registo de novos perfis (cadastro-sucesso.cy.js).
-Dashboard: Validação de interações e exibição correta de dados no painel administrativo (dashboard.cy.js).

Como Executar o Projeto Localmente
Pré-requisitos: Certifique-se de ter o Node.js instalado na sua máquina.

Instalação das Dependências:
Bash
# Na raiz do projeto ou diretórios específicos
npm install
Executar a API (Backend):

Bash
cd server
npm run start
Executar a Aplicação Web (Frontend):

Bash
cd web
npm start
Executar os Testes Cypress:

Bash
# Para abrir a interface gráfica do Cypress
npx cypress open

# Para executar os testes em modo headless (linha de comando)
npx cypress run
