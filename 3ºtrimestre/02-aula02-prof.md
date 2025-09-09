# 📘 UC22 – Aula 2 – Estrutura e Problemas em Arquivos CSV

*(Versão Professor – com comentários e soluções)*

[![CSV](https://img.shields.io/badge/Formato-CSV-orange?logo=file)]()
[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python\&logoColor=white)]()
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-green?logo=pandas)]()
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Notebook-yellow?logo=googlecolab)]()

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
🗓️ **Semana 1 – Aula 2 do 3º Trimestre**
⏱️ **Duração:** 90 minutos
📍 **Tema:** Estrutura, problemas e boas práticas em arquivos CSV
🐍 **Ferramenta principal:** Google Colab

---

## ✨ Abertura

💬 Sugestão pedagógica:

* Pergunte se os alunos já abriram um arquivo `.csv` no Excel ou Google Planilhas.
* Mostre que às vezes “vem tudo numa coluna só” → esse é o gancho para falar de **separadores e codificação**.

Frase no quadro:

> “Se os dados são o novo petróleo, o CSV é o barril onde eles são transportados.”

---

## 🎯 Objetivos da Aula

* Apresentar a **estrutura básica** de arquivos CSV.
* Identificar **separadores, cabeçalhos e colunas**.
* Discutir problemas comuns de **acentuação e formatação**.
* Comparar um dataset **lúdico** (Pokémon) e um dataset **real** (Censo Escolar 2023).
* Preparar para o uso de **Pandas** como ferramenta de leitura.

---

## 🧠 Parte Teórica

### Exemplo 1 – Pokémon (simples e motivador)

```csv
Nome,Tipo,HP,Ataque
Pikachu,Elétrico,35,55
Charmander,Fogo,39,52
```

💬 Use este exemplo para relembrar a ideia de **linhas** e **colunas**.

---

### Exemplo 2 – Censo Escolar 2023 (real e contextualizado)

```csv
CO_ENTIDADE,NO_ENTIDADE,TP_DEPENDENCIA,NO_MUNICIPIO
35000001,ESCOLA ESTADUAL JOÃO SILVA,Estadual,SÃO PAULO
35000002,ESCOLA ESTADUAL ANA LIMA,Estadual,SÃO PAULO
```

💬 Aqui mostre que os nomes de colunas são mais técnicos, mas representam **entidades reais** (escolas, municípios).

---

### Problemas comuns em CSV

| Problema observado                   | Causa provável             | Solução em Pandas                                 |
| ------------------------------------ | -------------------------- | ------------------------------------------------- |
| Dados em **uma única coluna**        | Separador incorreto        | `pd.read_csv('arquivo.csv', sep=';')`             |
| Acentuação quebrada (Ã, Õ, Ç errado) | Codificação diferente      | `pd.read_csv('arquivo.csv', encoding='latin-1')`  |
| Arquivo sem cabeçalho                | Exportado sem títulos      | `pd.read_csv('arquivo.csv', header=None)`         |
| Colunas desalinhadas                 | Separadores inconsistentes | `pd.read_csv('arquivo.csv', on_bad_lines='skip')` |

💬 Demonstre abrindo o mesmo CSV no **Bloco de Notas, Excel e Colab** → cada ferramenta pode interpretar de forma diferente.

---

## 💻 Parte Prática – Google Colab

### Pokémon

```python
import pandas as pd

df_poke = pd.read_csv("pokemons.csv", encoding="utf-8")
print("📊 Estrutura Pokémon:")
print(df_poke.info())
print(df_poke.head())
```

✔️ Aqui os alunos verão dados limpos e organizados.

---

### Censo Escolar

```python
df_escolas = pd.read_csv("escolas_estaduais_censo_escolar_2023.csv", encoding="latin-1", sep=",")
print("🏫 Estrutura Escolas:")
print(df_escolas.info())
print(df_escolas.head())
```

✔️ Explique que usamos `latin-1` por causa dos acentos.
✔️ Mostre que a tabela é muito maior e mais realista que a dos Pokémons.

---

## 📊 Mini-Experimento (em dupla ou trio)

1. No **Pokémon**:

   * Quantas linhas tem?
   * Cite 5 colunas.

2. No **Censo Escolar**:

   * Quantas escolas listadas (`df.shape[0]`)?
   * Cite 3 municípios diferentes (`df['NO_MUNICIPIO'].unique()[:3]`).

---

## 📝 Atividade Teórica – Gabarito

1. O que significa CSV? → *Comma-Separated Values*.
2. Função do cabeçalho? → Identificar colunas.
3. Dois problemas comuns? → Separador errado, acentuação quebrada.
4. UTF-8 → Padrão universal de codificação de caracteres.
5. Uso em ciência de dados → Simples, leve e compatível com várias ferramentas.

---

## 💻 Atividade Prática – Gabarito

```python
# Pokémon
print(df_poke.shape)        # linhas e colunas
print(df_poke.sample(5))    # 5 registros aleatórios
print(df_poke.columns[:10]) # primeiras 10 colunas

# Escolas
print(df_escolas.shape)
print(df_escolas.sample(5))
print(df_escolas.columns[:10])
```

💬 Oriente que comparem o tamanho e a complexidade entre os dois datasets.

---

## 📎 Conclusão

✅ Hoje a turma:

* Entendeu o que é um CSV.
* Identificou **problemas comuns**.
* Comparou um dataset **lúdico** (Pokémon) e um **real** (Censo Escolar).
* Percebeu a importância de **padronizar separadores e codificações**.

🔮 Próxima aula → **Pandas** e **DataFrames** (transformando CSV em estrutura inteligente para análise).

---

👉 Essa versão já traz:

* **Comentários didáticos (💬)** para guiar explicações.
* **Exemplos prontos** de gabarito.
* **Comparações entre datasets** para fixar melhor o conteúdo.
