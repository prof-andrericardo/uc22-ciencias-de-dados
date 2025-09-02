# 📘 UC22 – Aula 4 – Seleção e Filtros em DataFrames (Pokémons)  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-DataFrame-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Iniciante➜Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 2 – Aula 4 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Seleção de colunas e filtros em DataFrames  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Filtrar dados é como escolher os melhores Pokémons para sua equipe: você precisa saber quais características são mais importantes.” – IAra ⚡  

---

## 🎯 Objetivos da Aula  

- Aprender a selecionar colunas específicas em um DataFrame.  
- Compreender como aplicar **filtros simples e compostos**.  
- Explorar os dados Pokémon para responder perguntas práticas.  
- Exercitar o raciocínio lógico aplicado à análise de dados.  

---

## 🧠 Parte Teórica – Seleção de Colunas  

Imagine que o DataFrame é uma **planilha do Excel**.  
Às vezes, não precisamos de todas as colunas, apenas das que nos interessam.  

### 🔹 Selecionando uma única coluna  

```python
df['Nome']
```

✅ Retorna apenas a coluna **Nome** (como uma lista de valores).

------

### 🔹 Selecionando múltiplas colunas

```python
df[['Nome', 'Tipo 1', 'Velocidade']]
```

✅ Retorna um novo DataFrame com apenas essas colunas.

------

## 🧠 Parte Teórica – Filtrando Linhas

Um **filtro** significa mostrar apenas os registros que atendem a uma condição.

### 🔹 Filtro por igualdade

```python
df[df['Tipo 1'] == 'Fogo']
```

✅ Retorna apenas os Pokémons do **tipo Fogo** 🔥.

------

### 🔹 Filtro por valor numérico

```python
df[df['HP'] > 100]
```

✅ Retorna apenas Pokémons com **HP acima de 100** (os “tanques”). 💖

------

### 🔹 Filtros compostos (E / OU)

- `&` → **E** (ambas condições verdadeiras).
- `|` → **OU** (uma ou outra condição verdadeira).

```python
# Tipo Água e Velocidade > 80
df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 80)]

# Tipo Gelo OU Psíquico
df[(df['Tipo 1'] == 'Gelo') | (df['Tipo 1'] == 'Psíquico')]
```

------

## 💻 Parte Prática – Investigando no Google Colab

### 🔹 Seleção básica

```python
# Listar apenas os nomes
print(df['Nome'].head(10))

# Nome + Tipo + Velocidade
print(df[['Nome', 'Tipo 1', 'Velocidade']].head(10))
```

------

### 🔹 Filtros simples

```python
# Pokémons do tipo Elétrico ⚡
print(df[df['Tipo 1'] == 'Elétrico'][['Nome', 'Velocidade']])

# Pokémons com Ataque acima de 120
print(df[df['Ataque'] > 120][['Nome', 'Ataque']])
```

------

### 🔹 Filtros compostos

```python
# Pokémons do tipo Água com velocidade maior que 90
print(df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 90)][['Nome', 'Velocidade']])

# Pokémons com Defesa > 100 OU Ataque > 120
print(df[(df['Defesa'] > 100) | (df['Ataque'] > 120)][['Nome', 'Defesa', 'Ataque']])
```

------

## 📊 Mini-Experimento Pokémon

Responda com código no Colab:

1. Liste todos os **Pokémons do tipo Fogo**.
2. Quais têm **HP maior que 120**?
3. Quais são do tipo **Elétrico e têm velocidade > 100**?
4. Mostre apenas os **nomes e ataques** dos Pokémons com ataque > 150.
5. Qual o total de Pokémons do tipo **Água**?

------

## 💬 Atividade Teórica – Questões no caderno

1. Explique a diferença entre selecionar colunas e filtrar linhas.
2. O que significa `df['HP'] > 100`?
3. Por que precisamos usar **parênteses** em filtros compostos?
4. Qual a diferença entre `&` e `|`?
5. Dê um exemplo prático de filtro que faria sentido na sua vida escolar.

------

## 🧩 Atividade Prática – Seu Time Pokémon

🎮 Desafio: Monte **seu time de 6 Pokémons** usando filtros no Pandas.

Critérios:

- Pelo menos 1 do tipo Água 🌊.
- Pelo menos 1 do tipo Elétrico ⚡.
- Pelo menos 1 com HP > 100 💖.
- Pelo menos 1 com Velocidade > 90 🏃.

```python
meu_time = df[(df['Tipo 1'].isin(['Água','Elétrico'])) | (df['HP'] > 100) | (df['Velocidade'] > 90)]
print(meu_time[['Nome','Tipo 1','HP','Velocidade']].head(10))
```

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- A **selecionar colunas** em um DataFrame.
- A aplicar **filtros simples e compostos**.
- A responder perguntas sobre o dataset Pokémon.
- Que filtrar dados é essencial para análises inteligentes.

🔮 **Na próxima aula**: vamos aprender a **ordenar dados, agrupar informações e criar os primeiros gráficos** para visualizar padrões no dataset Pokémon.

------

#### ⏪ Voltar: Leitura de CSV com Pandas

#### ⏩ Próxima Aula: Agrupamento, Ordenação e Gráficos

#### 🏠 Início