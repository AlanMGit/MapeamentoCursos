# 1933 A - Parte 1: Domínio

## Aula 1 - Modelando o domínio
00:14:45 Separando validações em um projeto separado (Commom ou Shared)  
00:15:00 Utilizacao de AssertionConcern  
00:24:30 Utilizacao de resources para erros  

## Aula 2 - Repository Pattern 
00:29:00 Criação de índice único no mapeamento do EF
00:30:40 Explicação sobre como funciona a criação dos dbsets
00:43:00 Migrations

## Aula 3 - Injeção de dependências 
00:01:55 Melhor explicação sobre injeção de dependencias
00:11:25 Lugar onde iremos trocar os repositórios caso haja mudança de banco de dados

## Aula 4 - Services 
 Foi o módulo que mais deu noção sobre por que implementar uma camada Serviços  
00:04:00 Por que levar alguns métodos que existem na camada Domínio para a camada Serviços  
Basicamente é o módulo onde fica todo o fluxo de realização para cada operação. Por exemplo: para cadastrar um usuário você precisar  verificar se o e-mail já existe na tabela, ver se a senha é igual a confirmação de senha e verificar se a senha é válida, todos esses três  passos são métodos separados da camada de domínio, porém na camada de domínio ficaria dentro de um método Criar que conteria todos esses  três passos.  
Caso esses passos fossem feito fora da camada de serviço, por exemplo no controller, iríamos precisar reescrevê-los no controller de cada  projeto: Api, MVC, Mobile e no corpo do programa da Console Application.

## Aula 5 - Consumindo os Services
Este módulo mostra como usar a camada de serviços em 3 diferentes projetos: Api, MVC e Console Application  
00:02:30 Como utilizar globalização para mensagens de erros
00:11:25 ModelState é o dicionário de erros padrão do ASP.Net MVC
00:12:06 Refletindo a mensagem de erro do dicionário ModelState na view


# 1933 B - Parte 2 - API 

## Aula 1 - Iniciando a API 
00:03:50 Instalar o Owin (redução de referências)
00:06:00 CORS serve para quando iremos publicar nossa API em um servidor e a interface em outro servidor
  Permitir implantar até por Controller
	
## Aula 2 - Autenticação em serviços 
Utilizando o OAuth (sem Identity)

Para complemento dessa vídeo aula, assisti dois vídeos no youtube:

### Autenticação em Serviços - Parte 1 : Backend
 Explicação do fluxo de funcionamento da autenticação no ASP.Net
	05:00 Instalação dos pacotes necessários
 Uma maneira de saber se o usuário está vinculado a uma unidade é adicionar uma claim ao mesmo com a unidade e na hora de obtermos os dados  passamos o conteúdo desta claim como parâmetro nos filtros

### Autenticação em Serviços - Parte 2 : Frontend ********** 
 00:02:00 Fazendo a requisição para obter o token
 00:04:45 Onde armazenar o token gerado em uma aplicação ASP.Net MVC
 00:09:30 Quando não for uma aplicação ASP.Net MVC, podemos armazenar no localstorage ou no cookie
 00:17:30 Angular Js

## Aula 3 - Criando o endpoint 
00:05:50 Utilização de ViewModels para registrar usuário
00:06:50 ModelStatel.IsValid não funciona no WebApi
00:17:00 Como trabalhar com dois métodos post em um mesmo Controller
  Através do atributo Route
00:22:00 Padronizando o retorno com HttpResponseMessages

## Aula 4 - Performance e Padronização 
00:04:00 Task
00:06:20 Remover XML  
  Identação Json
00:09:00 Preservando a referência de objetos aninhados em JSON
00:16:40 Compressão

# 1933 C - Parte 3 - Infraestrutura

## Aula 1 - Publicando a API
