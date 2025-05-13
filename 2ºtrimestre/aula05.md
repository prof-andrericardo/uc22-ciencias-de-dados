# 📘 UC22 – Aula 5 – Selecionando e Filtrando Dados com Pandas (Pokémons – Versão Detalhada)

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 3 – Aula 5 do 2º Trimestre**
 ⏱️ **Duração:** 45 minutos
 📍 **Tema:** Seleção e Filtros em DataFrames com Pandas
 🐍 **Nível:** Iniciantes em Python com aprofundamento

------

## ✨ Frase motivadora

> “Filtrar dados é como escolher os melhores Pokémons para sua equipe: você precisa saber exatamente quais características importar.” – IAra

------

## 🎯 Objetivos da Aula

- Compreender com profundidade como **selecionar colunas** e **filtrar linhas** em um DataFrame.
- Aplicar **condições simples e compostas** para visualizar subconjuntos específicos dos dados.
- Utilizar esses conceitos para **analisar dados reais** (Pokémons).
- Desenvolver o raciocínio lógico para leitura e interpretação de conjuntos de dados.

------

## 🧠 Parte Teórica – Seleção de Colunas e Filtros de Linhas

------

### 🔹 O que significa **selecionar colunas**?

Imagine que um DataFrame é como uma **tabela de Excel** com muitas colunas (ex: Nome, HP, Ataque, Tipo...).
 Mas às vezes, você só quer trabalhar com **algumas colunas**, como “Nome” e “Tipo 1”.

No Pandas, podemos fazer isso com os seguintes comandos:

#### 📌 Exemplo 1 – Selecionar uma única coluna:

```python
df['Nome']
```

🔍 **Explicação:**

- Esse comando retorna **apenas a coluna “Nome”**.
- O resultado será do tipo **Series** (uma coluna isolada).
- É útil quando queremos listar ou analisar valores de apenas uma coluna.

#### 📌 Exemplo 2 – Selecionar múltiplas colunas:

```python
df[['Nome', 'Tipo 1', 'Velocidade']]
```

🔍 **Explicação:**

- Aqui usamos **duas colchetes** para criar uma **lista de colunas** que queremos visualizar.
- O resultado é um **novo DataFrame** apenas com essas colunas.
- Ideal para tabelas mais compactas e específicas.

------

### 🔹 O que significa **filtrar linhas**?

Filtrar significa **mostrar apenas os dados que atendem a uma condição lógica**.

#### 📌 Exemplo 3 – Mostrar apenas os Pokémons do tipo “Fogo”:

```python
df[df['Tipo 1'] == 'Fogo']
```

🔍 **Explicação passo a passo:**

1. `df['Tipo 1'] == 'Fogo'` → retorna uma **série de valores booleanos** (True ou False) indicando quais linhas possuem esse tipo.
2. `df[...]` → quando passamos essa série para dentro do `df`, o Pandas **retorna apenas as linhas com True**.

#### 📌 Exemplo 4 – Filtrar por valor numérico (HP maior que 100):

```python
df[df['HP'] > 100]
```

🔍 **Explicação:**

- Exibe somente os Pokémons que têm **alta resistência** (HP acima de 100).
- Muito útil para encontrar os “tanques” do time.

------

### 🔹 Filtros compostos com **&** (E) e **|** (OU)

Às vezes queremos aplicar **duas condições ao mesmo tempo**.

#### 📌 Exemplo 5 – Tipo Água E Velocidade maior que 80:

```python
df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 80)]
```

🔍 **Explicação:**

- Os **parênteses são obrigatórios** em cada condição.
- O operador `&` representa uma conjunção (ambas as condições devem ser verdadeiras).
- Esse filtro retorna os Pokémons **rápidos do tipo Água**.

------

### 🔹 Dica: Filtros com valores nulos ou vazios

#### 📌 Exemplo 6 – Pokémons que têm Mega Evolução:

