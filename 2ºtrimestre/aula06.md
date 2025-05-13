# 📘 UC22 – Aula 6 – Ordenação, Agrupamento e Gráficos com Pandas (Pokémons)

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 3 – Aula 6 do 2º Trimestre**
 ⏱️ **Duração:** 45 minutos
 📍 **Tema:** Organização, agrupamento e visualização de dados com Pandas
 📊 **Ferramentas:** Pandas + Matplotlib
 🐍 **Nível:** Iniciantes com base consolidada

------

## ✨ Frase motivadora

> “Ver dados é entender padrões. Gráficos são como Pokédex visuais: mostram o que há de mais importante com um simples olhar.” – IAra

------

## 🎯 Objetivos da Aula

- Aprender a **ordenar** dados numéricos e alfabéticos.
- Agrupar dados com `groupby()` e calcular estatísticas básicas.
- Gerar **gráficos simples** (barras, linhas e pizza) com Pandas e Matplotlib.
- Aplicar tudo isso ao dataset `pokemons.csv`, interpretando os resultados visualmente.

------

## 🧠 Parte Teórica – Organização e Visualização

------

### 🔹 Ordenação com `sort_values()`

A ordenação permite que você **organize os dados por critérios**, como “quem tem mais HP?” ou “quem é o mais rápido?”.

#### 📌 Exemplo 1 – Ordenar por HP (do maior para o menor):

```python
df.sort_values(by='HP', ascending=False)
```

🔍 **Explicação:**

- `by='HP'` → indica a coluna usada para ordenação.
- `ascending=False` → ordem decrescente (do maior para o menor).
- Pode ser usado para qualquer coluna numérica ou textual.

#### 📌 Exemplo 2 – Ordenar por Nome (A → Z):

```python
df.sort_values(by='Nome')
```

------

### 🔹 Agrupamento com `groupby()`

Quer saber **média de velocidade por tipo**, ou **quantos Pokémons existem de cada tipo**?

#### 📌 Exemplo 3 – Contagem de Pokémons por Tipo:

```python
df['Tipo 1'].value_counts()
```

🔍 **Explicação:**

- Esse comando conta **quantas vezes cada tipo aparece**.
- Ideal para saber **quais tipos são mais comuns** no dataset.

#### 📌 Exemplo 4 – Média de atributos por tipo:

```python
df.groupby('Tipo 1')[['HP', 'Ataque', 'Velocidade']].mean()
```

🔍 **Explicação:**

- Agrupa os dados pelo valor da coluna “Tipo 1”.
- Para cada grupo (tipo), calcula a **média das colunas numéricas** indicadas.

------

### 🔹 Gráficos com Pandas + Matplotlib

#### 🎨 📊 Gráfico de Barras

```python
df['Tipo 1'].value_counts().plot(kind='bar')
```

- Mostra visualmente **quantos Pokémons existem de cada tipo**.

#### 🎨 📈 Gráfico de Linhas

```python
df.sort_values(by='Velocidade', ascending=False).head(10)[['Nome', 'Velocidade']].set_index('Nome').plot(kind='line')
```

- Mostra os **10 Pokémons mais rápidos** em uma linha contínua.

#### 🎨 🥧 Gráfico de Pizza

```python
df['Tipo 1'].value_counts().head(5).plot(kind='pie', autopct='%1.1f%%')
```

- Mostra os 5 tipos mais frequentes como **percentuais** em pizza.

> **Importante:** Após qualquer `plot()`, insira `plt.show()` para exibir o gráfico corretamente:

```python
import matplotlib.pyplot as plt
plt.show()
```

------

## 💻 Exemplo Guiado – Google Colab

```python
import pandas as pd
import matplotlib.pyplot as plt
from google.colab import files

uploaded = files.upload()
df = pd.read_csv('pokemons.csv')

# Ordenação por HP
print("🔝 Pokémons com mais HP:")
print(df.sort_values(by='HP', ascending=False)[['Nome', 'HP']].head(5))

# Ordenação alfabética
print("\n🔤 Pokémons em ordem alfabética:")
print(df.sort_values(by='Nome')[['Nome', 'Tipo 1']].head(5))

# Quantidade por tipo
print("\n📊 Quantidade por tipo:")
print(df['Tipo 1'].value_counts())

# Média de velocidade por tipo
print("\n⚡ Média de velocidade por tipo:")
print(df.groupby('Tipo 1')['Velocidade'].mean().sort_values(ascending=False))

# Gráfico de barras – tipos mais comuns
df['Tipo 1'].value_counts().plot(kind='bar', title='Quantidade por Tipo')
plt.ylabel("Número de Pokémons")
plt.xlabel("Tipo")
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()

# Gráfico de pizza – 5 tipos mais frequentes
df['Tipo 1'].value_counts().head(5).plot(kind='pie', autopct='%1.1f%%', title='Top 5 Tipos de Pokémon')
plt.ylabel('')
plt.tight_layout()
plt.show()
```

------

## 💬 Atividade Teórica – Interpretação e Análise

Responda no caderno:

1. Qual a diferença entre `sort_values()` e `groupby()`?
2. O que representa `value_counts()`?
3. Por que usamos `.mean()` após o `groupby()`?
4. Qual tipo de gráfico é melhor para mostrar **proporções**?
5. O que faz o comando `set_index('Nome')` nos gráficos?

------

## 💻 Atividade Prática – Explorando Visualizações

Execute e analise:

```python
# Top 10 mais rápidos
df.sort_values(by='Velocidade', ascending=False).head(10)[['Nome', 'Velocidade']].set_index('Nome').plot(kind='barh', title='Top 10 Velocidade')
plt.xlabel("Velocidade")
plt.tight_layout()
plt.show()

# Médias de ataque por tipo
df.groupby('Tipo 1')['Ataque'].mean().sort_values().plot(kind='barh', title='Média de Ataque por Tipo')
plt.xlabel("Ataque Médio")
plt.tight_layout()
plt.show()
```

------

### ✍️ Responda:

1. Quais são os 3 tipos com maior média de ataque?
2. Quais Pokémons têm **velocidade maior que 100 e tipo Elétrico**?
3. Qual gráfico você usaria para mostrar **a distribuição de HPs**?
4. Quais vantagens os gráficos oferecem em relação às tabelas?
5. O que mais chamou sua atenção ao ver os dados graficamente?

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu a:

- Organizar os dados por ordenação e agrupamento.
- Realizar contagens e médias por categoria.
- Gerar **gráficos simples, bonitos e informativos** com Pandas e Matplotlib.

🎓 Isso é a base da **comunicação visual de dados**, habilidade essencial para qualquer cientista de dados.

------

🔮 Na próxima aula...

> Vamos explorar **limpeza de dados, tratamento de valores ausentes, substituições e padronizações**.
>  Porque antes de analisar, é preciso **preparar os dados!**

------

#### ⏪ [Voltar: Seleção e Filtros em DataFrames](aula05.md)  
#### ⏩ [Próxima Aula: Limpeza e Padronização de Dados](aula07.md)
#### 🏠 [Início](../README.md)
