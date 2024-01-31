## Servidores

**ANALOGIA FAMOSA NA COMUNIDADE**
Imagine um servidor como um garçom em um restaurante.
Os clientes (outros dispositivos) chegam ao restaurante (rede) e fazem pedidos (solicitações).
O garçom (servidor) recebe esses pedidos, os leva para a cozinha (processa as solicitações) e traz a comida pronta de volta para os clientes.

- Agora, traduzindo para a tecnologia:

**Hardware do servidor**: Seria como o corpo físico do garçom, o lugar onde ele anota os pedidos e entrega a comida.

**Software do servidor**: Seria como a habilidade do garçom para entender os pedidos, organizá-los e garantir que a cozinha (o processamento) faça as coisas corretamente.

Com isso temos que :

O servidor é o cérebro de uma rede.
Um servidor é como um super garçom digital que está sempre pronto para receber pedidos e entregar informações na rede, seja fornecendo páginas web, armazenando arquivos, processando dados, ou realizando outras tarefas, dependendo do tipo de servidor que estamos falando. 


## Tipos de servidores: 

- **Servidor Web**
  - Fornece páginas web
  - Quando você se conecta a um site, está se conectando a um servidor web que envia as páginas para o seu navegador
  - Apache HTTP Server
- **Servidor de Arquivos**
  - Armazena e gerencia arquivos para serem acessados por outros dispositivos.
  - Um servidor de arquivos pode ser usado para compartilhar documentos ou mídia em uma rede.
  - Servidor de arquivos do Windows ou Samba
- **Servidor de Banco de Dados**
  - Armazena e gerencia dados, permitindo a recuperação eficiente de informações.
  - basicamente nosso ponto forte como programadores
  - MySQL, PostgreSQL ou Microsoft SQL Server
- **Servidor de Email**
  - Gerencia e distribui emails
  - envio e recebimento de email
  - Microsoft Exchange Server ou Postfix
- **Servidor DNS**
  - Traduz nomes de domínio em endereços IP.
  - digitar nome do site
  - BIND (Berkeley Internet Name Domain) ou Microsoft DNS
- **Servidor Proxy**
  - Age como intermediário entre os usuários e outros servidores, melhorando desempenho e segurança.
  - Pode ser usado para acessar conteúdo da web de forma mais rápida ou proteger a identidade do usuário.
  - Squid

## Hospedagem 

### O que é a hospedagem ?

é um serviço online que permite que o conteúdo do seu site fique acessível na internet.

Quando você hospeda um site, você está colocando o seu site em um servidor que provavelmente está em uma máquina fisica. SEMPRE.
Que está sempre ligada e acessivel a qualquer momento

### Consigo hospedar meu site sozinho ?

Sim, porém requer equipapmento e muito conhecimento técnico. A auto-hospedagem envolve a instalação e configuração de um servidor web a partir do zero

### Como Funciona um Servidor Web 

## RELEMBRAR O HTTP

- **Pedido (Request)**: Quando você digita um URL no seu navegador e pressiona Enter, você está fazendo um pedido ao servidor. Isso é chamado de solicitação (request). É como pedir ao servidor para mostrar uma página específica.

- **Resposta (Response)**: O servidor recebe sua solicitação e responde com a página web correspondente. Isso é chamado de resposta (response). O navegador então exibe essa resposta para você.

### Por que o HTTP é importante ?

- **Privacidade**: Garante que suas informações pessoais (senhas, dados de cartão) sejam transmitidas de forma segura.

- **Integridade**: Evita que dados sejam alterados no caminho entre o navegador e o servidor.

- **Autenticidade**: Certifica que o site é realmente quem diz ser.

## Introdução aos Contêineres

### O que são containers

Contêineres são como caixas que empacotam não apenas sua aplicação, mas também todas as coisas necessárias para ela funcionar - como bibliotecas, dependências e configurações. Essa caixa é isolada do resto, garantindo que o que está dentro funcione consistentemente, independentemente do ambiente externo.

### Como os containers funcionam ? 
  - **Metáfora**: Semelhante a uma caixa que contém tudo que você precisa para montar um LEGO.
  - **Explicação**: Os contêineres incluem a aplicação e todas as peças necessárias para ela, como bibliotecas e configurações. Isso facilita a movimentação da aplicação entre diferentes ambientes, como do seu laptop para um servidor de produção, sem se preocupar com as diferenças no ambiente.

### Principais vantagens
- isolamento: os containers garantem que as aplicações e suas dependencias fiquem isoladas
- consistência: os containers garantem que a aplicação funcione da mesma forma em diferentes ambientes
- eficiencia: os containers economizam recursos ja que compartilham o sistema operacional subjacente

### Docker: Uma Ferramenta de Contêinerização

Docker é um software de **código aberto** usado para implantar aplicativos dentro de containers virtuais.

A conteinerização permite que vários aplicativos funcionem em diferentes ambientes complexos.


### Provedores de Serviços em Nuvem

#### AWS (Amazon Web Services)

Principais Serviços:

- EC2 (Elastic Compute Cloud): Permite criar instâncias virtuais escaláveis para execução de aplicativos.
- S3 (Simple Storage Service): Oferece armazenamento de objetos escalável e durável.
- RDS (Relational Database Service): Gerencia bancos de dados relacionais, como MySQL, PostgreSQL, Oracle, e outros.

#### Azure

Tal como a AWS oferece diversos serviços de computação em núvem e a principal diferença é que a Azure é quase uma
queridinha da Microsoft e se integra muitoo bem com eles. A AWS tmb porém é conhecida mesmo por sua variedade de produtos
