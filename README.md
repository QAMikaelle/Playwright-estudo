# Playwright-estudo (Versão Cypress)

![Cypress](https://img.shields.io/badge/-cypress-%23E5E5E5?style=for-the-badge&logo=cypress&logoColor=058a5e)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)

Este repositório, apesar do nome sugestivo de estudo de Playwright, contém atualmente uma implementação de testes End-to-End (E2E) utilizando **Cypress**. O projeto foca na validação de vitrines e fluxos de autenticação da plataforma Lector Live.

## Cenários Automatizados

Os testes estão organizados em especificações (`.cy.js`) cobrindo as seguintes funcionalidades:

### Autenticação (`login.cy.js`)
* **Fluxos Negativos:** Validação de tentativas de login com e-mail ou senha incorretos.
* **Fluxo Positivo:** Login com sucesso (Happy Path).

### Vitrines e Categorias (`vitrines.cy.js`)
* **Navegação:** Acesso à vitrine de cursos.
* **Gestão de Categorias:** Criação de novas categorias na vitrine e validação de persistência dos dados.

## Stack Tecnológica

* **Linguagem:** JavaScript
* **Framework de Teste:** [Cypress](https://www.cypress.io/)
* **Ambiente:** Node.js

## Instalação e Configuração

Siga os passos abaixo para rodar o projeto localmente:

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/QAMikaelle/Playwright-estudo.git](https://github.com/QAMikaelle/Playwright-estudo.git)
   cd Playwright-estudo
   ```

## Instale as dependências:
```
npm install
```

## Como Executar os Teste:

### Modo Interface (Interativo)
Para abrir o Test Runner do Cypress e ver a execução em tempo real:

```
npx cypress open
```

### Modo Headless (Linha de Comando)
Para rodar todos os testes no terminal (ideal para CI/CD):

```
npx cypress run
```

### Para rodar apenas um arquivo específico:

```
npx cypress run --spec "cypress/e2e/vitrines.cy.js"
```

## Estrutura de Pastas:
```
Playwright-estudo/
│
├── cypress/
│   ├── e2e/
│   │   ├── login.cy.js       # Testes de Login
│   │   └── vitrines.cy.js    # Testes de Vitrines
│   ├── fixtures/             # Massas de dados
│   └── support/              # Comandos customizados (commands.js)
│
├── cypress.config.js         # Configuração global do Cypress
├── package.json              # Dependências do projeto
└── README.md                 # Documentação
