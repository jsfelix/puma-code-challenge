# Code challenge PUMA

## Instruções básicas

Você foi encarregado de construir um aplicativo web para a criação de uma lista
de usuários favoritos do GitHub.

Para isso, deverá ser utilizada a API oficial do GitHub (https://api.github.com)
cuja documentação se encontra em https://docs.github.com/pt/rest

A aplicação consistirá em um **backend**, que será responsável pelas requisições à
API do GitHub e persistência dos dados em memória, e um **frontend** para exibição e 
gerenciamento da lista de favoritos.

A linguagem de programação deverá ser Javascript. Utilize Node.js e um
framework como Express.js ou Fastify para o backend, e React, Angular ou Vue.js
para o frontend.

## Backend

O backend de sua aplicação consistirá nas seguintes rotas:

```
POST /users: adicionar um usuário à lista de favoritos (username, nome, avatar e url)

GET /users: listagem dos usuários favoritos salvos em memória

DELETE /users/{username}: remover um usuário da lista de favoritos

PATCH /users/{username}/toggle-star: marca/desmarca um usuário da lista de favoritos com 
uma estrela - essa rota deverá funcionar como uma chave (toggle), alternando entre 
liga/desliga a estrela do usuário

```

Regras de negócio:

- O utilizador poderá adicionar o máximo de 5 usuários favoritos;
- O utilizador não poderá adicionar um usuário que já foi adicionado na lista;
- Somente 1 usuário pode ser marcado com uma estrela. Se o utilizador tentar
  marcar um segundo usuário com uma estrela, o usuário anteriormente marcado
  deixará de ter a estrela;
- O utilizador poderá ordenar a lista de usuários em ordem alfabética de nome.

## Frontend

A aplicação web consistirá de uma entrada de texto onde o utilizador deverá
digitar o username do GitHub que deseja adicionar à lista de favoritos, um botão 
de adicionar e um grid contendo os cards dos usuários favoritos adicionados.

Ao clicar no botão adicionar, o usuário do GitHub escolhido deverá ser
adicionado à lista, que consistirá de cards contendo foto, nome do usuário e
username. O card deverá ter um link para a página do usuário no github.

Para cada usuário adicionado deverá existir um botão de excluir, e outro botão
de estrela.

Acrescentar um botão para ordenar a lista em ordem alfabética de nome.

## Observações

- Caso o usuário tente inserir um username que não existe no GitHub, uma
  mensagem de erro deve ser exibida;
- Exibir mensagem de erro caso o usuário tente adicionar um novo username quando
  o limite de favoritos tiver sido alcançado;
- Não é necessário salvar a lista de favoritos em banco dados, podendo ficar
  somente em memória;
- Utilizar testes unitários no backend;
- Utilizar os princípios de programação orientada a objetos, design patterns e
  arquitetura limpa quando apropriado.
- Crie um arquivo README.md contendo uma explicação resumida de como implementou
  sua aplicação, quais frameworks utilizou, bem como instruções de como executar
  sua aplicação.
  
## Forma e prazo de entrega do desafio

Para entregar o código, o candidato deverá subir em um repositório público em sua conta
do GitHub (caso não tenha uma conta, crie uma em https://github.com/signup) e enviar o
link do repositório para #####@######.

O prazo de entrega é de **24 horas, contadas a partir do término da entrevista técnica**. 
Caso não seja entregue no prazo, estará automaticamente eliminado do processo seletivo.

## Critérios de avaliação

Será avaliado do candidato:
- A capacidade de interpretação das regras de negócio e a resolução lógica do problema
apresentado;
- A clareza e organização do código;
- O conhecimento nos frameworks escolhidos para o desenvolvimento;
- A utilização de testes unitários automatizados.


Boa sorte!
