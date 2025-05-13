# 📘 UC22 – Aula 4 – Leitura de Arquivos CSV com Pandas (Explicado Passo a Passo)

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 2 – Aula 4 do 2º Trimestre**
 ⏱️ **Duração:** 45 minutos
 📍 **Tema:** Leitura de arquivos CSV com Python e Pandas
 🐍 **Nível:** Iniciantes em Python

------

## ✨ Frase motivadora

> “Você não precisa decorar códigos. Precisa entender o que está fazendo com os dados. E isso o Pandas vai te ensinar.” – IAra

------

## 🎯 Objetivos da Aula

- Aprender, de forma acessível, como **abrir um arquivo CSV com o Pandas**.
- Entender o que é um **DataFrame** e por que ele é essencial na ciência de dados.
- Analisar os dados de forma segura, mesmo sem ter domínio avançado de programação.
- Executar comandos **comentados linha por linha**, compreendendo seu funcionamento real.

------

## 🧠 Parte Teórica – Relembrando o CSV

### 📌 O que é um arquivo CSV?

Imagine que um arquivo `.csv` seja como uma **planilha de Excel**, mas salva em **texto puro**, onde os dados são organizados **linha por linha**, separados por vírgulas.

```csv
nome,idade,nota,aprovado
Ana,17,8.5,sim
Carlos,18,6.2,não
Lívia,17,9.1,sim
```

- Cada linha é **um aluno** (um registro).
- Cada **vírgula** separa uma **coluna** (ex: nome, idade...).
- O **nome de cada coluna** está na **primeira linha** → isso se chama **cabeçalho**.

📌 Esses arquivos são amplamente utilizados porque:

- São **leves**, abrem em qualquer sistema;
- Podem ser lidos por **programas de planilha** (Excel, Google Sheets);
- E principalmente, podem ser lidos e manipulados pelo Python com a biblioteca **Pandas**!

------

## 🐼 O que é Pandas?

Pandas é uma biblioteca do Python muito poderosa e muito usada em ciência de dados.

> 📦 **Pense assim**: o Excel é uma planilha, o Pandas é o "Excel programável" no Python.

Com ela, podemos:

- Abrir arquivos `.csv`;
- Ver as primeiras linhas;
- Saber o que cada coluna representa;
- Contar quantas linhas e colunas existem;
- E no futuro, **filtrar, agrupar, gerar gráficos e muito mais**.

------

## 💻 Ambiente: Google Colab

> 🔧 **Google Colab** é um ambiente online gratuito para programar em Python com apenas um navegador, **sem precisar instalar nada!**

1. Acesse: https://colab.research.google.com
2. Clique em `+ Novo notebook`
3. Renomeie como: `Aula_04_csv_pandas_uc22`

------

## 🧪 Exemplo Guiado e Comentado com o Arquivo `pokemons.csv`

### 🎯 Passo 1 – Importar a biblioteca Pandas

```python
import pandas as pd
```

🔍 **Explicação:**

- Estamos dizendo ao Python: "quero usar a biblioteca Pandas".
- O `as pd` é um apelido, uma forma mais curta de chamá-la depois.
- Toda vez que usarmos um comando do Pandas, vamos usar `pd.` antes.

------

### 📁 Passo 2 – Fazer upload do arquivo `.csv`

```python
from google.colab import files
uploaded = files.upload()
```

🔍 **Explicação:**

- Esse código abre uma janelinha para você escolher o arquivo `.csv` que está no seu computador.
- Quando o arquivo for carregado, o nome dele vai aparecer em uma caixinha logo abaixo.
- Guarde esse nome, porque vamos usá-lo no próximo passo.

------

### 📄 Passo 3 – Ler o arquivo CSV com Pandas

```python
df = pd.read_csv('pokemons.csv')
```

🔍 **Explicação:**

- O comando `read_csv()` lê o arquivo `.csv` e transforma ele em um **DataFrame**.
- `df` é uma variável que agora guarda os dados da sua tabela.
- **DataFrame** é uma estrutura do Pandas parecida com uma tabela do Excel: tem **linhas** (registros) e **colunas** (campos).
- Substitua `'nome_do_arquivo.csv'` pelo nome real do arquivo que você carregou.

------

### 👀 Passo 4 – Visualizar os primeiros registros

```python
df.head()
```

🔍 **Explicação:**

- O `head()` mostra as **5 primeiras linhas** da tabela (por padrão).
- É útil para **espiar o conteúdo**, ver como os dados estão organizados.
- Você pode usar `df.head(10)` para ver as 10 primeiras linhas.

------

### ℹ️ Passo 5 – Obter informações gerais da tabela

```python
df.info()
```

🔍 **Explicação:**

- Esse comando mostra:
  - Quais são as colunas
  - Quantos valores existem em cada coluna
  - Se existem dados faltando
  - E qual o **tipo de dado** de cada coluna (texto, número, decimal, booleano)

------

### 🔢 Passo 6 – Saber o tamanho da tabela

```python
df.shape
```

🔍 **Explicação:**

- O resultado será algo como `(150, 6)`
- Isso significa que sua tabela tem **150 linhas** e **6 colunas**

------

## 💬 Atividade Teórica – Explique com suas palavras

Responda no caderno:

1. Responda no caderno:
   1. O que faz a função `pd.read_csv()`?
   2. O que é um `DataFrame`?
   3. Por que usamos `df.head()` antes de trabalhar com os dados?
   4. O que `df.info()` nos ajuda a descobrir?
   5. O que significa o resultado de `df.shape`?
   6. Quais colunas do dataset `pokemons.csv` têm **números**? Quais têm **texto**?
   7. Dê um exemplo de uma linha e descreva o Pokémon correspondente.
   8. O que aconteceria se o arquivo `.csv` **não tivesse cabeçalho**? Como o Pandas se comportaria?

------

## 💻 Atividade Prática – Explorando seu CSV com Pandas

> Agora é com você, aluno cientista de dados iniciante! Vamos praticar:

### 📝 Instruções:

1. Abra o Google Colab.
2. Faça o upload de um arquivo `.csv` (o que você usou nas aulas anteriores).
3. Execute este código completo, **linha por linha**, e observe o que acontece:

```python
# Importa o Pandas
import pandas as pd

# Faz o upload do CSV
from google.colab import files
uploaded = files.upload()

# Lê o arquivo CSV (substitua com o nome correto se necessário)
df = pd.read_csv('pokemons.csv')

# Visualiza as primeiras linhas
print("🔍 Primeiros Pokémons:")
print(df.head())

# Informações gerais
print("\nℹ️ Informações gerais:")
df.info()

# Tamanho do dataset
print("\n📏 Quantidade de linhas e colunas:")
print(df.shape)

```

------

### ✍️ Após executar, responda:

1. Quantos Pokémons existem na lista?
2. Quantas colunas de atributos estão descritas?
3. Qual o Pokémon com maior velocidade?
4. Qual o tipo do Pikachu?
5. Quais colunas são mais relevantes para um gráfico de **força de ataque**?

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- O que é um arquivo CSV e como ele é estruturado.
- Como abrir e visualizar dados reais com Pandas.
- Que é possível trabalhar com **dados do seu interesse**, como Pokémon, para aprender programação e análise.

🔮 E na próxima aula...

> Vamos **filtrar os dados**, **selecionar colunas específicas** e descobrir **como responder perguntas com os dados**.

------

#### ⏪ [Voltar: Coleta e Leitura de Arquivos CSV](aula03.md)  
#### ⏩ [Próxima Aula: Seleção e Filtros em DataFrames](aula05.md)
#### 🏠 [Início](../README.md)
