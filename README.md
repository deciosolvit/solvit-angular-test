# Solvit Angular Test

Esta aplicação pretende demonstrar conhecimentos em HTML, CSS e JS (Angular Framework). O objetivo é construir uma simples página de login, funcional, a partir de um layout fornecido.
Poderá utilizar, se pretender, qualquer framework CSS que ajude nessa responsividade como as listadas abaixo:

-   [Tailwind CSS](https://tailwindcss.com/)
-   [Bootstrap](https://getbootstrap.com/)

## Como iniciar o projeto

Pré requisitos

-   Deverá ter o Node.js instalado - [Node.js](https://nodejs.org/pt/download/package-manager)
-   Deverá ter o AngularCLI (ng) instalado - [AngularCLI](https://v17.angular.io/guide/setup-local#install-the-angular-cli)

1. Fazer clone deste repositório
2. Abrir a pasta do projeto no IDE de preferência
3. Abrir o terminal no IDE ou abrir a pasta do projeto num terminal
4. Correr `npm install` para instalação dos pacotes Node
5. Após a instalação dos pacotes, correr no mesmo terminal, `ng serve` para criar um servidor de teste que estará acessível no browser em [http://localhost:4200/](http://localhost:4200/)

## Requisitos

-   O login deverá residir no ficheiro `app.component.html` com os métodos no ficheiro `app.component.ts`
-   O tipo de letra a utilizar é o [Plus Jakarta Sans](https://fonts.google.com/specimen/Plus+Jakarta+Sans?query=jakarta) disponível para inclusão no link fornecido
-   A página deverá ser responsive (apenas desktop e mobile).
-   O email deve ser validado como tal (incluir @ e . após o domínio)
-   A password deve ter um mínimo de 8 caracteres
-   Em caso de erro nalguma destas validações deve mostrar o erro correspondente
-   O login deverá ter uma chamada POST para o endpoint [https://json-placeholder.mock.beeceptor.com/login](https://json-placeholder.mock.beeceptor.com/login) em que envia o seguinte body: `{"username": "emailAqui",
"password": "passwordAqui"}` e deverá reagir de acordo com o resultado (sucesso ou insucesso). Poderá testar o mesmo enviando os prefixos `success-` ou `failed-` antes da password, ex: `failed-password`.
-   O código deve compilar correndo o comando `ng build` no terminal

### Exemplos de respostas do endpoint

#### Sucesso

    {
        "success": true,
        "message": "Login successful",
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...."
    }

#### Insucesso

    {
        "success": false,
        "error": {
            "code": "invalid_credentials",
            "message": "Invalid username or password."
        }
    }
