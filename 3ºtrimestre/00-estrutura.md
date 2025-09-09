# 📘 UC22 – Ciências de Dados

## 🌟 Guia do 3º Trimestre – Versão para Alunos

🎓 **Turma:** 3º Ano do Ensino Médio Técnico em Informática
 👨‍🏫 **Professor:** André Ricardo
 📌 **Tema:** *“Se tornar um Cientista Pokémon”*

------

## ⏱️ Carga Horária

- **20 aulas** de **90 minutos cada** (equivalente a 40 aulas de 45 minutos).
- Vamos aprender **passo a passo** como um **cientista de dados** trabalha:
   👉 Relembrar conceitos → Manipular dados → Limpar e padronizar → Revisar → Criar nossa **Pokédex Científica**.

------

# 🔹 Módulo 1 – Revisão e Introdução aos Dados (Aulas 1 a 3)

### 🎯 O que vamos aprender?

- O que são **dados abertos**.
- Como funciona um **arquivo CSV**.
- Primeiros passos com a biblioteca **Pandas** no Python.

------

### 📍 Aula 1 – Revisão + Dados Abertos

- Relembrar conceitos básicos: tipos de dados, variáveis, Big Data.
- Conhecer sites com dados abertos: **IBGE**, **dados.gov.br**, **Kaggle**.

👨‍💻 **Exemplo no Colab:**

```python
import pandas as pd

# Exemplo com um CSV público (pode mudar o link para outro dataset aberto)
url = "https://people.sc.fsu.edu/~jburkardt/data/csv/airtravel.csv"
df = pd.read_csv(url)

df.head()
```

🎮 **Missão Pokémon:** Descubra quantos Pokémon existem no nosso dataset `pokemons_pokedex.csv`.

------

### 📍 Aula 2 – Estrutura de Arquivos CSV

- CSV é um arquivo de **valores separados por vírgula**.
- Pode ser aberto em Bloco de Notas, Excel ou Colab.

👨‍💻 **Exemplo no Colab:**

```python
import pandas as pd

df = pd.read_csv("pokemons_pokedex.csv")
print(df.shape)   # mostra linhas e colunas
print(df.columns) # mostra nomes das colunas
```

🎮 **Missão Pokémon:** Liste o nome de **3 colunas** que você achou mais interessantes.

------

### 📍 Aula 3 – Primeiros Passos com Pandas

- Carregar dados.
- Visualizar as primeiras linhas.
- Explorar informações básicas.

👨‍💻 **Exemplo no Colab:**

```python
import pandas as pd

df = pd.read_csv("pokemons_pokedex.csv")

print(df.head())   # primeiras linhas
print(df.info())   # informações gerais
print(df.shape)    # dimensões (linhas x colunas)
```

🎮 **Missão Pokémon:** Descubra quantos Pokémon Lendários existem no dataset.

------

# 🔹 Módulo 2 – Manipulação de Dados (Aulas 4 a 9)

### 🎯 O que vamos aprender?

- Selecionar colunas.
- Criar filtros simples e compostos.
- Agrupar, ordenar e criar gráficos.

------

### 📍 Aula 4 – Seleção de Colunas

👨‍💻 **Exemplo no Colab:**

```python
df[['Name', 'Type 1', 'Attack']].head()
```

🎮 **Missão Pokémon:** Mostre apenas as colunas **Name**, **Type 1** e **Speed**.

------

### 📍 Aula 5 – Filtros Simples

👨‍💻 **Exemplo no Colab:**

```python
eletricos_rapidos = df[(df['Type 1'] == 'Electric') & (df['Speed'] > 80)]
eletricos_rapidos.head()
```

🎮 **Missão Pokémon:** Quantos Pokémon do tipo **Fogo** têm **Attack maior que 90**?

------

### 📍 Aula 6 – Filtros Compostos

👨‍💻 **Exemplo no Colab:**

```python
agua_rapida = df[(df['Type 1'] == 'Water') & (df['Speed'] > 70) & (df['Defense'] < 60)]
agua_rapida.head()
```

🎮 **Missão Pokémon:** Monte um time **defensivo** (alta defesa + ataque baixo).

------

### 📍 Aula 7 – Agrupamentos com `groupby()`

👨‍💻 **Exemplo no Colab:**

```python
media_por_tipo = df.groupby('Type 1')[['Attack', 'Speed', 'HP']].mean()
media_por_tipo
```

🎮 **Missão Pokémon:** Qual **tipo** tem a maior **média de HP**?

------

### 📍 Aula 8 – Ordenação com `sort_values()`

👨‍💻 **Exemplo no Colab:**

```python
top_10_speed = df.sort_values(by='Speed', ascending=False).head(10)
top_10_speed
```

🎮 **Missão Pokémon:** Descubra o Pokémon com **maior Attack**.

------

### 📍 Aula 9 – Gráficos com Matplotlib

👨‍💻 **Exemplo no Colab:**

```python
import matplotlib.pyplot as plt

df['Type 1'].value_counts().plot(kind='bar')
plt.title("Quantidade de Pokémon por Tipo")
plt.show()
```

🎮 **Missão Pokémon:** Crie um gráfico de **pizza** mostrando a proporção de Pokémon Lendários.

------

# 🔹 Módulo 3 – Higienização e Padronização (Aulas 10 a 12)

### 📍 Aula 10 – Detectando Dados Nulos

```python
df.isnull().sum()
```

### 📍 Aula 11 – Tratando Nulos

```python
df['Speed'].fillna(df['Speed'].mean(), inplace=True)
```

### 📍 Aula 12 – Padronização de Texto

```python
df['Type 1'] = df['Type 1'].str.capitalize()
df['Type 1'].unique()
```

🎮 **Missão Pokémon:** Descubra **quantos tipos únicos** de Pokémon existem após a padronização.

------

# 🔹 Módulo 4 – Consolidação e Avaliação (Aulas 13 a 16)

- Revisão geral no Colab.
- Avaliação teórica com questões.
- Estudo de caso Pokémon: ranking de velocidade, ataques, gerações.
- Discussão coletiva em sala.

------

# 🔹 Módulo 5 – Projeto Final: Pokédex Científica (Aulas 17 a 20)

- Grupos vão criar análises e gráficos.
- Cada grupo será responsável por um tema: **Ataque, Defesa, Velocidade, Tipos ou Evoluções**.
- Produção de relatório com **texto + tabelas + gráficos**.
- Apresentação em sala.

🎯 **Produto Final:**
 👉 Sua própria **Pokédex Científica**, criada com Python + Pandas + Matplotlib!

