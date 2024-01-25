## O que é um framework ?
- É uma estrutura-base que contem um conjunto de funções e componentes pre-definidos. Essas funções e components se relacionam para disponibilizar
 funcionalidades especificas no desenvolvimento de sofware. Todos são genéricos e pré-prontos e basicamente servem para agilizar o seu tempo e evitar
 re-trabalho

- possuem um fluxo de trabalho a ser seguido

Exemplos: Next, Angular, Vue, Ionic, Django, CherryPy

## O que é uma biblioteca ?

Também é um conjunto base de código que tende a fornecer funcionalidade prática para resolver alguns problemas. É muito menos amplo que o Framework e bem mais específica.

exemplos: Moment (lib de datas) | React (lib de interfaces) | Pandas | Numpy | Matplotlib

## Qual a diferença entre Framework e Biblioteca ?

Polemico ! 

Mas é facil pensar da seguinte forma : 

Na grande maioria dos casos o Framework tende a USAR o nosso código, ou seja, ele ja tem uma estrutura pronta e a gente aplica.
As bibliotecas tendem a ser utilizadas em nosso código.

Acredito que esse seja o maior dos gatilhos ! 

Porém é facil cair em erros, por exemplo: O Angular muitas vezes é chamado de Biblioteca, sendo que ele é e se autodenomina um FRAMEWORK ROBUSTO.

O mesmo acontece com React (que é até polêmico), ele se denomina uma biblioteca, mas devido o ecossistema ter crescido TANTO, muita gente o considera um framework

---























## Exemplo prático com Python

### Biblioteca: **Requests**

A biblioteca **Requests** simplifica o processo de fazer requisições HTTP. Oferece métodos e funções que você pode chamar para enviar solicitações HTTP e maniputar os retornos.

```python

import requests

response = requests.get("https://api.adviceslip.com/advice")
print(response.status_code)
print(response.json())

```
Percebemos que a biblioteca **Requests** oferece funcionalidades específicas mas não dita como o seu programa deve ser estruturado.



### Framework: **Django**

O **Django** é um framework web em python que segue a filosofia de bateria inclusa e fornece uma estrutura muito mais abrangente para o desenvolvimento web.

Ela não simplesmente fornece recursos para a manipulação de requisições **HTTP** como também define uma arquitetura **MVP**

```python
from django.http import HttpResponse

def my_view(request):
  request HttpResponse("Hello, World!!")
```

Percebemos aqui que o **Framework Django** não fornece apenas funcionalidades para a manipulação de solicitações **HTTP** mas também define uma estrutura mais abrangente para o desenvolvimento



