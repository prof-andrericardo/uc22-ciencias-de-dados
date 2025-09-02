# 📘 UC22 – Aula 3 – Leitura de Arquivos CSV com Pandas  

[![CSV](https://img.shields.io/badge/Formato-CSV-orange?logo=file)]()  
[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-DataFrame-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Iniciante➜Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 2 – Aula 3 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Lendo arquivos CSV com Pandas  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Você não precisa decorar códigos, precisa entender o que os dados querem te contar.” – IAra 💡  

---

## 🎯 Objetivos da Aula  

- Compreender o que é um **DataFrame** no Pandas.  
- Aprender a **abrir arquivos CSV** de forma automatizada no Python.  
- Explorar funções básicas: `head()`, `info()`, `shape`.  
- Reconhecer colunas, tipos de dados e primeiros problemas no dataset.  
- Praticar com o dataset `pokemons.csv`.  

---

## 🧠 Parte Teórica – O que é o Pandas?  

🐼 **Pandas** é uma biblioteca Python voltada para **análise e manipulação de dados**.  
👉 Ele transforma um simples CSV em uma estrutura chamada **DataFrame**.  

📖 **Definição:**  
Um **DataFrame** é como uma **planilha inteligente** dentro do Python:  
- Linhas = registros (cada Pokémon).  
- Colunas = atributos (HP, Ataque, Velocidade, Tipo etc.).  

📌 Exemplo simplificado:  

```csv
Nome,Tipo 1,HP,Ataque
Pikachu,Elétrico,35,55
Charmander,Fogo,39,52
Squirtle,Água,44,48
```

🔎 No Pandas, isso vira:

| Nome       | Tipo 1   | HP   | Ataque |
| ---------- | -------- | ---- | ------ |
| Pikachu    | Elétrico | 35   | 55     |
| Charmander | Fogo     | 39   | 52     |
| Squirtle   | Água     | 44   | 48     |

------

## 💻 Parte Prática – Explorando no Google Colab

### 🔹 Passo 1 – Importando Pandas

```python
import pandas as pd
```

📌 `pd` é apenas um apelido para usar a biblioteca de forma mais curta.

------

### 🔹 Passo 2 – Lendo um arquivo CSV

```python
df = pd.read_csv("pokemons.csv")
```

- `pd.read_csv()` → lê o arquivo CSV.
- `df` → variável que guarda o DataFrame.

------

### 🔹 Passo 3 – Primeiras linhas

```python
df.head()
```

✅ Mostra as **5 primeiras linhas** (ou `df.head(10)` para 10 linhas).

------

### 🔹 Passo 4 – Estrutura do dataset

```python
df.info()
```

✅ Retorna:

- Quantas colunas existem.
- Quantos valores nulos por coluna.
- Tipos de dados (`int`, `float`, `object`).

------

### 🔹 Passo 5 – Dimensão da tabela

```python
df.shape
```

✅ Resultado: `(n_linhas, n_colunas)`

Exemplo: `(800, 10)` → 800 Pokémons e 10 colunas de atributos.

------

## 📊 Mini-Experimento Pokémon

Execute os comandos abaixo e anote suas descobertas:

```python
# Primeiros Pokémons
print(df.head(3))

# Últimos Pokémons
print(df.tail(3))

# Colunas disponíveis
print(df.columns)

# Tipos de dados
print(df.dtypes)
```

------

## 💬 Atividade Teórica – Questões no caderno

1. O que é um **DataFrame**?
2. Qual a diferença entre `head()` e `tail()`?
3. Para que serve o comando `info()`?
4. Se `df.shape` retorna `(800, 12)`, o que isso significa?
5. Cite uma vantagem de usar o Pandas em vez de abrir o CSV no Excel.

------

## 🧩 Atividade Prática – Investigando Pokémons

No **Google Colab**, responda com código:

1. Quantos Pokémons estão listados?
2. Qual o nome das **3 primeiras colunas**?
3. Qual o tipo de dado da coluna “Velocidade”?
4. Qual Pokémon aparece na **última linha**?
5. Liste todos os valores únicos da coluna **“Tipo 1”**.

```python
print("Quantidade total:", df.shape[0])
print("Colunas:", df.columns[:3])
print("Tipo de Velocidade:", df['Velocidade'].dtype)
print("Último Pokémon:", df.tail(1)['Nome'])
print("Tipos únicos:", df['Tipo 1'].unique())
```

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- O que é o **Pandas** e como ele lê arquivos CSV.
- O conceito de **DataFrame** e sua importância na ciência de dados.
- Como explorar um dataset com `head()`, `info()`, `shape`.
- A analisar dados reais de Pokémons no **Google Colab**.

🔮 **Na próxima aula**: vamos aprender a **selecionar colunas e aplicar filtros** no DataFrame, entendendo como responder perguntas específicas com nossos dados Pokémon.

------

#### ⏪ Voltar: Estrutura e Problemas em CSV

#### ⏩ Próxima Aula: Seleção e Filtros em DataFrames

#### 🏠 Início