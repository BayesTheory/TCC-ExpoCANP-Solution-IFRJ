# Sistema de Gerenciamento ExpoCANP - IFRJ (TCC)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <!-- Opcional: Badge de Licença -->

Sistema web desenvolvido como Trabalho de Conclusão de Curso (TCC) para o Instituto Federal de Educação, Ciência e Tecnologia do Rio de Janeiro (IFRJ) - Campus Pinheiral.

## Sobre o Projeto

A ExpoCANP é uma semana acadêmica que reúne palestras, minicursos, workshops e outros eventos no IFRJ Campus Pinheiral. Este sistema foi desenvolvido para [3]:
*   Facilitar o cadastro e gerenciamento desses eventos (palestras, minicursos, etc.).
*   Permitir que os alunos consultem a programação (dia, hora, local).
*   Informar sobre o número de vagas disponíveis.
*   Indicar o público-alvo de cada evento.

## Tecnologias Utilizadas

*   **Backend:** PHP 7.x (Laravel Framework - *confirmar versão se possível*) [3]
*   **Frontend:** HTML, CSS, JavaScript (Possivelmente com Bootstrap, Blade Templates)
*   **Banco de Dados:** MySQL [3]
*   **Gerenciador de Dependências:** Composer (PHP) [3], NPM/Yarn (JS - inferido por `package.json`, `yarn.lock`)
*   **Servidor Web:** (Recomendado: Apache ou Nginx)

## Pré-requisitos

Antes de começar, garanta que você tenha instalado [3]:
*   PHP >= 7.0 (Verificar a versão exata requerida pelo `composer.json`)
*   Servidor Web (Ex: Apache, Nginx)
*   MySQL
*   Composer
*   Node.js e NPM ou Yarn (para dependências frontend)

*Observação: Ferramentas como XAMPP, WAMP, MAMP (Windows/Mac) ou Laragon podem facilitar a instalação do ambiente PHP/MySQL/Servidor. O Laravel Valet (Mac) ou Sail (Docker) também são alternativas.*

## Instalação e Configuração

Siga os passos abaixo para configurar o ambiente de desenvolvimento local:

1.  **Clone o Repositório:**
    ```
    git clone https://github.com/BayesTheory/TCC-ExpoCANP-Solution-IFRJ.git
    cd TCC-ExpoCANP-Solution-IFRJ
    ```

2.  **Instale as Dependências PHP:**
    ```
    composer install
    ```

3.  **Instale as Dependências Frontend:**
    ```
    npm install
    # ou
    yarn install
    ```

4.  **Configure o Ambiente:**
    *   Copie o arquivo de exemplo `.env.example` para `.env`:
      ```
      copy .env.example .env # Windows
      # ou
      cp .env.example .env  # Linux/Mac
      ```
    *   Gere a chave da aplicação:
      ```
      php artisan key:generate
      ```
    *   **Edite o arquivo `.env`** e configure as credenciais de acesso ao seu banco de dados MySQL (DB_DATABASE, DB_USERNAME, DB_PASSWORD).

5.  **Banco de Dados:**
    *   Crie um banco de dados MySQL com o nome definido em `DB_DATABASE` no arquivo `.env`.
    *   Importe a estrutura inicial do banco de dados usando o script `expoCANP.sql` fornecido no repositório (utilize uma ferramenta como phpMyAdmin, DBeaver, ou o cliente `mysql`).
    *   Execute as migrations (para garantir que a estrutura esteja atualizada com o código):
      ```
      php artisan migrate
      ```
    *   (Opcional, mas recomendado se houver seeders) Execute os seeders para popular o banco com dados iniciais:
      ```
      php artisan db:seed
      ```
      *(Verificar se os seeders existem e são necessários)*

6.  **Compile os Assets Frontend:**
    ```
    npm run dev # Para desenvolvimento
    # ou
    npm run build # Para produção (ou `npm run prod`)
    # ou os comandos equivalentes com yarn
    ```

7.  **Inicie o Servidor de Desenvolvimento:**
    ```
    php artisan serve
    ```
    A aplicação estará geralmente disponível em `http://127.0.0.1:8000` ou `http://localhost:8000`.

## Uso

Atualmente está desativado!

## Licença

Distribuído sob a licença MIT. Veja `LICENSE` para mais informações.


