# 📘 UC22 – Aula 5 – Agrupamento, Ordenação e Gráficos (Pokémons)  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Groupby-green?logo=pandas)](https://pandas.pydata.org/)  
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualização-orange?logo=plotly)](https://matplotlib.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 3 – Aula 5 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Agrupamento, ordenação e gráficos em DataFrames  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Visualizar dados é como abrir a Pokédex: em segundos você enxerga padrões escondidos.” – IAra 📊  

---

## 🎯 Objetivos da Aula  

- Aprender a **ordenar** dados numéricos e alfabéticos (`sort_values`).  
- Agrupar dados com **`groupby()`** e calcular estatísticas básicas.  
- Criar **gráficos simples** (barras, linhas, pizza) com Pandas + Matplotlib.  
- Interpretar visualmente padrões nos Pokémons.  

---

## 🧠 Parte Teórica – Ordenação  

### 🔹 Ordenando por valores  

```python
# Do maior para o menor HP
df.sort_values(by='HP', ascending=False).head(5)
```

✅ Mostra os **5 Pokémons com mais HP**.

------

### 🔹 Ordenando por texto

```python
# Ordem alfabética
df.sort_values(by='Nome').head(10)
```

✅ Lista os **10 primeiros Pokémons em ordem alfabética**.

------

## 🧠 Parte Teórica – Agrupamento

### 🔹 Contagem de categorias

```python
df['Tipo 1'].value_counts()
```

✅ Mostra quantos Pokémons existem de cada tipo.

------

### 🔹 Estatísticas por grupo

```python
df.groupby('Tipo 1')[['HP', 'Ataque', 'Velocidade']].mean()
```

✅ Mostra a **média de HP, Ataque e Velocidade** por tipo.

------

## 🧠 Parte Teórica – Gráficos

### 🔹 Gráfico de barras

```python
df['Tipo 1'].value_counts().plot(kind='bar', title='Quantidade por Tipo')
```

📊 Mostra visualmente a quantidade de Pokémons por tipo.

------

### 🔹 Gráfico de linhas

```python
df.sort_values(by='Velocidade', ascending=False).head(10)[['Nome','Velocidade']].set_index('Nome').plot(kind='line')
```

📈 Mostra os **10 Pokémons mais rápidos**.

------

### 🔹 Gráfico de pizza

```python
df['Tipo 1'].value_counts().head(5).plot(kind='pie', autopct='%1.1f%%', title='Top 5 Tipos')
```

🥧 Mostra a proporção dos **5 tipos mais frequentes**.

------

## 💻 Parte Prática – Explorando no Colab

```python
import pandas as pd
import matplotlib.pyplot as plt

# Carregar dataset
df = pd.read_csv("pokemons.csv")

# Ordenação: Top 5 com mais ataque
print("⚔️ Pokémons com mais ataque:")
print(df.sort_values(by='Ataque', ascending=False).head(5)[['Nome','Ataque']])

# Agrupamento: média de velocidade por tipo
print("\n⚡ Média de velocidade por tipo:")
print(df.groupby('Tipo 1')['Velocidade'].mean().sort_values(ascending=False))

# Gráfico de barras: quantidade por tipo
df['Tipo 1'].value_counts().plot(kind='bar', title='Quantidade de Pokémons por Tipo')
plt.xlabel("Tipo")
plt.ylabel("Quantidade")
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

------

## 📊 Mini-Experimento Pokémon

Responda no Colab:

1. Qual o tipo com **maior média de HP**?
2. Quem são os **5 Pokémons mais rápidos**?
3. Quantos Pokémons do tipo **Água** existem?
4. Crie um gráfico de **pizza** com os **5 tipos mais comuns**.
5. Crie um gráfico de **barras** mostrando a **média de ataque por tipo**.

------

## 💬 Atividade Teórica – Questões no caderno

1. Qual a diferença entre `sort_values()` e `groupby()`?
2. Para que serve o `value_counts()`?
3. Qual tipo de gráfico melhor representa **proporções**?
4. Por que gráficos são mais fáceis de interpretar que tabelas?
5. Cite um exemplo do cotidiano escolar que poderia ser representado com gráficos.

------

## 🧩 Atividade Prática – Seu Top 5 Pokémon

🎮 Crie no Colab:

- O gráfico dos **5 Pokémons com mais defesa**.
- O gráfico dos **5 Pokémons com mais velocidade**.
- O gráfico de **pizza dos tipos mais frequentes**.

📌 Depois, escreva **em texto**:

> “No meu Top 5, percebi que os Pokémons do tipo ___ se destacam em defesa, enquanto os do tipo ___ são mais rápidos.”

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- Ordenar dados com `sort_values()`.
- Agrupar informações com `groupby()` e `value_counts()`.
- Criar gráficos de barras, linhas e pizza com Pandas + Matplotlib.
- Interpretar padrões nos Pokémons de forma **visual e analítica**.

🔮 **Na próxima aula**: vamos aprender a **limpar e padronizar dados**, tratando nulos e inconsistências (o famoso “dados sujos, conclusões sujas”).

------

#### ⏪ Voltar: Seleção e Filtros em DataFrames

#### ⏩ Próxima Aula: Limpeza e Padronização de Dados

#### 🏠 Início