📦 Cadastro de Produtos com Validação
Sistema web simples para cadastro de produtos, desenvolvido utilizando HTML, CSS, PHP e MySQL. O projeto possui um formulário para inserir o nome e o preço de um produto, realiza uma validação básica dos dados e armazena as informações em um banco de dados.

🎯 Objetivo
O objetivo deste projeto é desenvolver uma aplicação simples de cadastro de produtos, praticando:

Criação de formulários HTML;

Estilização básica com CSS;

Validação de dados;

Recebimento de dados utilizando PHP;

Conexão entre PHP e MySQL;

Inserção de dados em um banco de dados;

Exibição de mensagens de sucesso ou erro.

🛠️ Tecnologias utilizadas
HTML5 — Estrutura da página e formulário;

CSS3 — Estilização do cabeçalho;

PHP — Processamento e validação dos dados;

MySQL — Armazenamento dos produtos;

MySQLi — Conexão do PHP com o banco de dados.

📋 Funcionalidades
O sistema permite:

Informar o nome de um produto;

Informar o preço do produto;

Validar se o preço é maior que zero;

Cadastrar o produto no banco de dados;

Exibir uma mensagem de sucesso após o cadastro;

Exibir uma mensagem de erro caso ocorra algum problema;

Ocultar automaticamente a mensagem após alguns segundos.

🗄️ Banco de Dados
O projeto utiliza um banco de dados chamado exercicio.

É necessário criar a tabela produtos antes de executar o sistema.

Estrutura da tabela
CREATE DATABASE exercicio;

USE exercicio;

CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    preco DECIMAL(10,2) NOT NULL
);

⚙️ Configuração do banco de dados
No arquivo PHP, a conexão está configurada da seguinte maneira:

$servername = "localhost";
$username = "root";
$password = "Senai@118";
$dbname = "exercicio";

Caso as configurações do seu MySQL sejam diferentes, altere esses valores de acordo com o seu ambiente.

Importante: em projetos reais, não é recomendado deixar senhas do banco de dados diretamente no código-fonte. O ideal é utilizar variáveis de ambiente ou um arquivo de configuração protegido.

🚀 Como executar o projeto
1. Instale um servidor local
Você pode utilizar ferramentas como:

XAMPP

WAMP

Laragon

É necessário ter Apache, PHP e MySQL funcionando.

2. Coloque o projeto na pasta do servidor
No XAMPP, por exemplo, coloque os arquivos do projeto dentro de:

C:\xampp\htdocs\cadastro-produtos

3. Inicie os serviços
No painel do XAMPP, inicie:

Apache
MySQL

4. Crie o banco de dados
Acesse o phpMyAdmin e execute:

CREATE DATABASE exercicio;

USE exercicio;

CREATE TABLE produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(255) NOT NULL,
    preco DECIMAL(10,2) NOT NULL
);

5. Acesse o projeto
Abra o navegador e acesse:

http://localhost/cadastro-produtos/

📝 Funcionamento
O usuário preenche os campos:

Nome do Produto

Preço do Produto

Ao clicar em Cadastrar Produto, o formulário envia os dados utilizando o método POST.

O PHP verifica se a requisição foi enviada pelo método POST e recupera os valores:

$nome = $_POST['nomedoproduto'];
$preco = $_POST['preco'];

Em seguida, o sistema verifica se o preço é maior que zero.

Caso o preço seja inválido, uma mensagem de erro é apresentada:

Insira um preço maior que zero.

Caso seja válido, o sistema realiza a conexão com o banco de dados e insere o produto na tabela produtos.

Após o cadastro, é exibida a mensagem:

Produto cadastrado com sucesso!

A mensagem desaparece automaticamente após alguns segundos.

📁 Estrutura do projeto
Uma estrutura simples para o projeto pode ser:

cadastro-produtos/
│
├── index.php
└── README.md

🔐 Observação sobre segurança
Este projeto possui finalidade educacional. Para uma aplicação em produção, algumas melhorias seriam necessárias, principalmente na inserção dos dados no banco.

Atualmente, os valores são inseridos diretamente na consulta SQL. O recomendado é utilizar Prepared Statements para evitar problemas de SQL Injection.

Também seria importante realizar validações adicionais no servidor, como:

Verificar se o nome do produto foi preenchido;

Limitar o tamanho do nome;

Validar corretamente o formato do preço;

Tratar valores enviados diretamente pelo usuário;

Não armazenar credenciais do banco diretamente no código.

📚 Objetivo educacional
Este projeto foi desenvolvido como exercício para praticar a integração entre HTML, PHP e MySQL, demonstrando o funcionamento básico de um sistema de cadastro com validação e persistência de dados.

Projeto: Cadastro de Produtos com Validação
Tecnologias: HTML5, CSS3, PHP e MySQL
Finalidade: Educacional