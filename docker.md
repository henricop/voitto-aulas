## Introdução ao Docker

- O que é Docker?

**Docker é uma plataforma de código aberto que permite que você crie, distribua e execute aplicativos em contêineres** <!-- (já ja entraremos no conceito de container).  -->

- Por que usar Docker?
O Docker **garante que um aplicativo seja executado da mesma maneira em diferentes ambientes, como desenvolvimento, teste e produção** <!--Só com isso vemos a praticidade-->


## Conceitos Básicos

- Containerização

Um contêiner é uma **unidade leve e portátil que empacota todo o software necessário para executar um aplicativo**, incluindo bibliotecas, dependências e código, em um único pacote.

- Imagens e Containers:

Uma **imagem Docker** é um pacote leve, independente e executável que contém todo o necessário para executar uma aplicação: código, runtime, bibliotecas, variáveis de ambiente e configurações.

**Pense em uma imagem como uma receita ou um modelo para criar containers.**

**IMPORTANTE**: A imagem é contruidas a partir do arquivo DOCKETFILE

Vantagens da utilização de containers em comparação com máquinas virtuais tradicionais.

## Arquitetura do Docker

- Docker Engine: Explique o papel do Docker Engine na criação e execução de containers.
- Docker Daemon e Docker Client: Como o Docker Daemon e o Docker Client interagem para gerenciar os containers.
- Docker Registry: Introdução aos repositórios de imagens Docker, como Docker Hub e Docker Store.

## Principais Comandos

- docker pull: Baixar imagens do Docker Hub.
- docker run: Criar e executar um container a partir de uma imagem.
- docker ps: Listar containers em execução.
- docker stop e docker rm: Parar e remover containers.
- docker images: Listar imagens baixadas.
- docker rmi: Remover imagens.


## Networking no Docker

- Comunicação entre containers.
- Exposição de portas para acesso externo.
- Criação de redes personalizadas para comunicação entre containers.

## Persistência de Dados

- Montagem de volumes: Como persistir dados em containers.
- Uso de volumes para compartilhar dados entre o host e o container.

## Orquestração de Containers (Breve Introdução)

Breve explicação sobre orquestradores de containers, como Kubernetes e Docker Swarm.
Importância da orquestração para gerenciar e escalar aplicativos em contêineres em ambientes de produção.

## Conclusão

- Recapitulação dos conceitos-chave abordados.
- Sugestões para recursos adicionais de aprendizado.
- Encorajamento para explorar e experimentar com Docker.

## Perguntas e Respostas
- Espaço para responder perguntas dos alunos e esclarecer dúvidas adicionais.