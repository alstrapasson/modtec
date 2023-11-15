# Treinamento

## Ferramentas

Utilizaremos as ferramentas do:

- Google Colab
    - O **Google Colab** é uma plataforma de desenvolvimento de código aberto que permite escrever e executar códigos Python no navegador. Ele oferece acesso gratuito a GPUs, o que pode ser útil para treinar modelos de aprendizado de máquina. O Colab não requer nenhuma configuração e permite que você compartilhe facilmente seus notebooks com outras pessoas. Além disso, você pode importar dados do Google Drive, GitHub e outras fontes. O Colab é uma ferramenta útil para estudantes, cientistas de dados e pesquisadores de IA que desejam trabalhar em projetos de aprendizado de máquina e análise de dados.
- Chatgpt
    - O **ChatGPT** é um chatbot movido a inteligência artificial que interage de forma conversacional com os usuários. [Ele foi criado com base na família GPT-3 de modelos computacionais extensivos da OpenAI, e treinado com técnicas de aprendizado por reforço e supervisionado 1](https://openai.com/chatgpt). O ChatGPT é capaz de responder a perguntas, descrever objetos, gerar conteúdo criativo como poemas, histórias, código, etc. Além disso, ele pode ajudar os usuários com tarefas como planejamento de viagens, resolução de problemas técnicos, sugestões de presentes, etc. [O ChatGPT é uma ferramenta útil para estudantes, escritores, programadores, entusiastas de IA e qualquer pessoa que deseje conversar com um assistente virtual inteligente 1](https://openai.com/chatgpt)[2](https://openai.com/blog/chatgpt/).

## **Prompts com resultados otimizados**

Ao executar esses prompts no ChatGPT em seu próprio computador, é possível que você obtenha respostas um pouco diferentes das que são mostradas nas aulas, pois o modelo tem como uma de suas características a **aleatoriedade**. Inclusive, se você executar o mesmo prompt várias vezes, as respostas podem sofrer variações. No entanto, não se preocupe, pois o objetivo é analisar as respostas geradas pelo ChatGPT e adaptá-las às nossas necessidades. 

```jsx
Tenho o endereço de um dataset. Escreva o código para importar os dados.
```

Observe que, com esse prompt extremamente direto e simples, o ChatGPT não foi capaz de determinar qual linguagem de programação usar no código, resultando em exemplos em Python e R. Além disso, como o formato do arquivo não foi especificado, o modelo presumiu que fosse um arquivo CSV. Outro ponto importante é que não fornecemos nenhum contexto, então o modelo nem sequer tem conhecimento do tema do projeto. Ao iniciar uma conversa, é importante fornecer um contexto adequado ao modelo sobre o trabalho em questão. 

Vamos tentar fazer isso agora e trazer um prompt mais detalhado?

```jsx
Quero que você atue como um cientista de dados e codifique para mim. Estou desenvolvendo um projeto de Machine Learning sobre clientes de uma instituição financeira aceitarem um empréstimo pessoal. Tenho o endereço do dataset no formato xlsx armazenado em uma variável chamada "url". Escreva o código em Python para importar os dados.
```

O resultado foi bem melhor, né?

Quando fornecemos um **contexto claro** ao prompt, **especificando o tipo de arquivo** e a **linguagem desejada**, o ChatGPT terá uma compreensão melhor das nossas necessidades e será capaz de gerar **respostas mais relevantes e precisas**. Ao estabelecer um contexto adequado, informamos ao modelo as informações essenciais para que ele possa direcionar suas respostas de maneira mais adequada e útil para o nosso projeto. Isso resultará em interações mais produtivas e eficientes com o ChatGPT.

Exemplo de prompt para ideias

Método TRIZ

Teoria da Resolução de Problemas inventivos

```jsx
Como especialista em TRIZ, estamos tentando desenvolver uma solução para os problemas causados em jovens com a internet usada como ferramenta de distração e inimiga dos estudos. Estes dispositivos são destinados à Escolas Estaduais e Municipais. Usando os princípios da TRIZ, como podemos identificar contradições e potenciais soluções?
```

## Importando um dataset

- Disponibilizar a URL com os dados do projeto;
- Disponibilizar o acesso ao colab.

```jsx
Quero que você atue como um cientista de dados e codifique para mim. 
Estou desenvolvendo um projeto de Machine Learning sobre clientes de uma instituição financeira aceitarem um empréstimo pessoal.
Tenho o endereço do dataset no formato xlsx armazenado em uma variável chamada "url" . Escreva o código em Python para importar os dados.
```

# Explorando os dados

```jsx
Os dados foram carregados e armazenados na variável "df".
Escreva o código para exploração de dados para que os resultados sejam exibidos sem a necessidade de usar a função `print()`.
Adicione um comentário em cada código para saber do que se trata.
```

## Checando se temos valores duplicados

Remover os dados duplicados seria um passo importante na preparação de dados para um modelo de Machine Learning. Ao fazer isso, garantimos que o modelo não seja afetado negativamente por duplicações desnecessárias. Isso ajuda a melhorar a qualidade e a confiabilidade do modelo, permitindo que ele generalize de forma mais precisa para novos dados.

```jsx
Por que é importante analisarmos se temos dados duplicados em um dataset que será utilizado para um modelo de Machine Learning? Escreva o código para somar a quantidade de dados duplicados no DataFrame "df".
```

## Entendendo às variáveis

```jsx
Me ajude a entender cada uma das variáveis que temos no dataset:
"ID", "Age", "Experience", "Income", "ZIP Code", "Family", "CCAvg",
"Education", "Mortgage", "Personal Loan", "Securities Account",
"CD Account", "Online", "CreditCard"
```

## Visualizando os dados

```jsx
Neste dataset temos:
- Colunas com valores numéricos:
"Age, Experience, Income, CCAvg, Mortgage"
- Colunas com dados categóricos:
"Family, Education, Personal Loan, Securities Account, CD Account, Online e CreditCard"
Crie códigos em Python com a biblioteca Seaborn para visualizar
a distribuição dos dados numéricos e para visualizar as quantidades dos dados categóricos.
Quero visualizar os gráficos em relação à variável "Personal Loan",
usando cores diferentes para as categorias "Não Aceitou" e "Aceitou".
```

Uma otimização, podemos usar o seguinte prompt para incluir os gráficos na mesma imagem

```jsx
Crie códigos em Python para visualizar em uma única figura lado a lado os gráficos de distribuição dos dados numéricos: "Age, Experience, Income, CCAvg e Mortgage" no DataFrame "df".

A figura pode conter três linhas, com dois gráficos nas primeiras linhas e um gráfico na última linha.

Ajustar espaçamento entre os gráficos.

Além disso, quero visualizar os gráficos em relação à variável "Personal Loan", de forma empilhada e usando cores diferentes para as categorias "Não Aceitou " e "Aceitou".

Por fim, adicione um título geral para a figura.
```

Limpando o código

```jsx
Alguma dessas colunas: "ID", "Age", "Experience", "Income", "ZIP Code", "Family", "CCAvg", "Education", "Mortgage", "Personal Loan", "Securities Account", "CD Account", "Online", "CreditCard" é desnecessária para criar um modelo de Machine Learning?
```

Vamos avaliar a correção entre os campos de idade e experiência

```jsx
Como posso obter uma figura com os valores de correlação entre as variáveis?
```

## O que é correlação?

```jsx
Explique o que é correlação entre as variáveis.
```

```jsx
Os valores de correlação entre as colunas "Age" e "Experience" são próximos de 1.
A presença de alta correlação entre variáveis pode ser problemática em modelos de Machine Learning?
```

## **Tratando valores discrepantes**

```jsx
Quais técnicas podem ser utilizadas para retirada de Outliers do DataFrame?
```

```jsx
A grande maioria das pessoas possuem o valor igual a 0 em "Mortgage".
Como descobrir se temos outliers aqui e como retirá-los com a técnica do "zscore"?
```

## Transformando variáveis numéricas

```jsx
A distribuição do rendimento anual "Income" é algo anual e os gastos com o cartão "CCAvg" são mensais.
Como deixar o "CCAvg" com um valor anual na mesma coluna?
```

## Normalizando variáveis numéricas

```jsx
Nas colunas "Age", "Income", "Family", "CCAvg", "Mortgage" temos diferentes grandezas de valores.
É necessário mudar as escalas dos valores para criar os modelos de Machine Learning?
```

```jsx
Como aplicar a técnica de "min-max" nas variáveis: "Age", "Income", "Family", "CCAvg" e "Mortgage"?
```

## Transformando variáveis categóricas

```jsx
A coluna "Education" possui 3 categorias, que estão identificadas pelos números 1,2 e 3. É preciso aplicar alguma transformação nessa coluna?
Como fazer isso?
```

## Dividindo os dados entre treino e testes

y = X.modelo

```jsx
Escreva o código Python que seleciona todas as nossas features do DataFrame "df", exceto o target ("Personal Loan"), em uma variável de nome X.
```

```jsx
Agora escreva o código que coloca em uma variável de nome y o nosso target.
```

```jsx
A variável X contém as features e  a variável y contém o target. 
Quero separar os dados em dados de treino e de teste. 
Separe 20% dos dados para teste.
```

## Treinando o modelo

```jsx
Escreva o código com a Sklearn para fazer o treinamento do modelo de Machine Learning em um problema de classificação com um modelo baseline, como o Dummy Classifier.
```

```jsx
Quais seriam os modelos ideais que possam classificar "Personal loan" com base nas features "Age", "Income", "Family", "CCAvg", "Mortgage", "Securities Account", "CD Account", "Online", "CreditCard", "Education_1", "Education_2", "Education_3". Se atente às informações delimitadas por """ abaixo:

Informações:
""""
- As features "Age", "Income", "Family", "CCAvg", "Mortgage" são dados numéricos que passaram pelo processo de normalização, com MinMaxScaler.
- As features "Securities Account", "CD Account", "Online", "CreditCard" são dados binários.
- As features "Education_1", "Education_2", "Education_3" pertenciam a uma coluna que tinha 3 categorias, mas que passou pelo processo de "One hot encoding".
"""
```

```jsx
Escreva o código para treinar os dados com os modelos: 
"Dummy Classifier", "Logistic Regression" e "Decision Tree". 
Além disso, quero saber a acurácia de cada modelo.
```

## Validando o modelo

```jsx
Agora que já tenho meus modelos, quero saber quais métricas são importantes para avaliar, além da acurácia.
```

```jsx
Escreva o código para obter a figura da "Confusion Matrix" dos modelos "dummy_model", "logreg_model" e "dt_model".
```

- pode ser necessário solicitar a normalização dos dados para análise;

## Salvando o modelo
