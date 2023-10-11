# Projeto Laravel

Este é um projeto Laravel que tem como objetivo criar um sistema de gerenciamento de assinaturas para um site de streaming. O sistema disponibiliza uma API Restful que permite que os clientes vejam suas faturas e pendências de pagamento. Cada cliente pode ter várias assinaturas ativas, e o sistema rastreia todas as informações relacionadas a essas assinaturas, incluindo faturas e histórico de pagamento.


## Requisitos

Antes de começar, certifique-se de ter os seguintes requisitos instalados em sua máquina:

- [PHP](https://www.php.net/) versão 8 ou superior
- [Composer](https://getcomposer.org/)
- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)
- [MySQL](https://www.mysql.com/) ou outro banco de dados relacional de sua escolha
- [Git](https://git-scm.com/)
- Servidor web (por exemplo, Apache, Nginx, etc.)

## Instruções de Instalação

Siga estas etapas para configurar e executar o projeto:

1. Clone o repositório:

```bash
git clone https://github.com/michaelrodriguess/apiLaravel.git
```
2. Navegue até a pasta do projeto:

  ```bash
  cd apiLaravel
```
3. Instale as dependências PHP com o Composer:

  ```bash
  composer install
  ```  
4. Copie o arquivo .env.example para .env:

  ```bash
  cp .env.example .env
```
5.Gere uma chave de aplicativo:

  ```bash
  php artisan key:generate
```

6.Configure o arquivo .env com as informações do banco de dados (DB_HOST, DB_PORT, DB_DATABASE, DB_USERNAME, DB_PASSWORD) e outras configurações relevantes.


7.Execute as migrações do banco de dados para criar as tabelas:

  ```bash
  php artisan migrate
```
8.Inicie o servidor de desenvolvimento:

  ```bash
  php artisan serve
```

Abra o navegador e acesse http://localhost:8000 para ver a aplicação em execução.

- Para acessar informações sobre clientes (customers), faça uma requisição GET para /api/version1/customers.
- Para criar um novo cliente, faça uma requisição POST para /api/version1/customers.
- Para atualizar informações de um cliente existente, faça uma requisição PATCH para /api/version1/customers/{id}.
- Para acessar informações sobre faturas (invoices), faça uma requisição GET para /api/version1/invoices.
- Para criar uma nova fatura, faça uma requisição POST para /api/version1/invoices.
- Para atualizar informações de uma fatura existente, faça uma requisição PATCH para /api/version1/invoices/{id}.
- Para fazer requisições com filtros de pesquisa, você pode incluir parâmetros na URL. Por exemplo, para buscar clientes com CEP (postalCode) maior que 30000 e tipo (type) igual a "I", você pode fazer uma requisição para /api/version1/customers?postalCode[gt]=30000&type[eq]=I

Certifique-se de incluir o token de autorização nas requisições da API para obter acesso aos recursos protegidos. Além disso, forneça os dados necessários no corpo das requisições POST e PATCH, conforme a estrutura da sua API.

### Contato
Se você tiver alguma dúvida ou precisar de ajuda, entre em contato com [Michael Rodrigues](https://www.linkedin.com/in/michaelrodriguess/) via michaelrodrigues.dev@proton.me

