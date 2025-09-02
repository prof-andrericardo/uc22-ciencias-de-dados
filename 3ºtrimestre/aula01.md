# 📘 UC22 – Aula 1 – Revisão e Introdução a Dados Abertos  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Iniciante➜Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 1 – Aula 1 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Revisão dos fundamentos + Introdução a Dados Abertos  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Dados são o combustível do futuro. Quem sabe analisá-los, cria o futuro.” – IAra 🚀  

---

## 🎯 Objetivos da Aula  

- Revisar os **fundamentos do 2º Trimestre** (tipos de dados, variáveis, pipeline, visualização).  
- Entender o que são **dados abertos** e sua importância na sociedade.  
- Explorar **portais oficiais de dados abertos** (INEP, IBGE, Dados.gov, Kaggle).  
- Aprender a abrir e interpretar um arquivo `.csv` em diferentes ferramentas.  
- Preparar o ambiente no **Google Colab** para os próximos projetos.  

---

## 🧠 Parte Teórica – Revisão dos Fundamentos  

### 📌 Tipos de Dados  

| Tipo       | Explicação                      | Exemplo (cotidiano)          |
| ---------- | ------------------------------- | ---------------------------- |
| `int`      | Número inteiro                  | idade = `17`                 |
| `float`    | Número com casas decimais       | nota final = `8.75`          |
| `string`   | Texto (sequência de caracteres) | nome = `"Ana Júlia"`         |
| `boolean`  | Verdadeiro/Falso                | aprovado = `True` ou `False` |
| `datetime` | Datas e horários                | matrícula = `2025-02-10`     |

---

### 📌 Pipeline de Dados  

🔄 O caminho que os dados percorrem até se tornarem informação útil:  

```text
[Fonte de dados] → [Coleta] → [Transformação] → [Armazenamento] → [Análise] → [Visualização]
```

------

### 📌 Visualização de Dados

- 📊 **Gráfico de barras** → comparar categorias.
- 📈 **Gráfico de linhas** → analisar evolução no tempo.
- 🥧 **Gráfico de pizza** → proporção entre partes.

------

## 🌍 Parte Teórica – O que são Dados Abertos?

📖 **Definição:**
 Dados abertos são informações públicas que podem ser **livremente acessadas, utilizadas e compartilhadas** por qualquer pessoa.

📌 **Exemplos reais de uso:**

- 🏫 **INEP**: notas do ENEM e indicadores educacionais.
- 🌍 **IBGE**: censos demográficos e mapas populacionais.
- 🚍 **EMTU/SP**: rotas e horários de transporte público.
- 🎮 **Kaggle**: datasets de projetos do mundo todo (Pokémon, esportes, redes sociais, etc.).

------

## 💻 Parte Prática – Preparando o Ambiente no Google Colab

### 🔹 Passo 1 – Acessar o Colab

1. Abra 👉 [Google Colab](https://colab.research.google.com)
2. Clique em **“+ Novo notebook”**
3. Renomeie para: `UC22_Aula01.ipynb`

------

### 🔹 Passo 2 – Testando o Python

```python
# Primeiro código no Colab
print("Olá, Cientista de Dados Pokémon! ⚡")
```

✅ Resultado esperado:

```
Olá, Cientista de Dados Pokémon! ⚡
```

------

### 🔹 Passo 3 – Criando um Mini-Exemplo

```python
# Criando listas de alunos e notas
alunos = ["Ana", "Carlos", "Lívia"]
notas = [8.5, 6.2, 9.1]

# Exibindo pares aluno-nota
for i in range(len(alunos)):
    print(f"{alunos[i]} → Nota: {notas[i]}")
```

✅ Saída esperada:

```
Ana → Nota: 8.5
Carlos → Nota: 6.2
Lívia → Nota: 9.1
```

------

## 📊 Mini-Projeto da Aula – Importando Dados

🎯 **Desafio:** Acesse o portal [dados.gov.br](https://dados.gov.br) e baixe um dataset em formato `.csv`.

### Etapa 1 – Identifique

- 📛 Nome do dataset
- 🏛️ Órgão responsável
- 📏 Quantidade de colunas e linhas
- 📝 Três colunas e seus significados

------

### Etapa 2 – Abra no Google Colab

#### ✅ Opção A – Upload direto no Colab

```python
import pandas as pd
from google.colab import files

# Upload manual (abre janela para escolher o CSV)
uploaded = files.upload()

# Ler o arquivo (substitua pelo nome correto)
df = pd.read_csv("nome_do_arquivo.csv")
df.head()
```

------

#### ✅ Opção B – Usando o Google Drive

```python
from google.colab import drive
import pandas as pd

# Montar o Google Drive
drive.mount('/content/drive')

# Ler o arquivo salvo no Drive
df = pd.read_csv("/content/drive/MyDrive/dados_uc22/meu_dataset.csv")
df.info()
```

------

### Etapa 3 – Comparação

Responda em um parágrafo:

1. Qual forma foi mais rápida para você?
2. Qual delas é mais prática para um projeto longo?
3. Se fosse trabalhar em grupo, qual usaria? Por quê?

------

## 📝 Atividade Teórica – Google Docs

1. O que são dados abertos? Cite um exemplo do cotidiano.
2. Qual a diferença entre **int** e **float**?
3. Dê um exemplo de **variável categórica** e uma **numérica**.
4. Explique por que é importante ter **dados padronizados**.
5. Se você fosse criar um dataset Pokémon, que colunas colocaria nele?

📌 **Instruções:**

- Responda em um **Google Docs**.
- Nomeie o arquivo: `UC22_Aula01_Teoria_NomeDoAluno`.
- Entregue no **Google Sala de Aula**.

------

## 💻 Atividade Prática – Google Colab

📌 Pegue o arquivo `pokemons.csv` (fornecido pelo professor).

1. Abra no **Bloco de Notas** → observe vírgulas e acentos.
2. Abra no **Excel/Google Planilhas** → confira colunas e linhas.
3. Abra no **Google Colab com Pandas** → rode:

```python
df.info()
df.shape
```

1. Compare as visualizações → o que mudou?

📌 **Instruções:**

- Salve como: `UC22_Aula01_Pratica_NomeDoAluno.ipynb`.
- Entregue no **Google Sala de Aula**.

------

## 📎 Conclusão da Aula

✅ Hoje você revisou:

- Fundamentos da Ciência de Dados.
- O que são dados abertos e onde encontrá-los.
- Como abrir datasets `.csv` em diferentes ferramentas.
- Como preparar o ambiente no **Google Colab**.

🔮 **Na próxima aula**: vamos aprofundar na **estrutura dos arquivos CSV** e entender problemas comuns (acentuação, separadores e cabeçalhos).

------

## 📌 Entrega obrigatória no Google Sala de Aula

- Arquivo **Google Docs** com respostas teóricas.
- Arquivo **Google Colab (.ipynb)** com exercícios práticos.

------

#### 🏠 Voltar ao Início

#### ⏩ Próxima Aula: Estrutura e Problemas em Arquivos CSV
