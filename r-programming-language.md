![Alt text](image.png)

# Python vs. R: Qual é Melhor Para Ciência de Dados?

- Vantagens e desvantagens de usar Python e R para ciência de dados.

## Python e  R na Ciência de Dados

As linguagens de programação Python e R são amplamente utilizadas no campo da ciência de dados. Ambas têm suas características únicas e oferecem recursos poderosos para o processamento e análise de dados.

### Python

- versátil, simples e legível
- comunidade enorme
- grande variedade de bibliotecas
- Curva de aprendizado facilitada

### R

- específico análise estatística e visualização de dados
- ferramentas estatísticas e gráficas.
- ambientes acadêmicos
- Pacotes estatísticos avançados
- Curva de aprendizado complexa


## Python x R

São semelhantes mas precisamos destacar alguns pontos:

1. Sintaxe (Python é muito mais simples que o R)

**Cálculo da média de uma lista de números**:

```python
# Python
numbers = [10, 20, 30, 40, 50]
mean = sum(numbers) / len(numbers)
print("Média dos números:", mean)

```
---
```r
# R
numbers <- c(10, 20, 30, 40, 50)
mean <- mean(numbers)
print(paste("Média dos números:", mean))

```


2. Python é muito robusto para a ciencia de dados porém o R é focado em análise estatística
  - para o fullstack o python é ideal justamente pela possibilidade de mais abrangência
3. Os graficos de visualização de dados do R são muito detalhados mas não é nada que com um pouco mais de código a gente não consiga fazer
4. Python é fundamentalmente mais rápido que R (mais rápido que a maioria das linguagens) principalmente lidando com bigdata
5. Integração do python é muito melhor em tudo (com outras linguagens para sistemas complexos,  desenvolvimento web, automação e diversos outros serviços), já o R é voltado  para análise estatística e visualização de dados

## Tabela comparativa: 

|                       | Python                                           | R                                               |
|-----------------------|--------------------------------------------------|-------------------------------------------------|
| Data de criação       | 1991                                             | 1995                                            |
| Versão atual          | 3.6.4                                            | 3.4.4                                           |
|                       | (lançada em 13/09/2015)                          | (lançada em 10/12/2015)                        |
| Origem                | Python foi inspirada na linguagem C, Modula-3 e ABC. | R foi uma implementação da linguagem S da Bell Labs. |
| Usabilidade           | Codificação e Debugging é mais fácil, pois a sintaxe é bem simples. | Modelos estatísticos podem ser escritos com poucas linhas de código. |
| Padronização          | Python possui um padrão mais bem definido, permitindo que diferentes tipos de funcionalidades sejam escritos da mesma forma. | A mesma funcionalidade pode ser escrita de diversas formas diferentes em R. |
| Flexibilidade         | Python é bastante flexível e permite facilmente escrever algo a partir do zero. | É fácil escrever formulas complexas em R. Praticamente todos os tipos de testes e modelos estatísticos estão disponíveis para uso na linguagem. |
| Repositórios          | PyPi é o repositório de Python, com diversas bibliotecas. Usuários podem contribuir com novos pacotes. | CRAN (Comprehensive R Archive Network) é o repositório da linguagem R em que cada usuário pode contribuir com novos pacotes (que são coleções de funções em R com código compilado). Esses pacotes podem ser facilmente instalados com uma linha de código. |
| Usando as duas linguagens juntas | Use a biblioteca RPy2 para executar código R dentro do Python. Ele provê uma interface entre as linguagens. | Use o pacote rPython para executar pacotes do Python dentro do código R. É possível passar e receber dados de Python, chamar funções ou métodos. |
| Uso em Análise de Dados | Python é principalmente usada quando a análise de dados precisa ser integrada com aplicativos web ou se o código estatístico precisa ser integrado em um servidor em ambiente de produção, que vai servir muitos usuários. | R é principalmente usada quando as atividades de análise de dados requerem computação standalone (em um único computador) ou análise em servidores individuais. |
| Tratamento de dados   | Python não foi criada inicialmente para análise de dados, mas a linguagem tem crescido rapidamente e cada vez oferece mais recursos. | R é extremamente eficiente em análise de dados, devido seu grande número de pacotes com modelos, fórmulas e testes estatísticos. |
| IDE                   | Python IDE, Spyder e IPython Notebook           | RStudio                                         |
| Pacotes mais populares| - SciPy / NumPy (computação científica)        | - dplyr, plyr e data.table (manipulação de dados) |
|                       | - Pandas (manipulação de dados)                 | - stringr (manipulação de strings)              |
|                       | - Matplotlib (gráficos)                         | - zoo (time-series)                            |
|                       | - Scikit-learn (Machine Learning)               | - ggvis, lattice e ggplot2 (gráficos)          |
|                       |                                                  | - caret (Machine Learning)                      |
| Pontos positivos      | - Python é ótima para criação de scripts e automatização de regras para mineração de dados. | - R é ótimo para prototipagem e para análise estatística. |
|                       | - Se integra facilmente em um fluxo de trabalho de produção de desenvolvimento. | - R tem um enorme conjunto de bibliotecas disponíveis para análise de diferentes tipos de estatística. |
|                       | - Pode ser usada em diferentes partes no processo de desenvolvimento de software (back-end, front-end) | - Rstudio IDE é definitivamente uma grande vantagem. Ele facilita a maioria das tarefas tediosas e facilita o fluxo de trabalho. |
|                       | - IPython Notebook é uma poderosa ferramenta para análise exploratória e apresentações. |                                                     |
| Pontos Negativos      | - Não é tão completo para análise estatística como R, mas já percorreu um longo caminho nestes últimos anos. | - A sintaxe pode ser obscura, às vezes.        |
|                       | - Na minha opinião, a curva de aprendizado é mais acentuada do que R, por se tratar de uma linguagem muito mais completa. | - É mais difícil de integrar a um fluxo de desenvolvimento de produção. |
|                       |                                                  | - Na minha opinião, é mais adequado para tarefas do tipo “consultoria”. |
| Propósito             | - Python é uma linguagem de uso geral, com características inerentes a outras linguagens de programação de computadores. Isso permite que pessoas com diferentes backgrounds possam utilizar a linguagem. | - R foi desenvolvida por estatísticos, para estatísticos. Engenheiros, cientistas e estatísticos sem conhecimento de programação de computadores, consideram R fácil de usar. |
| Velocidade            | - Python é considerada uma das linguagens de programação mais velozes atualmente. | - R foi desenvolvida para fazer análise de dados, não para ser rápida. Entretanto, o código pode ser otimizado. O problema, é que a linguagem é bastante utilizada por quem não possui conhecimentos de programação, tornando o código mais lento do que deveria. |



