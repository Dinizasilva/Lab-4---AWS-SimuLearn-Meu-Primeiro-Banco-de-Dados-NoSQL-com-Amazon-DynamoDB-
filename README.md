# Lab-4-AWS-SimuLearn-Meu-Primeiro-Banco-de-Dados-NoSQL-com-Amazon-DynamoDB-
Hands-on AWS Skill Builder focado em Amazon DynamoDB, modelagem NoSQL, Partition Key, Sort Key e consultas de dados.

<p align="center">
  <img src="./Etapa%201.png" width="500" />
</p>



## Visão Geral

Aqui o foco foi sair um pouco da infraestrutura e entrar em outra parte importante da Cloud: **dados**.
A proposta foi trabalhar com o Amazon DynamoDB, um banco de dados NoSQL totalmente gerenciado da AWS, 

Criando uma tabela, 
Estruturando os itens, 
Inserindo dados e 
Realizando consultas.

O objetivo para mim foi entender como pensar a estrutura de um banco NoSQL e como o DynamoDB organiza e consulta essas informações. 

Plataformas digitais precisam registrar cada detalhe do consumo dos usuários (qual vídeo foi assistido, o momento exato em que parou, preferências de idiomas e os tipos de dispositivos suportados). O grande desafio técnico é fazer isso mantendo alta escalabilidade e performance.


## O problema

Imagine uma plataforma de vídeo que precisa armazenar o histórico de reprodução de seus usuários.
Cada usuário pode assistir a vários vídeos e, para cada reprodução, podemos ter informações como:

* ID do usuário;
* ID do vídeo;
* Data e hora da última reprodução;
* Idioma preferido;
* Dispositivos suportados;
* Avaliação do conteúdo;
* Outras informações relacionadas à experiência daquele usuário.

O desafio é conseguir armazenar e consultar esse histórico de forma rápida e escalável.
É nesse cenário que entra o Amazon DynamoDB.

Em vez de pensar primeiro em tabelas e relacionamentos como fazemos em um banco relacional, no DynamoDB precisamos pensar principalmente em:
Como os dados serão acessados?

Essa foi uma das partes mais importantes que comecei a perceber durante o laboratório.

<p align="center">
  <img src="./Etapa%202.png" width="600" />
</p>


## O desafio do laboratório

O objetivo foi construir uma tabela NoSQL para armazenar o histórico de vídeos assistidos pelos usuários.

Durante o laboratório, precisei:

Entender o funcionamento de um banco NoSQL.
Criar uma tabela no Amazon DynamoDB.
Definir a chave de partição.
Definir a chave de classificação.
Inserir itens na tabela.
Trabalhar com diferentes tipos de atributos.
Realizar consultas utilizando a chave de classificação.
Criar manualmente um novo registro como parte do desafio prático.
Adicionar um atributo numérico de avaliação (rating).
Validar o resultado final do laboratório.


## O que eu precisei entender, compreender e fazer.

Primeiro fui entender como funciona um **Banco NoSQL**.

Durante o laboratório, comecei entendendo que o DynamoDB trabalha de uma forma diferente de um banco de dados relacional. Em vez de pensar primeiro em tabelas e relacionamentos, precisei pensar em como os dados seriam armazenados e principalmente como seriam consultados.

Na prática, aprendi que cada registro é um item e que os dados desse item são organizados por atributos. Também entendi o papel da Partition Key (userId), que identifica e organiza os dados de um usuário, e da Sort Key (lastDateWatched), que permite organizar os registros dentro dessa mesma chave.

Foi fazendo a criação da tabela, inserindo os itens e realizando as consultas que esse conceito começou a fazer sentido para mim. 
Ou seja, não fiquei apenas na teoria: **criei, inseri, consultei e validei os dados no DynamoDB**.


## A tabela utilizada no laboratório foi:

Um dos pontos que mais chamou minha atenção foi perceber que um item do DynamoDB não precisa seguir uma estrutura rígida como uma tabela relacional tradicional.

No laboratório, trabalhei com atributos como:

* userId
* Sort Key
* lastDateWatched
* videoId
* preferredLanguage
* supportedDeviceTypes

e, no desafio prático:
* rating

Também trabalhei com diferentes tipos de dados, incluindo String, Number e List.
Isso ajudou a tornar mais concreto o conceito de estrutura flexível do NoSQL.

Esse ponto foi especialmente importante para entender uma diferença fundamental entre bancos relacionais e NoSQL:
No DynamoDB, a forma como os dados são modelados está diretamente relacionada à forma como eles serão consultados.


## Serviços e tecnologias utilizados
* Amazon DynamoDB
* Banco de dados NoSQL totalmente gerenciado da AWS.

Neste laboratório utilizei o DynamoDB para:

* Criar a tabela;
* Definir as chaves;
* Inserir itens;
* Armazenar diferentes tipos de atributos;
* Consultar os registros;
* Testar filtros utilizando a chave de classificação.

## AWS Skill Builder / SimuLearn
* Ambiente utilizado para realizar o laboratório prático e validar as atividades propostas.


## Partition Key e Sort Key
**Partition Key — userId**

A userId identifica o usuário ao qual aquele registro pertence.
É a chave utilizada para determinar a partição lógica onde os dados serão armazenados.

## Sort Key — lastDateWatched
A lastDateWatched permite organizar os registros dentro da mesma chave de partição.

Assim, podemos pensar no modelo desta maneira:

userId
   │
   ├── lastDateWatched
   │       └── videoId
   │
   ├── lastDateWatched
   │       └── videoId
   │
   └── lastDateWatched
           └── videoId

Ou seja: **um usuário → vários registros de histórico → organizados pela data**.







