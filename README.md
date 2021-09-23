### Informações Gerais

Projeto desenvolvido durante formação em desenvolvedor Web Full Stack pela Trybe.

---

# Boas vindas ao repositório do projeto de MongoDB Commerce!

Neste projeto foi praticado os conceitos de update de **MongoDB** utilizando o banco de dados `commerce`, que contém dados do cardápio do **McDonald's**, como ingredientes, valores nutricionais e dados fictícios de vendas.

Lembrando que esta aplicação corresponde aos meus esforços para melhorar minhas hard skills e soft skills, sinta-se à vontade para explorá-la! Feedbacks construtivos são sempre bem vindos!

Abaixo você poderá encontrar mais informações técnicas sobre este projeto.

---

# Sumário

- [Habilidades](#habilidades)
- [Intruções para fazer o fork do repositório](#intruções-para-fazer-o-fork-do-repositório)
- [Informações do projeto](#informações-do-projeto)
  - [Linter](#linter)
  - [Instruções para restaurar o banco de dados commerce](#instruções-para-restaurar-o-banco-de-dados-commerce)
  - [Implementações técnicas](#implementações-técnicas)
- [Desafios](#desafios)
  - [Desafio 1](#desafio-1)
  - [Desafio 2](#desafio-2)
  - [Desafio 3](#desafio-3)
  - [Desafio 4](#desafio-4)
  - [Desafio 5](#desafio-5)
  - [Desafio 6](#desafio-6)
  - [Desafio 7](#desafio-7)
  - [Desafio 8](#desafio-8)
  - [Desafio 9](#desafio-9)
  - [Desafio 10](#desafio-10)
  - [Desafio 11](#desafio-11)
  - [Desafio 12](#desafio-12)
  - [Desafio 13](#desafio-13)
  - [Desafio 14](#desafio-14)
  - [Desafio 15](#desafio-15)
  - [Desafio 16](#desafio-16)
  - [Desafio 17](#desafio-17)
  - [Desafio 18](#desafio-18)
  - [Desafio 19](#desafio-19)
  - [Desafio 20](#desafio-20)
  - [Desafio 21](#desafio-21)
  - [Desafio 22](#desafio-22)

---

# Habilidades

Nesse projeto, fui capaz de:

  * Utilizar o método `updateOne()` e `updateMany()`
  * Utilizar os operadores `$set`, `$mul`, `$inc`, `$min`, `$max` e `$currentDate`
  * Renomear campos e remover campos
  * Incorporar dados aos documentos através de arrays
  * Utilizar os operadores `$pop`, `$pull` e `$push`
  * Utilizar o operador `$addToSet`
  * Utilizar os operadores `$each`, `$slice` e `$sort`
  * Utilizar o operador `$all` para filtrar documentos
  * Utilizar o operador `$elemMatch` para filtrar documentos
  * Utilizar o operador `$size` para filtrar documentos pelo tamanho de arrays
  * Utilizar o operador `$expr` para criar expressões de agregação
  * Utilizar expressões regulares e o operador `$regex` para buscar documentos
  * Utilizar o índice textual e o operador `$text`
  * Utilizar o operador `$mod`

---

# Instruções para fazer o fork do repositório

1. Faça o fork do repositório

2. Instale as dependências do projeto
  * Instale as dependências:
    * `npm install`

---

# Informações do projeto

### Linter

Para garantir a qualidade do código de forma a tê-lo mais legível, de mais fácil manutenção e seguindo as boas práticas de desenvolvimento foi utilizado neste projeto o linter `ESLint`.

### Instruções para restaurar o banco de dados `commerce`

1. Abra o terminal e conecte-se à sua instância local do **MongoDB**.

2. Agora que você tem certeza de que a sua instância está no ar e que você está conectado a ela, digite `exit`. Você voltará ao terminal para iniciar a importação dos dados.

3. Na raiz do diretório do projeto, execute o seguinte comando que fará a restauração da base de dados `commerce`:
   ```sh
   DBNAME=commerce ./scripts/resetdb.sh assets/produtos
   ```

- A execução desse script criará um banco de dados chamado `commerce` e importará os dados para a coleção `produtos`.

---

### Implementações técnicas

Para executar localmente os testes, é preciso escrever o seguinte no seu terminal, estando na raiz do diretório do projeto:

```sh
./scripts/evaluate.sh
```

Esse script passará por **todos os desafios** e imprimirá um relatório indicando se passou ou não para cada desafio. Como a execução do script **envolve restauração da base de dados `commerce`** de um teste para outro, recomenda-se esperar pela sua execução completa.

Para executar somente o teste de um desafio, execute o comando abaixo, substituindo N pelo númedo do desafio

```sh
./scripts/evaluate.sh desafioN
```

⚠️ Como na avaliação o banco de dados `commerce` é restaurado de um teste para outro, **se atente a fazer uso do banco restaurado na hora de fazer um desafio**. ⚠️

---

# Desafios

### Desafio 1 

Inclua o campo `criadoPor` em todos os documentos, colocando `"Ronald McDonald"` no valor desse campo.

Para isso, escreva no arquivo `desafio1.js` duas queries, **nesta ordem**:

1. Crie uma query que adicione o campo `criadoPor` em todos os documentos, colocando `"Ronald McDonald"` no valor desse campo.

2. Crie uma query que retorne o `nome` e `criadoPor` de todos os produtos.

### Desafio 2 

Inclua o campo `valorUnitario` em todos os documentos em que esse campo não existe e atribua a ele o valor `"0.00"`, com o tipo `NumberDecimal`.

Para isso, escreva no arquivo `desafio2.js` duas queries, **nesta ordem**:

1. Crie uma query que adicione o campo `valorUnitario` em todos os documentos em que esse campo não existe e atribua a ele o valor `"0.00"`, com o tipo `NumberDecimal`.

2. Crie uma query que retorne o `nome` e `valorUnitario` de todos os produtos.

### Desafio 3 

Adicione o campo `avaliacao` em todos os documentos da coleção e efetue alterações nesse campo.

Para isso, escreva no arquivo `desafio3.js` quatro queries, **nesta ordem**:

1. Crie uma query que inclua o campo `avaliacao` do tipo `NumberInt` e com o valor `0` em todos os documentos da coleção.

2. Crie uma query que incremente o valor do campo `avaliacao` em `5` em todos os sanduíches de carne do tipo `bovino`. Dica: utilize como filtro o campo `tags`.

3. Crie uma query que incremente o valor do campo `avaliacao` em `3` em todos os sanduíches de `ave`.

4. Crie uma query que retorne o `nome` e `avaliacao` de todos os sanduíches.

### Desafio 4 

Atribua a data corrente ao campo `ultimaModificacao` no sanduíche `Big Mac`.

Para isso, escreva no arquivo `desafio4.js` duas queries, **nesta ordem**:

1. Crie uma query que atribua a data corrente ao campo `ultimaModificacao` no sanduíche `Big Mac`. Para a data corrente faça uso do tipo `Date`.

2. Crie uma query que retorne o `nome` de todos os documentos em que o campo `ultimaModificacao` existe.

### Desafio 5 

Adicione `ketchup` aos `ingredientes` para todos os sanduíches menos o `McChicken`, garantindo que não haja duplicidade nos `ingredientes`.

Para isso, escreva no arquivo `desafio5.js` duas queries, **nesta ordem**:

1. Crie uma query que adicione `ketchup` aos `ingredientes` para todos os sanduíches menos o `McChicken`, garantindo que não haja duplicidade nos `ingredientes`.

2. Crie uma query que retorne o `nome` e `ingredientes` de todos os documentos.

### Desafio 6 

Inclua `bacon` no final da lista de `ingredientes` dos sanduíches `Big Mac` e `Quarteirão com Queijo`.

Para isso, escreva no arquivo `desafio6.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a inclusão de `bacon` no final da lista de `ingredientes` dos sanduíches `Big Mac` e `Quarteirão com Queijo`.

2. Crie uma query que retorne o `nome` e `ingredientes` de todos os documentos.

### Desafio 7 

Remova o item `cebola` de todos os sanduíches.

Para isso, escreva no arquivo `desafio7.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a remoção do item `cebola` em todos os sanduíches.

2. Crie uma query que retorne o `nome` e `ingredientes` de todos os documentos.

### Desafio 8 

Remova o **primeiro** `ingrediente` do sanduíche `Quarteirão com Queijo`.

Para isso, escreva no arquivo `desafio8.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a remoção do **primeiro** `ingrediente` no sanduíche `Quarteirão com Queijo`.

2. Crie uma query que retorne o `nome` e `ingredientes` de todos os documentos.

### Desafio 9 

Remova o **último** `ingrediente` do sanduíche `Cheddar McMelt`.

Para isso, escreva no arquivo `desafio9.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a remoção do **último** `ingrediente` no sanduíche `Cheddar McMelt`.

2. Crie uma query que retorne o `nome` e `ingredientes` de todos os documentos.

### Desafio 10

Adicione a quantidade de vendas dos sanduíches por dia da semana.

Para isso, escreva no arquivo `desafio10.js` quatro queries, **nesta ordem**:

1. Crie uma query que inclua um _array_ com sete posições em todos os sanduíches. Cada uma delas representará um dia da semana, e cada posição iniciará em `0`. O _array_ deve se parecer como abaixo:
   ```json
   "vendasPorDia": [0, 0, 0, 0, 0, 0, 0]
   ```

- O primeiro item desse _array_ representa as vendas no **domingo**, o segundo item representa as vendas na **segunda-feira**, e assim até chegar ao último item, que representa as vendas no **sábado**.

2. Crie uma query que incremente as vendas de `Big Mac` às **quartas-feiras** em `60`.

3. Crie uma query que incremente as vendas de todos os sanduíches de carne do tipo `bovino` e `pão` aos **sábados** em `120`.

4. Crie uma query que retorne o `nome` e `vendasPorDia` de todos os documentos.

### Desafio 11

Insira os elementos `combo` e `tasty` no _array_ `tags` de todos os sanduíches e aproveite para deixar os elementos em ordem alfabética ascendente.

Para isso, escreva no arquivo `desafio11.js` duas queries, **nesta ordem**:

1. Crie uma query que faça tanto a inserção dos elementos `combo` e `tasty` no _array_ `tags` de todos os sanduíches quanto a ordenação dos elementos de `tags` em ordem alfabética ascendente.

2. Crie uma query que retorne o `nome` e `tags` de todos os documentos.

### Desafio 12

Ordene em todos os documentos os elementos do _array_ `valoresNutricionais` pelo campo `percentual` de forma descendente.

Para isso, escreva no arquivo `desafio12.js` duas queries, **nesta ordem**:

1. Crie uma query que faça em todos os documentos a ordenação dos elementos do _array_ `valoresNutricionais` pelo campo `percentual` de forma descendente. Dica: mesmo sem adicionar nenhum novo elemento, para essa operação é necessário utilizar também o modificador `$each`.

2. Crie uma query que retorne o `nome` e `valoresNutricionais` de todos os documentos.

### Desafio 13

Adicione o elemento `muito sódio` ao final do _array_ `tags` nos produtos em que o `percentual` de `sódio` seja maior ou igual a `40`.

Para isso, escreva no arquivo `desafio13.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a adição do elemento `muito sódio` ao final do _array_ `tags` nos produtos em que o `percentual` de `sódio` seja maior ou igual a `40`.

2. Crie uma query que retorne o `nome` e `tags` de todos os documentos.

### Desafio 14

Adicione o elemento `contém sódio` ao final do _array_ `tags` nos produtos em que o `percentual` de `sódio` seja maior do que `20` e menor do que `40`.

Para isso, escreva no arquivo `desafio14.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a adição do elemento `contém sódio` ao final do _array_ `tags` nos produtos em que o `percentual` de `sódio` seja maior do que `20` e menor do que `40`.

2. Crie uma query que retorne o `nome` e `tags` de todos os documentos.

### Desafio 15

Conte quantos produtos contêm `Mc` no nome, sem considerar letras maiúsculas ou minúsculas.

### Desafio 16

Conte quantos produtos têm `4` ingredientes.

### Desafio 17

Conte quantos documentos contêm as palavras `frango` ou `hamburguer` utilizando o operador `$text`.

Para isso, escreva no arquivo `desafio17.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a criação de um índice do tipo `text` no campo `descricao` com o idioma padrão `portuguese`.

2. Crie uma query que retorne a quantidade de documentos que contêm as palavras `frango` ou `hamburguer` utilizando o operador `$text`.

### Desafio 18

Conte quantos documentos contêm a **expressão** `feito com` utilizando o operador `$text`.

Para isso, escreva no arquivo `desafio18.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a criação de um índice do tipo `text` no campo `descricao` com o idioma padrão `portuguese`.

2. Crie uma query que retorne a quantidade de documentos que contêm a **expressão** `feito com` utilizando o operador `$text`.

### Desafio 19

Renomeie o campo `descricao` para `descricaoSite` em todos os documentos.

Para isso, escreva no arquivo `desafio19.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a renomeação do campo `descricao` para `descricaoSite` em todos os documentos.

2. Crie uma query que retorne o `nome`, `descricao` e `descricaoSite` de todos os documentos.

### Desafio 20

Remova o campo `curtidas` do item `Big Mac`.

Para isso, escreva no arquivo `desafio20.js` duas queries, **nesta ordem**:

1. Crie uma query que faça a remoção do campo `curtidas` do item `Big Mac`.

2. Crie uma query que retorne o `nome` e `curtidas` de todos os documentos.

### Desafio 21

Retorne o `nome` dos sanduíches em que o número de `curtidas` é maior que o número de sanduíches `vendidos`.

### Desafio 22

Retorne o `nome` e a quantidade de vendas (`vendidos`) dos sanduíches em que o número de vendas é múltiplo de `5`.

---