```python
df[df['Mega Evolução/Forma Regional'] != 'None']
```

🔍 **Explicação:**

- Esse comando filtra todas as linhas em que a coluna “Mega Evolução” **possui valor diferente de 'None'**.
- Assim encontramos todos que **possuem Mega ou forma alternativa**.

------

## 💻 Exemplo Guiado no Google Colab

Execute no seu notebook:

```python
import pandas as pd
from google.colab import files

# Upload do arquivo pokemons.csv
uploaded = files.upload()

# Leitura do arquivo
df = pd.read_csv('pokemons.csv')

# Visualização geral
print(df.head())

# Exemplo 1: Listar os nomes dos Pokémons
print("\n🧾 Lista de nomes:")
print(df['Nome'])

# Exemplo 2: Nome, Tipo e Velocidade
print("\n⚡ Nome, Tipo e Velocidade:")
print(df[['Nome', 'Tipo 1', 'Velocidade']])

# Exemplo 3: Apenas os Pokémons do tipo Fogo
print("\n🔥 Pokémons do tipo Fogo:")
print(df[df['Tipo 1'] == 'Fogo'])

# Exemplo 4: Pokémons com HP alto
print("\n💖 Pokémons com HP > 100:")
print(df[df['HP'] > 100])

# Exemplo 5: Pokémons do tipo Água com Velocidade > 80
print("\n🌊 Água + Velocidade Alta:")
print(df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 80)])

# Exemplo 6: Com Mega Evolução
print("\n✨ Com Mega Evolução:")
print(df[df['Mega Evolução/Forma Regional'] != 'None'][['Nome', 'Mega Evolução/Forma Regional']])
```

------

## 💬 Atividade Teórica – Explicações e Interpretações

Responda no caderno:

1. O que acontece se eu escrever `df['HP'] < 50`?
2. Qual a diferença entre `&` e `|`? Dê exemplos.
3. O que `df[df['Habilidade Oculta'].notnull()]` retorna?
4. Por que usamos colchetes duplos em `df[['Nome', 'HP']]`?
5. Qual a função prática de filtrar dados em ciência de dados?

------

## 💻 Atividade Prática – Análise Pokémon com Filtros

1. Abra o `pokemons.csv` no Google Colab.
2. Execute os filtros abaixo e interprete os resultados:

```python
# Pokémons tipo Gelo ou Psíquico
print(df[(df['Tipo 1'] == 'Gelo') | (df['Tipo 1'] == 'Psíquico')][['Nome', 'Tipo 1', 'Ataque Especial']])

# Pokémons com Defesa > 100 E Velocidade > 90
print(df[(df['Defesa'] > 100) & (df['Velocidade'] > 90)][['Nome', 'Defesa', 'Velocidade']])

# Pokémons sem Habilidade Oculta
print(df[df['Habilidade Oculta'].isnull()][['Nome', 'Habilidade', 'Habilidade Oculta']])
```

------

### ✍️ Responda:

1. Quais Pokémons têm **maior HP e menor velocidade**?
2. Quais têm **Ataque acima de 120**?
3. Liste **todos do tipo Elétrico com Velocidade > 90**.
4. Quantos Pokémons possuem Mega Evolução?
5. Quais Pokémons possuem **mais de uma forma de evolução**?

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu a:

- Selecionar colunas com precisão.
- Filtrar dados com condições lógicas simples e compostas.
- Explorar dados reais de forma prática, aplicando **ciência de dados no universo Pokémon**.

📢 Na próxima aula, prepare-se para:

> **Organizar, agrupar e visualizar os dados com gráficos simples**, dando vida aos números por meio de imagens.

------

#### ⏪ [Voltar: Leitura de CSV com Pandas](aula04.md)  
#### ⏩ [Próxima Aula: Agrupamentos, Ordenação e Gráficos](aula06.md)
#### 🏠 [Início](../README.md)
