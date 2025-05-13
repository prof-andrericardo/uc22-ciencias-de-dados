# 📘 UC22 – Aula 7 – Limpeza e Padronização de Dados com Pandas (Pokémons)

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 4 – Aula 7 do 2º Trimestre**
 ⏱️ **Duração:** 45 minutos
 📍 **Tema:** Limpeza de dados: valores nulos, substituições e padronizações
 🧹 **Ferramentas:** Pandas
 🐍 **Nível:** Iniciantes com base consolidada

------

## ✨ Frase motivadora

> “Dados sujos geram conclusões sujas. A limpeza é a primeira etapa do verdadeiro conhecimento.” – IAra

------

## 🎯 Objetivos da Aula

- Entender a importância de **limpar e padronizar dados antes da análise**.
- Aprender a identificar e tratar **valores ausentes (nulos)**.
- Substituir valores e padronizar formatos em colunas textuais.
- Aplicar essas técnicas no dataset `pokemons.csv`.

------

## 🧠 Parte Teórica – O que é “limpeza de dados”?

Antes de fazer gráficos, filtros ou análises, é essencial **verificar se os dados estão corretos, completos e padronizados**.

Alguns problemas comuns:

- Valores ausentes ou nulos (colunas vazias)
- Inconsistências de formatação (ex: “Sim” e “sim”, “fogo” e “Fogo”)
- Colunas desnecessárias ou duplicadas
- Tipos de dados errados (ex: número como texto)

------

## 🔍 Como detectar problemas?

### 📌 Ver se há valores nulos:

```python
df.isnull()
```

- Mostra um DataFrame com `True` onde há valores nulos.
- Muito útil, mas grande.

### 📌 Contar quantos nulos existem por coluna:

```python
df.isnull().sum()
```

- Exibe um resumo por coluna.

### 📌 Ver tipos de dados:

```python
df.dtypes
```

- Isso ajuda a verificar se colunas numéricas estão sendo interpretadas como texto, por exemplo.

------

## 🛠️ Como tratar valores nulos?

### 📌 Remover linhas com valores nulos:

```python
df.dropna()
```

- Remove **qualquer linha** que tenha valor nulo em **qualquer coluna**.
- Cuidado: pode excluir muitos dados.

### 📌 Preencher valores nulos com um padrão:

```python
df['Habilidade Oculta'].fillna('Não Informado', inplace=True)
```

- Substitui valores nulos na coluna por um texto fixo.

------

## 🔁 Substituindo e padronizando valores

### 📌 Substituir valores específicos:

```python
df['Shiny'].replace('Sim', 'sim', inplace=True)
```

- Útil para padronizar letras maiúsculas/minúsculas.

### 📌 Padronizar nomes com `.str`:

```python
df['Tipo 1'] = df['Tipo 1'].str.capitalize()
```

- Torna a primeira letra maiúscula em toda a coluna.

------

## 💻 Exemplo Guiado – Google Colab

```python
import pandas as pd
from google.colab import files

uploaded = files.upload()
df = pd.read_csv('pokemons.csv')

# Verificar se há nulos
print("🔎 Valores nulos por coluna:")
print(df.isnull().sum())

# Preencher habilidade oculta com 'Não Informado'
df['Habilidade Oculta'].fillna('Não Informado', inplace=True)

# Padronizar capitalização dos tipos
df['Tipo 1'] = df['Tipo 1'].str.capitalize()
df['Tipo 2'] = df['Tipo 2'].str.capitalize()

# Padronizar a coluna Shiny
df['Shiny'] = df['Shiny'].str.lower()

# Verificar tipos de dados
print("\n🧪 Tipos de dados:")
print(df.dtypes)

# Exibir amostra dos dados
print("\n🧾 Dados atualizados:")
print(df.head())
```

------

## 💬 Atividade Teórica – Interpretação

Responda no caderno:

1. O que acontece quando usamos `dropna()`?
2. Qual a diferença entre `fillna()` e `replace()`?
3. Por que padronizar letras em colunas de texto?
4. Como saber se uma coluna tem números armazenados como texto?
5. O que significa `inplace=True`?

------

## 💻 Atividade Prática – Higienizando o Dataset Pokémon

Execute os seguintes comandos e interprete:

```python
# Contar nulos novamente após tratamento
print(df.isnull().sum())

# Exibir valores únicos em Shiny
print("Valores únicos em Shiny:", df['Shiny'].unique())

# Padronizar gênero (sem espaços e tudo minúsculo)
df['Gênero'] = df['Gênero'].str.lower().str.strip()

# Substituir 'sem gênero' por 'não especificado'
df['Gênero'] = df['Gênero'].replace('sem gênero', 'não especificado')

# Verificar os gêneros únicos agora
print("Valores únicos em Gênero:", df['Gênero'].unique())
```

------

### ✍️ Responda:

1. Após o `fillna`, quantos nulos ainda existem no DataFrame?
2. Como você padronizaria os valores da coluna “Natureza”?
3. O que você faria com uma coluna que tem 100% de valores nulos?
4. Quais colunas podem ser consideradas “categóricas”?
5. Por que é perigoso analisar dados sem limpá-los antes?

------

## 📎 Conclusão da Aula

✅ Hoje você aprendeu a:

- Detectar e tratar valores nulos.
- Padronizar formatação textual (letras, espaços, letras maiúsculas).
- Tornar os dados consistentes, legíveis e prontos para análise.

📢 **Limpar dados é como preparar o campo de batalha antes da luta:** sem isso, nenhuma análise será confiável!

------

🔮 Na próxima aula...

> Você vai criar um **mini-projeto de análise descritiva completa**, combinando todos os comandos estudados até agora: leitura, seleção, filtro, agrupamento, gráficos e limpeza.

---

#### ⏪ [Voltar: Agrupamentos, Ordenação e Gráficos](aula06.md)  
#### ⏩ [Próxima Aula: Revisão Teórica Avaliativa (com questões)](aula08.md)
#### 🏠 [Início](../README.md)
