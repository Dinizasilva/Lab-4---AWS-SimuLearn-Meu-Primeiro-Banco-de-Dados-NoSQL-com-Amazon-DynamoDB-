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
