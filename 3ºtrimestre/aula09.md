# 📘 UC22 – Aula 9 – Projeto Final: A Pokédex Científica  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Project-green?logo=pandas)](https://pandas.pydata.org/)  
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Gráficos-orange?logo=plotly)](https://matplotlib.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Colaboração-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Intermediário➜Avançado-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 7 – Aula 9 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Projeto prático final – Pokédex Científica  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Ciência de Dados é transformar números em histórias que fazem sentido. Agora é sua vez de contar a história dos Pokémons.” – IAra 📖  

---

## 🎯 Objetivos da Aula  

- Iniciar o **Projeto Final – Pokédex Científica**.  
- Dividir a turma em grupos com responsabilidades distintas.  
- Estruturar análises temáticas (ataque, defesa, velocidade, tipos, habilidades).  
- Produzir gráficos, tabelas e conclusões em **linguagem natural**.  
- Estimular o trabalho colaborativo em ciência de dados.  

---

## 🧠 Estrutura do Projeto  

A turma será dividida em **5 grupos**, cada um com uma análise específica:  

| Grupo | Tema                          | Perguntas Norteadoras                                        |
| ----- | ----------------------------- | ------------------------------------------------------------ |
| 1️⃣     | **Ataque e Defesa**           | Quem são os Top 10 em ataque e defesa? Existe correlação entre eles? |
| 2️⃣     | **Velocidade**                | Quais os Pokémons mais rápidos? Quais tipos tendem a ser mais velozes? |
| 3️⃣     | **HP e Resistência**          | Quais os Pokémons “tanques”? Qual tipo tem maior média de HP? |
| 4️⃣     | **Tipos**                     | Quais são os tipos mais comuns? Como se distribuem entre os atributos? |
| 5️⃣     | **Habilidade Oculta e Shiny** | Quantos Pokémons possuem Habilidade Oculta? Qual a proporção de Shiny? |

---

## 💻 Passo a Passo no Colab  

### 🔹 1. Preparação  

```python
import pandas as pd
import matplotlib.pyplot as plt

# Carregar o dataset
df = pd.read_csv("pokemons.csv")

# Inspeção inicial
print(df.head())
print(df.info())
```

------

### 🔹 2. Análises Obrigatórias

Cada grupo deve produzir:

- 2 **tabelas com comandos Pandas**.
- 1 **gráfico informativo** (barras, linhas ou pizza).
- 1 **texto conclusivo** em linguagem natural.

------

### 🔹 3. Exemplos de Análises

#### Grupo 1 – Ataque e Defesa

```python
print(df.sort_values(by='Ataque', ascending=False).head(10)[['Nome','Ataque']])
print(df.sort_values(by='Defesa', ascending=False).head(10)[['Nome','Defesa']])
```

📌 Texto:

> “Os Pokémons mais ofensivos são ___. Já em defesa, destacam-se ___.”

------

#### Grupo 2 – Velocidade

```python
print(df.sort_values(by='Velocidade', ascending=False).head(10)[['Nome','Velocidade']])
df.groupby('Tipo 1')['Velocidade'].mean().sort_values(ascending=False).plot(kind='bar', title='Média de Velocidade por Tipo')
plt.show()
```

📌 Texto:

> “O tipo Psíquico se destaca pela velocidade média. Entre os mais rápidos estão ___.”

------

#### Grupo 3 – HP

```python
print(df.sort_values(by='HP', ascending=False).head(10)[['Nome','HP']])
print(df.groupby('Tipo 1')['HP'].mean().sort_values(ascending=False))
```

📌 Texto:

> “Os Pokémons mais resistentes são ___, com HP elevado. O tipo ___ tem a maior média de HP.”

------

#### Grupo 4 – Tipos

```python
df['Tipo 1'].value_counts().plot(kind='bar', color='purple', title='Quantidade por Tipo')
plt.show()
```

📌 Texto:

> “O tipo mais comum é ___, representando ___% do total.”

------

#### Grupo 5 – Habilidade Oculta e Shiny

```python
total = len(df)
com_ha = df[df['Habilidade Oculta'] != 'Não Informado']
print(f"Percentual com Habilidade Oculta: {(len(com_ha)/total)*100:.2f}%")

print("Valores únicos de Shiny:", df['Shiny'].unique())
```

📌 Texto:

> “Aproximadamente ___% dos Pokémons têm Habilidade Oculta. Os valores possíveis de Shiny são ___.”

------

## 📊 Entregáveis da Aula

Cada grupo deve entregar no Colab:

1. Um **notebook com códigos, tabelas e gráficos**.
2. Um **parágrafo explicativo** com as conclusões.
3. Um título criativo para sua parte da Pokédex.

------

## 💬 Discussão Final em Sala

- Cada grupo apresenta rapidamente seus resultados.
- A turma debate: **quais descobertas foram mais surpreendentes?**
- O professor registra os achados para compor a **Pokédex Científica da Turma**.

------

## 📎 Conclusão da Aula

✅ Hoje você:

- Iniciou o **projeto integrador da Pokédex Científica**.
- Aprendeu a trabalhar em equipe com dados reais.
- Conectou código, gráficos e texto em um relatório colaborativo.

🔮 **Na próxima aula**: avançaremos para a **consolidação do projeto**, refinando análises, padronizando gráficos e redigindo o relatório final.

------

#### ⏪ Voltar: Estudo de Caso Prático

#### ⏩ Próxima Aula: Projeto Final – Consolidação e Refinamento

#### 🏠 Início