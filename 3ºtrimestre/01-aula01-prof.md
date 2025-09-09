# 📘 UC22 – Aula 1 – Revisão e Introdução a Dados Abertos

*(Versão Professor – com comentários e soluções)*

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python\&logoColor=white)]()
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)]()
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)]()
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()
[![Nível](https://img.shields.io/badge/Nível-Iniciante➜Intermediário-purple)]()

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
🗓️ **Semana 1 – Aula 1 do 3º Trimestre**
⏱️ **Duração:** 90 minutos
📍 **Tema:** Revisão dos Fundamentos + Introdução a Dados Abertos
🐍 **Ferramenta principal:** Google Colab

---

## ✨ Abertura

💬 **Dica pedagógica:** inicie perguntando aos alunos:

* Onde eles já viram planilhas com muitos dados? (Escola, futebol, games, Enem etc.)
* Qual a importância de **organizar** e **compartilhar** informações?

Isso ativa o conhecimento prévio e prepara para o conceito de **dados abertos**.

📢 Frase motivadora para escrever no quadro:

> “Dados são o combustível do futuro. Quem sabe analisá-los, cria o futuro.” – IAra 🚀

---

## 🎯 Objetivos da Aula

* Relembrar conceitos do **2º trimestre** (tipos de dados, variáveis, pipeline).
* Introduzir o conceito de **dados abertos**.
* Explorar o portal [dados.gov.br](https://dados.gov.br).
* Abrir e analisar um **dataset real** (`escolas_estaduais_censo_escolar_2023.csv`).
* Configurar o ambiente no **Google Colab**.

---

## 🧠 Parte Teórica

### Tipos de Dados (revisão rápida)

💬 Sugira exemplos ligados ao cotidiano dos alunos:

* `int` → idade, número de Pokémons capturados.
* `float` → nota do boletim.
* `string` → nome do aluno, apelido.
* `boolean` → aprovado (True/False).
* `datetime` → data de matrícula, dia do jogo.

---

### Pipeline de Dados

Mostre o esquema no slide/quadro:

```text
[Fonte de dados] → [Coleta] → [Transformação] → [Armazenamento] → [Análise] → [Visualização]
```

💡 Explique que o curso neste trimestre percorrerá exatamente esse caminho.

---

### Dados Abertos

💬 Sugestão:

* Abra em sala o portal **dados.gov.br**.
* Mostre um exemplo de dataset (INEP, IBGE, escolas, transporte público).

📌 Enfatize que **qualquer pessoa** pode usar esses dados, inclusive eles.

---

## 💻 Parte Prática – Google Colab

### Passo 1 – Primeiro código

```python
print("Olá, Cientista de Dados! 🚀")
```

💬 Use esse momento para descontrair e mostrar que programação pode ser divertida.

---

### Passo 2 – Upload e Leitura do Dataset

```python
import pandas as pd
from google.colab import files

# Upload manual do CSV fornecido
uploaded = files.upload()

# Leitura do arquivo
df = pd.read_csv("escolas_estaduais_censo_escolar_2023.csv", encoding="latin-1")
df.head()
```

💡 **Comentário didático:**

* Explique o parâmetro `encoding="latin-1"` (necessário para lidar com acentuação em português).
* Se o aluno tiver problema de separador, lembre do `sep=";"`.

---

### Passo 3 – Primeira exploração

```python
df.info()      # Estrutura do dataset
df.shape       # Linhas e colunas
df.columns[:5] # Mostra primeiras colunas
```

💬 Explique:

* `info()` mostra tipos de dados e nulos.
* `shape` mostra a dimensão (n\_linhas, n\_colunas).
* `columns` revela nomes das colunas.

---

### Passo 4 – Mini-investigação

```python
print("Total de escolas:", df.shape[0])
print("Colunas principais:", df.columns[:3])
print(df.sample(5))  # Amostra aleatória
```

---

## 📊 Mini-Projeto da Aula

**Desafio prático:**

* Descobrir o número total de escolas listadas.
* Identificar quantas colunas existem.
* Verificar em qual município aparecem mais escolas (usando `value_counts()` – só mostrar se der tempo).

```python
df['MUNICIPIO'].value_counts().head(5)
```

---

## 📝 Atividade Teórica (Google Docs) – Gabarito

1. O que são dados abertos? → Informações públicas, acessíveis e reutilizáveis.
2. Cite um portal oficial de dados abertos no Brasil. → `dados.gov.br`.
3. Diferença entre `int` e `float`. → Inteiro vs número decimal.
4. Exemplo categórica vs numérica. → Gênero da escola (categórica), número de alunos (numérica).
5. Colunas em dataset escolar. → Nome, município, nº alunos, etapas oferecidas etc.

---

## 💻 Atividade Prática (Google Colab) – Gabarito

1. `df.head()` → exibe primeiras linhas.
2. `df.shape[0]` → total de escolas.
3. `df.columns[9]` → mostra a 10ª coluna.
4. `df.sample(5)` → cinco linhas aleatórias.

---

## 📎 Conclusão

✅ Hoje a turma:

* Revisou fundamentos da ciência de dados.
* Descobriu o conceito de **dados abertos**.
* Manipulou pela primeira vez um **CSV real** do Brasil.
* Explorou o ambiente **Google Colab** com Pandas.

📢 Reforce: *“Não precisamos decorar código, precisamos aprender a interpretar dados.”*

🔮 Próxima aula → Estrutura e problemas em arquivos CSV.

---

👉 Professor, esta versão já traz:

* **Comentários didáticos** (💬).
* **Soluções sugeridas** para atividades.
* **Expansão opcional** com `value_counts()` para aprofundar se houver tempo.
