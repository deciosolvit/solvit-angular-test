# Solvit Angular Test

Esta aplicação pretende demonstrar conhecimentos em HTML, CSS e JS (Angular Framework). O objetivo é construir uma simples página de login, funcional, a partir de um layout fornecido.
Poderá utilizar, se pretender, qualquer framework CSS que ajude nessa responsividade como as listadas abaixo:

-   [Tailwind CSS](https://tailwindcss.com/)
-   [Bootstrap](https://getbootstrap.com/)

# Como iniciar o projeto

1. Fazer clone deste repositório
2. Abrir a pasta do projeto no IDE de preferência
3. Abrir o terminal no IDE ou abrir a pasta do projeto num terminal
4. Correr `npm install` para instalação dos pacotes Node
5. Após a instalação dos pacotes, correr no mesmo terminal, `ng serve` para criar um servidor de teste que estará acessível no browser em [http://localhost:4200/](http://localhost:4200/)

# Requisitos

-   A página deverá ser responsive (apenas desktop e mobile).
-   O login deverá ter uma chamada POST para o endpoint [https://json-placeholder.mock.beeceptor.com/login](https://json-placeholder.mock.beeceptor.com/login) em que envia o seguinte body: `{"username": "emailAqui",
"password": "passwordAqui"}` e deverá reagir de acordo com o resultado (sucesso ou insucesso). Poderá testar o mesmo enviando os prefixos `success-` ou `failed-` antes da password, ex: `failed-password`.

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
