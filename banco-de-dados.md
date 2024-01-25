## Introdução aos Bancos de Dados

- Um banco de dados é uma coleção organizada de informações - ou dados - estruturadas, normalmente armazenadas eletronicamente em um sistema de computador. 
- Um banco de dados normalmente é controlado por um gerenciador  de banco de dados (**DBMS** ou **SGMS**)
  - MySQL, PostgreSQL, Microsoft SQL Server (são SGMS)
  - Inserir, excluir, acessar, visualizar, selecionar, ordenar, juntar ou intercalar registros;
  - Copiar e eliminar ficheiros;
  - Alterar estruturas de campos;
  - Inserir, remover e estabelecer relações entre tabelas;
  - Importar ou exportar dados entre outras bases de dados;
  - Criar chaves primárias e externas;
  - Realizar consultas, elaborar formulários e relatórios na base de dados;
  - Criar usuários, com permissões de acesso diferenciados.

## Tipos de Bancos de Dados

- SGBDs relacionais, difundidos e consolidados já há algum tempo;
- E os conhecidos como NoSQL (Not Only SQL). Estes últimos, cada vez mais vem conquistando espaço nas organizações


- Bancos de Dados Relacionais
 - O banco de dados relacional tem como base a utilização de tabelas
 - linhas e colunas que se relacionam
 - **Analogia com Excel**

Exemplos: MySQL, PostgreSQL.

## Exemplo prático de SQL RELACIONAL

### Cenário: Sistema de Gerenciamento de Pedidos em um E-commerce

Imagine um sistema de gerenciamento de pedidos para um e-commerce, onde você precisa armazenar informações sobre clientes, produtos, pedidos e suas relações. Nesse caso, um banco de dados relacional é geralmente mais apropriado devido à estrutura altamente organizada e inter-relacional dos dados.

#### Modelo de Dados Relacional:

Tabelas:

- Tabela de Clientes (customer_id, nome, email, etc.)
- Tabela de Produtos (product_id, nome, preço, etc.)
- Tabela de Pedidos (order_id, customer_id, data, etc.)
- Tabela de Itens do Pedido (order_id, product_id, quantidade, etc.)

**Relacionamentos**:

- Um cliente pode fazer vários pedidos (relacionamento 1:N entre Clientes e Pedidos).
- Um pedido pode conter vários itens (relacionamento 1:N entre Pedidos e Itens do Pedido).
- Cada item do pedido está associado a um produto específico.

Por que um banco relacional é apropriado:

**Integridade Referencial**: O modelo relacional suporta a integridade referencial, garantindo que todas as referências entre as tabelas sejam válidas. Por exemplo, não podemos ter um pedido associado a um cliente inexistente.

**Transações ACID**: Para um sistema de e-commerce, é crucial manter a consistência dos dados. O modelo relacional oferece suporte a propriedades ACID (Atomicidade, Consistência, Isolamento e Durabilidade), garantindo transações seguras.

**Consultas Complexas**: O SQL, a linguagem padrão para bancos de dados relacionais, permite realizar consultas complexas e relacionadas, essenciais para extrair informações detalhadas sobre clientes, pedidos e produtos.

**Escalabilidade Vertical**: Em muitos casos, um sistema de e-commerce pode funcionar bem com escalabilidade vertical (adicionando mais recursos a um servidor existente) em vez de escalabilidade horizontal (adicionando mais servidores). Bancos de dados relacionais são frequentemente otimizados para esse tipo de escalabilidade.

Enquanto bancos de dados não relacionais (como bancos de dados de documentos ou grafos) têm suas vantagens em certos cenários, a estrutura fortemente relacionada e transacional de um banco de dados relacional faz sentido quando você precisa de consistência e relacionamentos complexos entre os dados.


Bancos de Dados Não Relacionais (NoSQL)
 - tables dao lugar a coleção de dados (mongo)
 - nao gera um relacionamento forte entre os dados

Exemplos: MongoDB (orientado a documentos), Redis (chave-valor), Cassandra (colunas largas)

## Exemplo prático de NOSQL NÃO RELACIONAL


### Cenário: Sistema de Comentários em um Blog ou Fórum

Imagine um sistema de comentários para um blog ou fórum online, onde os dados não têm uma estrutura rígida e podem variar de comentário para comentário. Neste caso, um banco de dados não relacional, como um banco de dados de documentos baseado em JSON, poderia ser mais adequado.

#### Modelo de Dados NoSQL:

Coleção de Comentários:
Cada comentário é armazenado como um documento JSON.
Os documentos podem ter campos diferentes, dependendo do conteúdo do comentário.
Exemplo de documentos:

```json
{
   "comment_id": 1,
   "user_id": 123,
   "username": "usuario123",
   "content": "Ótimo post!",
   "timestamp": "2024-01-25T12:30:00Z",
   "likes": 5,
   "replies": [
      {
         "comment_id": 2,
         "user_id": 456,
         "username": "outro_usuario",
         "content": "Concordo totalmente!",
         "timestamp": "2024-01-25T12:45:00Z",
         "likes": 2
      }
   ]
}
```

**Por que um banco não relacional é apropriado**:

- Esquema Flexível: Os bancos de dados NoSQL permitem que os documentos tenham esquemas flexíveis. Cada comentário pode ter campos diferentes, e novos campos podem ser adicionados sem afetar outros comentários.

- Desempenho em Leitura e Gravação: Em sistemas com grande volume de leitura e gravação, os bancos de dados NoSQL podem ser mais eficientes. Como os comentários podem variar em estrutura, não há a necessidade de consultar várias tabelas relacionadas.

- Evolução Gradual do Esquema: À medida que o sistema evolui, novos campos podem ser introduzidos nos documentos sem a necessidade de alterações em toda a base de dados. Isso é particularmente útil em ambientes dinâmicos.

- Escala Horizontal: Bancos de dados NoSQL são frequentemente projetados para escala horizontal, permitindo adicionar mais servidores conforme a demanda aumenta.

## NewSQL, o banco de dados misto

Aqui, a ideia é pegar o melhor dos bancos de dados relacionais e não relacionais para formar uma ferramenta extremamente prática, segura e funcional.