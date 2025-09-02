# 📘 UC22 – Aula 2 – Estrutura e Problemas em Arquivos CSV  

[![CSV](https://img.shields.io/badge/Formato-CSV-orange?logo=file)]()  
[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Iniciante%20➜%20Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 1 – Aula 2 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Estrutura, problemas e boas práticas em arquivos CSV  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Se os dados são o novo petróleo, o CSV é o barril onde eles são transportados.” – Anônimo da TI ⛽📊  

---

## 🎯 Objetivos da Aula  

- Entender o que é um arquivo **CSV** e como ele organiza dados.  
- Reconhecer a estrutura básica: **linhas, colunas, separadores e cabeçalhos**.  
- Identificar problemas comuns ao abrir CSVs em diferentes softwares.  
- Explorar arquivos CSV no **Bloco de Notas, Excel/Planilhas e Google Colab**.  
- Preparar o terreno para leitura automatizada com Pandas.  

---

## 🧠 Parte Teórica – O que é um CSV?  

📖 **CSV** = *Comma-Separated Values* (Valores Separados por Vírgula).  
É um formato de **texto simples** usado para armazenar tabelas.  

📌 Estrutura:  
- Cada **linha** = 1 registro (ex: um aluno, um Pokémon).  
- Cada **vírgula** = separador entre colunas.  
- A primeira linha geralmente é o **cabeçalho** (nomes das colunas).  

### 🔹 Exemplo de CSV (Alunos):  

```csv
id,nome,idade,nota,aprovado
1,Ana,17,8.5,True
2,Carlos,18,6.2,False
3,Lívia,17,9.1,True
```

| id   | nome   | idade | nota | aprovado |
| ---- | ------ | ----- | ---- | -------- |
| 1    | Ana    | 17    | 8.5  | True     |
| 2    | Carlos | 18    | 6.2  | False    |
| 3    | Lívia  | 17    | 9.1  | True     |

------

## ⚠️ Problemas Comuns em Arquivos CSV

| Situação                                     | Causa provável                                   |
| -------------------------------------------- | ------------------------------------------------ |
| Dados ficam em **uma única coluna** no Excel | Separador errado (`;` ao invés de `,`)           |
| Acentos aparecem como “Ã” ou “Õ”             | Problema de **codificação** (UTF-8 vs ANSI)      |
| Arquivo não tem cabeçalho                    | Foi exportado sem linha de títulos               |
| Colunas ficam bagunçadas                     | Falta de separador ou separadores inconsistentes |

------

## 💻 Parte Prática – Explorando CSV

### 🔹 Passo 1 – Abrir no Bloco de Notas

- Clique com o botão direito → **Abrir com > Bloco de Notas**.
- Observe: separador, acentos, cabeçalho.

### 🔹 Passo 2 – Abrir no Excel/Google Planilhas

- Arquivo → **Abrir com Excel/Planilhas**.
- Perguntas:
  - As colunas ficaram organizadas?
  - Os acentos foram preservados?

### 🔹 Passo 3 – Abrir no Google Colab com Pandas

```python
import pandas as pd

# Lendo o dataset Pokémon (substitua pelo caminho correto se necessário)
df = pd.read_csv("pokemons.csv")

# Visualizando primeiras linhas
print("🔍 Primeiros registros:")
print(df.head())

# Estrutura geral
print("\nℹ️ Informações do dataset:")
df.info()

# Dimensão da tabela
print("\n📏 Linhas e colunas:")
print(df.shape)
```

------

## 📊 Mini-Experimento Pokémon

🔎 Abra o arquivo `pokemons.csv` e responda:

1. Quantos Pokémons existem na tabela?
2. Quantas colunas há? Cite 5 delas.
3. Qual o tipo de dado da coluna **HP**?
4. Há valores nulos em alguma coluna?
5. Qual o Pokémon listado na primeira linha?

------

## 💬 Atividade Teórica – Responda no caderno

1. O que significa a sigla **CSV**?
2. Qual a função do **cabeçalho** em um CSV?
3. Cite dois problemas que podem ocorrer ao abrir um CSV.
4. O que é **codificação UTF-8** e por que ela é importante?
5. Por que o CSV é tão utilizado em ciência de dados?

------

## 🧩 Atividade Prática – Criando Seu Próprio CSV

1. Abra o **Bloco de Notas**.
2. Digite uma mini-tabela com **3 colunas** e **5 registros** (pode ser sobre sua turma, esportes ou Pokémons).
3. Salve como `meu_arquivo.csv`.
4. Abra no **Google Colab** e rode:

```python
meu_df = pd.read_csv("meu_arquivo.csv")
print(meu_df)
```

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- A estrutura básica de um arquivo CSV.
- Problemas comuns ao abrir CSVs em diferentes softwares.
- Como abrir e inspecionar um CSV no **Google Colab** usando Pandas.
- Como criar seu **próprio arquivo CSV**.

🔮 **Na próxima aula**: vamos aprender a **ler arquivos CSV com Pandas** de forma mais detalhada e comentada, entendendo o que é um **DataFrame** e como ele funciona.

------

#### ⏪ Voltar: Revisão e Dados Abertos

#### ⏩ Próxima Aula: Leitura de CSV com Pandas

#### 🏠 Início