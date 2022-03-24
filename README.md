# apim-arqt-refe-movie-v1

Versão Inicial por:
  < Name and/or Discord nic or None >

Demais Contribuições:
  < Name and/or Discord nic or None >

Criado em:
  < dd-mm-yyyy>

## Descrição
(1 parágrafo) O que estamos fazendo e por quê? Que problema você está tentando
resolver? Quais são as metas e NÃO-metas? Por favor, faça o objetivo
compreensível para alguém não familiarizado com este projeto, incluindo o
contexto necessário, mas mantenha-o curto. Elabore os detalhes abaixo no
Seções de antecedentes e requisitos.

## Conceitos e Referências
(1-2 parágrafos) Que conceitos são necessários para o entendimento? Tente usar links ou referências para
fontes externas (outros documentos ou da web), em vez de escrever seus próprios
explicações. Nota: Descrição conceitual; não escreva sobre seu projeto, detalhes de requisitos específicos 
ou ideias para resolver problemas aqui.

## Requisitos
(2-5 parágrafos) Quais são as restrições para o problema que você está tentando resolver?
Quem são os usuários desta solução? O que é necessário para ser produzido?
Qual é o alcance desse esforço? Seu trabalho aqui é educar rapidamente os outros
sobre os detalhes que você conhece sobre o espaço do problema, para que eles possam ajudar a revisar
sua implementação. Estimar aproximadamente os detalhes relevantes. Qual o tamanho dos dados?
Quais são as taxas de transação? Largura de banda?

## Proposta para Solução
(2-5 parágrafos) Uma visão geral curta e agradável de suas ideias de implementação. Se
você tem soluções alternativas para um problema, liste-as concisamente em um marcador
Lista. Isso não deve conter todos os detalhes de sua implementação e não
não inclui código. Use um diagrama quando necessário. Cobrir as principais estruturas
elementos de uma forma muito sucinta. Quais tecnologias você usará? O que
novos componentes você vai escrever? Quais tecnologias você usará para escrevê-los?

## Design da Especificação de Referência

# Movies API

This is an API Blueprint example describing a movies API.

### [GET] List all Movies [/v1/movies]

List movies in order of publication.

#### Parameters

| Parameter            | Type      | Description Content             |
| :------------------  | :-------- | :---------------------------    |
| limit                | `query`   | return max 100                  |

#### Response Content

| Name             | Element       | Type       | Required | Description                      |
| :-------------   | :---------    | :--------- | :--------| :------------------------------  |
| `Next link`      | `x-next`      | `header`   | `true`   |  description xxx.                |
| `Movies List`    | `Movies`      | `array`    | `true`   |  description xxx.                |


### [POST] Insert a New Movie [/v1/movies]

Insert a new Movie.

#### RequestBody (Payload) Elements:

| Name             | Element       | Type       | Required | Description                      |
| :-------------   | :---------    | :--------- | :--------| :------------------------------  |
| `Movie Object`   | `Movie`       | `object`   | `true`   |  description xxx.                |

#### Response Content
- No Content
Status Code <201 - Created>


### [GET] List a specific Movie by id [/v1/movies/{movieId}]

Info for a specific movie.

| Parameter            | Type             | Description Content             |
| :------------------  | :--------------- | :---------------------------    |
| movieId              | `path parameter` | Movie ID Value                  |

#### Response Content

| Name             | Element       | Type       | Required | Description                      |
| :-------------   | :---------    | :--------- | :--------| :------------------------------  |
| `Movie Object`   | `Movie`       | `object`   | `true`   |  description xxx.                |


### [PUT] Update a specific Movie by id [/v1/movies/{movieId}]

Info for a specific movie.

| Parameter            | Type             | Description Content             |
| :------------------  | :--------------- | :---------------------------    |
| movieId              | `path parameter` | Movie ID Value                  |

#### Response Content
- No Content
Status Code <204 - Accepted>


## Definições de Schema 

## Movie Object

| Name             | Element       | Type       | Required | Description                      |
| :-------------   | :---------    | :--------- | :--------| :------------------------------  |
| `Movie ID`       | `id`          | `string`   | `true`   |  description xxx.                |
| `Movie Title`    | `title`       | `string`   | `true`   |  description xxx.                |
| `Movie Category` | `category`    | `string`   | `false`  |  description xxx.                |
| `Movie Duration` | `duration`    | `integer`  | `false`  |  description xxx.                |
| `Release Date`   | `releaseDate` | `date`     | `true`   |  description xxx.                |

## Movie Array

| Name             | Element       | Type       | Required | Description                      |
| :-------------   | :---------    | :--------- | :--------| :------------------------------  |
| `Movie Object`   | `Movie`       | `Movie`    | `true`   |  description xxx.                |


### SecuritySchemes e Error Object deve ser o mesmo padrão de todas as APIs do Projeto
Link: <add ref de documentação do repositório oficial>

## Impactos
Impacto da API? Impacto na segurança? Impacto da documentação? Impacto no desempenho?
Impacto do desenvolvedor? Impacto da capacidade de atualização?


##### Apoio ao Desenvolvimento de um aquivo YAML de uma Open API Specification 3.0.3 (OAS 3.0.3)

Utilizar o Template `spec-arqt-ref-movie-v1.yaml`.

Para demais dúvidas de desenvolvimento de uma OAS 3.0.3, é sugerido utilizar a documentação de referência da Open API Initiative:
https://github.com/OAI/OpenAPI-Specification/blob/main/versions/3.0.3.md

