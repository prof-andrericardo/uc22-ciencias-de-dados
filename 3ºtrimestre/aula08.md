# 📘 UC22 – Aula 8 – Estudo de Caso Prático: Investigando Dados Pokémon  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Analysis-green?logo=pandas)](https://pandas.pydata.org/)  
[![Matplotlib](https://img.shields.io/badge/Matplotlib-Gráficos-orange?logo=plotly)](https://matplotlib.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 6 – Aula 8 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Estudo de caso prático com Pandas e Matplotlib  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Dados sozinhos são apenas números. É quando fazemos as perguntas certas que eles se transformam em conhecimento.” – IAra 🔍  

---

## 🎯 Objetivos da Aula  

- Resolver um **estudo de caso realista** com o dataset `pokemons.csv`.  
- Aplicar seleção, filtros, agrupamentos, ordenação e gráficos.  
- Desenvolver autonomia para investigar dados.  
- Produzir respostas em **linguagem natural**, não apenas em código.  

---

## 🧠 Contexto do Estudo de Caso  

Você foi contratado como **Cientista de Dados da Pokédex Internacional** 📖⚡.  
Sua missão é responder perguntas estratégicas para ajudar os treinadores a entender melhor os Pokémons.  

---

## 💻 Parte Prática – Desafios  

### 🔹 Desafio 1 – Tipos de Pokémon  

Pergunta:  Quais são os **3 tipos de Pokémon mais comuns** no dataset?  
```python
df['Tipo 1'].value_counts().head(3)
```

📌 Escreva em texto: “Os 3 tipos mais comuns são ___, ___ e ___.”

------

### 🔹 Desafio 2 – Velocidade

Pergunta: Quem são os **5 Pokémons mais rápidos**?

```python
df.sort_values(by='Velocidade', ascending=False).head(5)[['Nome','Velocidade','Tipo 1']]
```

📌 Escreva em texto: “O Pokémon mais rápido é ___ com velocidade de ___. Os outros rápidos são ___.”

------

### 🔹 Desafio 3 – HP médio por tipo

Pergunta: Qual tipo de Pokémon tem a **maior média de HP**?

```python
df.groupby('Tipo 1')['HP'].mean().sort_values(ascending=False).head(1)
```

📌 Escreva em texto: “O tipo com maior média de HP é ___.”

------

### 🔹 Desafio 4 – Gráficos

Pergunta: Como visualizar a **quantidade de Pokémons por tipo**?

```python
df['Tipo 1'].value_counts().plot(kind='bar', title='Pokémons por Tipo', color='skyblue')
plt.xlabel("Tipo")
plt.ylabel("Quantidade")
plt.xticks(rotation=45)
plt.show()
```

📌 Escreva em texto: “O gráfico mostra que o tipo ___ é o mais comum, seguido por ___.”

------

### 🔹 Desafio 5 – Filtros compostos

Pergunta: Existem Pokémons **do tipo Água com Velocidade > 90**?

```python
df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 90)][['Nome','Velocidade']]
```

📌 Escreva em texto: “Foram encontrados X Pokémons do tipo Água com velocidade acima de 90, como ___ e ___.”

------

### 🔹 Desafio 6 – Habilidade Oculta

Pergunta: Qual a porcentagem de Pokémons que têm **Habilidade Oculta registrada**?

```python
total = len(df)
com_ha = df[df['Habilidade Oculta'] != 'Não Informado']
percentual = (len(com_ha) / total) * 100
print(f"{percentual:.2f}% dos Pokémons possuem Habilidade Oculta registrada.")
```

📌 Escreva em texto: “Aproximadamente ___% dos Pokémons possuem Habilidade Oculta registrada.”

------

## 📊 Mini-Relatório Final

🎯 Produza um pequeno relatório (em **linguagem natural**) no próprio Colab, respondendo a todas as perguntas.

Exemplo de conclusão:

> “Nesta análise, descobrimos que os tipos mais comuns são Água, Normal e Grama. O Pokémon mais rápido é Deoxys, com velocidade de 180. O tipo com maior média de HP é Dragão. Apenas 45% dos Pokémons possuem Habilidade Oculta registrada. Esses dados podem ajudar treinadores a escolherem times equilibrados.”

------

## 💬 Atividade Teórica – Questões no caderno

1. Qual foi a maior dificuldade que você encontrou no estudo de caso?
2. O que significa interpretar dados em **linguagem natural**?
3. Explique por que gráficos ajudam a convencer mais que tabelas.
4. Cite um exemplo do cotidiano em que seria útil agrupar dados por categorias.
5. Se você fosse ampliar a análise, que nova pergunta faria sobre os Pokémons?

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- A aplicar todos os conceitos em um **estudo de caso realista**.
- A combinar comandos Pandas para responder perguntas estratégicas.
- A escrever conclusões em **linguagem natural**, conectando código e interpretação.

🔮 **Na próxima aula**: vamos avançar para o **Projeto Prático Final – A Pokédex Científica**, onde cada grupo será responsável por uma parte da análise completa do dataset.

------

#### ⏪ Voltar: Revisão Teórica Avaliativa

#### ⏩ Próxima Aula: Projeto Prático – A Pokédex Científica

#### 🏠 Início