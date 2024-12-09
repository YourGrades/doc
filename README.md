YourStock

## Descrição

YourStock é um sistema de controle de estoque que permite gerenciar os recebimentos de produtos, cadastrar e gerenciar fornecedores e acompanhamento das entregas.

## Índice

1. [Objetivos do Projeto](#objetivo)
2. [Definições, Acrônimos e Abreviações](#definição)
3. [Requisitos](#requisitos)
   1. [Requisitos Funcionais](#rf)
   2. [Requisitos Não Funcionais](#rnf)
4. [Diagramas UML](#uml)
   1. [Diagrama de Casos de Uso](#uc)
   2. [Diagrama de Classe](#classe)
5. [Estrutura do Projeto](#estrutura)
6. [Padrão de Projeto](#padrao)
7. [Contribuição](#contribuição)
8. [Licença](#licença)
9. [Contato](#contato)

## Definições, Acrônimos.
Definições:
● Produto: Item no estoque que possui atributos como código, nome, descrição,
quantidade, categoria e fornecedor.
● Categoria: Classificação do produto, representada por um conjunto de valores
possíveis (enum), com código, nome e descrição.
● Fornecedor: Entidade ou empresa responsável por fornecer os produtos. Possui
atributos como código, nome, contato, telefone e email.
● Entrega: Registro de uma entrega, incluindo o código da entrega, data, status, produto e sua quantidade.
● Estoque: Controle do inventário de produtos, incluindo operações como cadastrar,
remover e consultar produtos, além de atualizar as quantidades com base em
pedidos.

Acrônimo:
● ENUM: Tipo de dado que define um conjunto fixo de valores possíveis (por exemplo,
para "Status do Pedido").
● SQLite: Sistema de gerenciamento de banco de dados relacional utilizado para
armazenar os dados do sistema de estoque.
● CRUD: Create, Read, Update, Delete — Operações básicas para manipulação de
dados no sistema.

## Requisitos

### Requisitos Funcionais
Cadastro e Gerenciamento de Produtos
● O sistema deve permitir o cadastro de novos produtos, com informações como
código, nome, descrição, quantidade, preço, categoria e fornecedor.
● O sistema deve permitir a edição e exclusão de produtos do estoque.
● O sistema deve calcular o valor total do estoque com base na quantidade e no preço
de cada produto.

Gestão de Fornecedores
● O sistema deve permitir o cadastro e edição de fornecedores.
● O sistema deve associar cada produto a um fornecedor.
Controle de Entregas
● O sistema deve permitir o registro de novas entregas, associando produto e
quantidade
● O sistema deve permitir consultar o status de uma entrega (pendente, enviado,
entregue) e atualizar o status conforme necessário.
● O sistema deve calcular o valor total de uma entrega com base na quantidade e
preço do produto.

Consulta e Relatórios
● O sistema deve permitir a consulta de produtos por código e fornecedor.
● O sistema deve gerar relatórios sobre:
  ● Quantidade total e valor do estoque atual.
  ● Histórico de entregas.
  ● Produtos existentes (dentro e fora do estoque).
  ● Histórico de recebimentos.


### Requisitos Não Funcionais
Escalabilidade
● O sistema deve ser capaz de suportar o crescimento no número de produtos e
entregas, sem que haja degradação significativa de desempenho.
Integridade
● O sistema deve garantir a integridade de dados cadastrados.
Desempenho
● O sistema deve ter um tempo de resposta baixo nas operações de consultas e
atualizações.

## Diagramas UML
   
### Diagrama de Casos de Uso
  
![Diagrama_de_CasoDeUso](imagens/YourStockUC.png)
   
### Diagrama de Classe

![Diagrama_de_Classe](imagens/YourStockClass.png)

## Estrutura do Projeto 
- `source/YourStock/src/` : Código-fonte do projeto
- `docs/README.md` : Documentação do Projeto

## Tecnologias Utilizadas
- Java
- SQLite

## Padrão de Projeto
O padrão Singleton garante que uma classe tenha apenas uma instância em todo o ciclo de vida de uma aplicação, 
fornecendo um ponto de acesso global a essa única instância. Utilizamos para criarmos uma única conexão com o banco de dados utilizando um objeto Singleton, 
evitando a abertura de múltiplas conexões e otimizando o uso de recursos. 
A mesma lógica foi utilizada para implementar a Classe do Estoque, podendo ser acessada através de um objeto Singleton, otimizando recursos e evitando múltiplos pontos de acesso.

## Licença
Este projeto está licenciado sob a Licença MIT - veja o arquivo <LICENSE> para mais detalhes.

## Contato
Gabriel Vasconcelos - 423195476
Ideval Alves - 4231922247
Josué Rodrigues - 4231922098
Pedro Henrique de Melo Silva- 4231925480
Victor Joseph - 4231922732 
