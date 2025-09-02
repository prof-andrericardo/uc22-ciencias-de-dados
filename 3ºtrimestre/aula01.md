# 📘 UC22 – Aula 1 – Revisão e Introdução a Dados Abertos  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Iniciante%20➜%20Intermediário-purple)]()  

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
- Entender o que são **dados abertos** e por que são importantes na sociedade.  
- Explorar **portais oficiais de dados abertos** (INEP, IBGE, Dados.gov, Kaggle).  
- Aprender a abrir e interpretar um arquivo `.csv` em diferentes ferramentas.  
- Preparar o ambiente no **Google Colab** para o trimestre.  

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

1. Abra: 👉 [Google Colab](https://colab.research.google.com)
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

## 📊 Mini-Projeto da Aula 1 – Importando Dados do dados.gov.br  

🎯 **Desafio:** Acesse o portal [dados.gov.br](https://dados.gov.br) e baixe um dataset em formato `.csv`.  
Você vai aprender duas formas diferentes de abrir esse arquivo no **Google Colab**:  

1. Fazendo o **upload direto** do arquivo.  
2. Montando o **Google Drive** no Colab.  

---

### 🔹 Etapa 1 – Exploração do Dataset  

Antes de abrir no Colab, identifique no dataset baixado:  

- 📛 Nome do dataset  
- 🏛️ Órgão responsável  
- 📏 Quantidade de colunas e linhas  
- 📝 Três colunas e seus significados  

---

### 🔹 Etapa 2 – Abrindo o CSV no Google Colab  

#### ✅ Opção A – Upload direto no Colab  

Esse é o jeito **mais simples e rápido** de carregar o arquivo.  
Você faz o upload do CSV diretamente para a sessão atual do Colab.  

```python
import pandas as pd
from google.colab import files

# Upload manual do arquivo (vai abrir uma janela para escolher o CSV)
uploaded = files.upload()

# Ler o arquivo CSV (substitua pelo nome correto do arquivo)
df = pd.read_csv("nome_do_arquivo.csv")

# Visualizar as 5 primeiras linhas
df.head()
```

📌 Observação: essa forma é prática, mas o arquivo **não fica salvo** no Colab.
 Se você fechar a aba, terá que fazer o upload novamente.

------

#### ✅ Opção B – Usando o Google Drive

Esse é o jeito **mais organizado e profissional**.
 Você salva o CSV em uma pasta do Google Drive e monta o Drive no Colab.

```python
from google.colab import drive
import pandas as pd

# Montando o Google Drive
drive.mount('/content/drive')

# Caminho até o arquivo salvo no seu Google Drive
df = pd.read_csv("/content/drive/MyDrive/dados_uc22/meu_dataset.csv")

# Visualizar informações gerais
df.info()
```

📌 Observação: aqui o arquivo **fica salvo** no seu Drive.
 Mesmo que você feche o Colab, poderá acessá-lo na próxima vez.

------

### 🔹 Etapa 3 – Comparação das Abordagens

No seu caderno (ou em uma célula de texto no Colab), responda:

1. Qual das duas formas foi mais rápida para você?
2. Qual delas parece mais prática para **um projeto longo**?
3. Você percebeu alguma diferença no código de leitura (`read_csv`)?
4. Se fosse fazer uma análise em grupo, qual abordagem usaria? Justifique.

------

### 🔹 Etapa 4 – Reflexão Final

📢 Escreva uma conclusão:

> “No meu caso, preferi a abordagem ___ porque ___.
> Aprendi que o Colab permite tanto uploads rápidos quanto o uso organizado de pastas no Google Drive.”

------

✅ Com isso, você já domina as **duas principais formas de importar dados no Colab**!
 Esse conhecimento será usado em **todo o restante do trimestre**.

------

## 💬 Atividade Teórica – Responda no caderno

1. O que são dados abertos? Cite um exemplo do cotidiano.
2. Qual a diferença entre **int** e **float**?
3. Dê um exemplo de **variável categórica** e uma **numérica**.
4. Explique por que é importante ter **dados padronizados**.
5. Se você fosse criar um dataset Pokémon, que colunas colocaria nele?

------

## 🧩 Atividade Prática – Explorando CSV

📌 Pegue o arquivo `pokemons.csv` (fornecido pelo professor).

1. Abra no **Bloco de Notas** → observe as vírgulas e acentos.
2. Abra no **Excel/Google Planilhas** → confira colunas e linhas.
3. Abra no **Google Colab** com Pandas → rode `df.info()` e `df.shape()`.
4. Compare as visualizações → o que mudou?

------

## 📎 Conclusão da Aula

✅ Hoje você revisou:

- Fundamentos da Ciência de Dados.
- O que são dados abertos e onde encontrá-los.
- Como abrir datasets `.csv` em diferentes ferramentas.
- Como preparar o ambiente no **Google Colab**.

🔮 **Na próxima aula**: vamos aprofundar na **estrutura dos arquivos CSV** e entender como os dados são armazenados, seus problemas e variações.

------

#### [🏠 Voltar ao Início](./README.md)

#### [⏩ Próxima Aula: Estrutura e Problemas em Arquivos CSV](./aula02.md)

