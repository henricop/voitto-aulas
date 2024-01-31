## Introdução aos Bancos de Dados
- Um banco de dados é uma coleção organizada de informações - ou dados - estruturadas, normalmente armazenadas eletronicamente em um sistema de computador. 
- Um banco de dados normalmente é controlado por um gerenciador  de banco de dados (**DBMS** ou **SGDB**)
  - MySQL, PostgreSQL, Microsoft SQL Server (são SGMS)
  - Inserir, excluir, acessar, visualizar, selecionar, ordenar, juntar ou intercalar registros;
  - Copiar e eliminar ficheiros;
  - Alterar estruturas de campos;

## Tipos de Bancos de Dados

- SGBDs relacionais, difundidos e consolidados já há algum tempo;
- E os conhecidos como NoSQL (Not Only SQL). Estes últimos, cada vez mais vem conquistando espaço nas organizações


## Bancos de Dados Relacionais
 - O banco de dados relacional tem como base a utilização de tabelas
 - linhas e colunas que se relacionam
 - **Analogia com Excel**

Exemplos: MySQL, PostgreSQL.

## Bancos de Dados Não Relacionais (NoSQL)
 - tables dao lugar a coleção de dados (mongo)
 - nao gera um relacionamento forte entre os dados

Exemplos: MongoDB (orientado a documentos), Redis (chave-valor), Cassandra (colunas largas)

## Então temos : 

O banco de dados relacional estrutura informações em tabelas inter-relacionadas, como uma rede complexa de conexões, enquanto o não relacional adota abordagens mais flexíveis, permitindo armazenamento de dados de maneira mais livre e descentralizada, como peças autônomas em um tabuleiro.

## Exemplo prático de SQL RELACIONAL

### Cenário: Sistema de Gerenciamento de Pedidos em um E-commerce

Imagine um sistema de gerenciamento de pedidos para um e-commerce, onde você precisa armazenar informações sobre clientes, produtos, pedidos e suas relações.
Estrutura altamente organizada e inter-relacional dos dados.

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


## SQL vs NoSQL

Enquanto o SQL oferece a solidez de um relacionamento estruturado, o NoSQL é flexivel, permitindo que os dados fluam em formas diversas, desafiando as fronteiras tradicionais e se adaptando dinamicamente às demandas modernas de escalabilidade e variedade.


| Característica                   | SQL                         | NoSQL                       |
|-----------------------------------|-----------------------------|-----------------------------|
| **Modelo de Dados**               | Tabelas (relacional)        | Diversos (documentos, grafos, colunas, etc.) |
| **Esquema**                       | Rígido                      | Dinâmico                    |
| **Consistência**                  | ACID (Atomicidade, Consistência, Isolamento, Durabilidade) | BASE (Basic Availability, Soft state, Eventually consistency) |
| **Consultas**                     | Linguagem SQL               | API específica ou consulta simplificada |
| **Escalabilidade**                | Vertical (mais recursos em um único servidor) | Horizontal (distribuição em vários servidores) |
| **Uso Comum**                     | Aplicações tradicionais, sistemas corporativos | Big Data, aplicações web escaláveis, dados não estruturados |
| **Flexibilidade**                 | Menos flexível, estrutura fixa | Mais flexível, adaptável a diferentes tipos de dados |
| **Exemplos de Banco de Dados**    | MySQL, PostgreSQL           | MongoDB, Cassandra, Redis    |


## NewSQL, o banco de dados misto

Aqui, a ideia é pegar o melhor dos bancos de dados relacionais e não relacionais para formar uma ferramenta extremamente prática, segura e funcional.


## Plataformas de Banco de Dados na Nuvem

- Amazon Web Services (AWS)
- Microsoft Azure
- Google Cloud Platform (GCP)

As principais plataformas de nuvem, como AWS, Azure e GCP, oferecem uma variedade de serviços de bancos de dados na nuvem, cada uma com características e diferenciais próprios. Essas soluções permitem armazenar e gerenciar dados de forma eficiente.

## Segurança em Bancos de Dados

- A segurança de dados é crucial para proteger informações sensíveis contra acessos não autorizados, garantindo integridade, confidencialidade e disponibilidade.

- Autenticação e Autorização
- Criptografia
- Backup e Recuperação de Dados
- Estratégias Recomendadas
