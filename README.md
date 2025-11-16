🛒 Sistema de Gestão de Comércio (E-Commerce Backoffice)

Status: Desenvolvido para fins de estudo e portfólio em Programação Orientada a Objetos (POO) com integração a banco de dados.

Uma aplicação de console robusta em Java para gerenciamento básico de funcionários e estoque de produtos, demonstrando a integração entre Java e MySQL usando JDBC.

🔗 Tecnologias em Destaque

Categoria

Tecnologia

Versão Mínima

Linguagem

Java

17+

Banco de Dados

MySQL

8+

Conexão

JDBC

N/A

IDE

IntelliJ IDEA (Recomendado)

N/A

🚀 Funcionalidades Chave

O sistema opera através de um menu de console intuitivo, oferecendo gerenciamento completo de recursos humanos e estoque.

👤 Módulo: Gestão de Funcionários

Cadastrar Novos Funcionários: Inserção de nome, cargo e salário.

Listar Funcionários: Exibe todos os registros da base de dados.

Relatórios por Cargo: Filtra e exibe funcionários de um cargo específico.

Relatório Total: Gera uma contagem do número total de colaboradores.

📦 Módulo: Gestão de Produtos

Cadastrar Produtos: Inserção de nome, descrição, preço e estoque inicial.

Listar Produtos: Exibe todos os itens em estoque.

Relatórios de Estoque:

Estoque Baixo: Lista produtos com quantidade atual abaixo do limite mínimo definido.

Produtos Zerados: Lista itens que estão sem estoque (estoque_atual = 0).

Total de Itens: Soma a quantidade total de todas as unidades em estoque.

🗂 Exportação de Dados

Exportar Relatórios (TXT): Todos os relatórios gerados (funcionários, estoque baixo, produtos zerados) podem ser exportados para um arquivo .txt para fácil compartilhamento ou arquivamento.

⚙️ Configuração do Ambiente e Setup

Para rodar o projeto localmente, siga os passos abaixo:

1. Requisitos Prévios

Java Development Kit (JDK): Versão 17 ou superior instalada.

MySQL Server: Versão 8.0 ou superior em execução.

Driver JDBC: O arquivo .jar do conector MySQL/Java (geralmente mysql-connector-java-X.X.X.jar) deve ser adicionado como dependência do projeto.

2. Estrutura do Banco de Dados (MySQL)

Crie um banco de dados (ex: comercio_db) e execute os comandos SQL abaixo para configurar as tabelas funcionarios e produtos.

-- TABELA: FUNCIONARIOS
CREATE TABLE funcionarios (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  cargo VARCHAR(100) NOT NULL,
  salario DECIMAL(10, 2) NOT NULL
);

-- TABELA: PRODUTOS
CREATE TABLE produtos (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(150) NOT NULL,
  descricao TEXT,
  preco_venda DECIMAL(10, 2) NOT NULL,
  estoque_atual INT NOT NULL DEFAULT 0,
  estoque_minimo INT NOT NULL DEFAULT 10,
  data_cadastro TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


3. Configuração JDBC no Código

Na classe responsável pela conexão (DatabaseManager ou similar), ajuste as seguintes variáveis para o seu ambiente local:

private static final String JDBC_URL = "jdbc:mysql://localhost:3306/comercio_db";
private static final String DB_USER = "seu_usuario_mysql"; // Ex: root
private static final String DB_PASSWORD = "sua_senha_mysql"; 


🛠 Como Executar o Sistema

Clone o repositório: git clone https://www.youtube.com/watch?v=w1RGT6FpXyY

Abra o projeto na sua IDE (IntelliJ IDEA, Eclipse, VSCode).

Certifique-se de que o Driver JDBC está configurado corretamente.

Execute a classe principal comerce.java.

Interaja com o menu de opções no console.

🙋 Contribuições e Contato

Sinta-se à vontade para sugerir melhorias ou reportar problemas!

Autor: [Sara2006]

LinkedIn: [https://www.linkedin.com/public-profile/settings?trk=d_flagship3_profile_self_view_public_profile]

Email: [saravitoria2006@gmail.com]
