# 📘 UC22 – Aula 6 – Limpeza e Padronização de Dados (Pokémons)  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Cleaning-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Intermediário-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 4 – Aula 6 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Limpeza e padronização de dados reais com Pandas  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Dados sujos geram conclusões sujas. A limpeza é o primeiro passo para o verdadeiro conhecimento.” – IAra 🧹  

---

## 🎯 Objetivos da Aula  

- Entender a importância de **limpar e padronizar dados**.  
- Detectar e tratar **valores nulos** (`NaN`).  
- Substituir valores inconsistentes.  
- Padronizar colunas textuais (maiúsculas/minúsculas).  
- Preparar o dataset Pokémon para análises confiáveis.  

---

## 🧠 Parte Teórica – Por que limpar dados?  

Problemas comuns em datasets reais:  
- ❌ **Valores ausentes** → colunas incompletas.  
- ❌ **Inconsistências de escrita** → “Sim”, “sim”, “SIM”.  
- ❌ **Tipos errados** → número armazenado como texto.  
- ❌ **Dados duplicados** → mesma linha registrada mais de uma vez.  

👉 Sem corrigir esses problemas, qualquer análise pode levar a conclusões erradas.  

---

## 🧠 Detectando problemas  

### 🔹 Verificar valores nulos  

```python
df.isnull().sum()
```

✅ Mostra a quantidade de valores ausentes em cada coluna.

------

### 🔹 Verificar tipos de dados

```python
df.dtypes
```

✅ Útil para identificar se colunas numéricas estão como texto.

------

### 🔹 Ver valores únicos em uma coluna

```python
df['Shiny'].unique()
```

✅ Permite verificar inconsistências (“Sim”, “sim”, “não”).

------

## 💻 Parte Prática – Tratando Dados no Colab

### 🔹 Exemplo 1 – Remover valores nulos

```python
df_sem_nulos = df.dropna()
```

⚠️ Remove todas as linhas que possuem algum valor nulo.
 ➡️ Cuidado: pode apagar muitos dados.

------

### 🔹 Exemplo 2 – Preencher valores nulos

```python
df['Habilidade Oculta'].fillna('Não Informado', inplace=True)
```

✅ Substitui valores vazios por um texto padrão.

------

### 🔹 Exemplo 3 – Padronizar textos

```python
df['Tipo 1'] = df['Tipo 1'].str.lower()
df['Shiny'] = df['Shiny'].str.strip().str.lower()
```

✅ Agora todos os valores ficam uniformes em **letras minúsculas**.

------

### 🔹 Exemplo 4 – Substituir valores específicos

```python
df['Gênero'] = df['Gênero'].replace('sem gênero', 'não especificado')
```

✅ Torna a coluna mais clara e padronizada.

------

## 📊 Mini-Experimento Pokémon

Execute e responda:

```python
# 1. Quantos valores nulos havia em cada coluna?
print(df.isnull().sum())

# 2. Preencha valores nulos de Natureza
df['Natureza'].fillna('Desconhecida', inplace=True)

# 3. Padronize a coluna Tipo 2
df['Tipo 2'] = df['Tipo 2'].str.capitalize()

# 4. Veja os valores únicos de Shiny
print(df['Shiny'].unique())
```

Perguntas:

1. Qual coluna tinha mais valores nulos?
2. Após padronizar, quantos valores únicos existem em “Shiny”?
3. Qual a vantagem de substituir em vez de apagar dados?

------

## 💬 Atividade Teórica – Questões no caderno

1. O que acontece se usamos `dropna()`?
2. Explique a diferença entre `fillna()` e `replace()`.
3. Por que padronizar letras em colunas de texto?
4. O que significa `inplace=True`?
5. Cite um exemplo da vida real em que **dados inconsistentes** podem causar problemas.

------

## 🧩 Atividade Prática – “Limpando sua Pokédex”

🎮 Desafio no Colab:

- Padronize todos os **tipos Pokémon** para minúsculas.
- Substitua valores nulos em “Habilidade Oculta” por **“Não informado”**.
- Padronize os valores de **Gênero** (minúsculo, sem espaços extras).
- Conte quantos Pokémons ficaram com “Habilidade Oculta = Não informado”.

📌 Escreva uma **conclusão em texto**:

> “Após a limpeza, percebi que a coluna ___ tinha muitos valores nulos. Agora o dataset está mais consistente e pronto para análise.”

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu:

- A detectar valores nulos e inconsistências.
- A usar `dropna()`, `fillna()` e `replace()`.
- A padronizar colunas textuais no Pandas.
- Que limpar dados é **indispensável** antes de qualquer análise.

🔮 **Na próxima aula**: vamos revisar e consolidar os conceitos aprendidos com **questões avaliativas teóricas e interpretativas**.

------

#### ⏪ Voltar: Agrupamento, Ordenação e Gráficos

#### ⏩ Próxima Aula: Revisão Teórica Avaliativa

#### 🏠 Início