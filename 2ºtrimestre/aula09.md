# 📘 UC22 – Aula 9 – Projeto Prático: Análise Descritiva com Pokémons

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 6 – Aula 9 do 2º Trimestre**
 🕒 **Duração:** 45 minutos
 📍 **Tema:** Projeto prático de análise descritiva utilizando o dataset `pokemons.csv`

------

## ✨ Frase motivadora

> “Analisar dados é como explorar uma Pokédex: você descobre padrões, compara atributos e toma decisões com base em informação.” — IAra

------

## 🌟 Objetivos da Aula

- Consolidar todos os conhecimentos prévios sobre Pandas, filtragem, seleção, agrupamento, visualização e limpeza de dados.
- Aplicar esses conhecimentos em um projeto realista com base em um dataset temático.
- Desenvolver habilidades de análise, interpretação e apresentação de resultados.

------

## ✅ Etapas do Projeto

### 1. 🔄 **Preparação do Ambiente**

1. Acesse o Google Colab: https://colab.research.google.com
2. Crie um novo notebook e renomeie como: `projeto_uc22_pokemon_nome_do_aluno`
3. Importe as bibliotecas:

```python
import pandas as pd
import matplotlib.pyplot as plt
```

1. Realize o upload do arquivo `pokemons.csv` fornecido pelo professor:

```python
from google.colab import files
uploaded = files.upload()
```

1. Carregue o dataset no Pandas:

```python
df = pd.read_csv('pokemons.csv')
```

1. Visualize os dados:

```python
print(df.head())
print(df.info())
print(df.shape)
```

------

### 2. 📊 **Análises Obrigatórias**

Realize todas as análises descritas abaixo. Para cada uma, insira o código, o resultado e escreva uma conclusão em uma célula de texto.

#### a) Contagem de Pokémons por Tipo 1:

```python
print(df['Tipo 1'].value_counts())
```

#### b) Top 5 Pokémons com maior Ataque:

```python
print(df.sort_values(by='Ataque', ascending=False).head(5)[['Nome', 'Ataque']])
```

#### c) Pokémons do tipo Água com Velocidade acima de 80:

```python
print(df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 80)][['Nome', 'Velocidade']])
```

#### d) Média de HP por Tipo 1:

```python
print(df.groupby('Tipo 1')['HP'].mean().sort_values(ascending=False))
```

#### e) Gráfico de barras com quantidade de Pokémons por tipo:

```python
df['Tipo 1'].value_counts().plot(kind='bar', title='Quantidade por Tipo')
plt.xlabel('Tipo')
plt.ylabel('Quantidade')
plt.xticks(rotation=45)
plt.tight_layout()
plt.show()
```

#### f) Gráfico de pizza com os 5 tipos mais frequentes:

```python
df['Tipo 1'].value_counts().head(5).plot(kind='pie', autopct='%1.1f%%', title='Top 5 Tipos')
plt.ylabel('')
plt.tight_layout()
plt.show()
```

------

### 3. 🧹 **Limpeza e Padronização**

Realize as tarefas abaixo antes de continuar a análise:

#### a) Preencher valores nulos da coluna "Habilidade Oculta":

```python
df['Habilidade Oculta'].fillna('Não Informado', inplace=True)
```

#### b) Padronizar "Tipo 1" e "Shiny" para letras minúsculas:

```python
df['Tipo 1'] = df['Tipo 1'].str.lower()
df['Shiny'] = df['Shiny'].str.lower()
```

#### c) Corrigir "Sem gênero" para "não especificado" na coluna "Gênero":

```python
df['Gênero'] = df['Gênero'].str.lower().str.strip()
df['Gênero'] = df['Gênero'].replace('sem gênero', 'não especificado')
```

------

### 4. 🧰 **Respostas Analíticas**

Escreva respostas em linguagem natural com base nas análises feitas.

1. Qual o tipo com maior média de velocidade?
2. Qual Pokémon tem o maior valor de Defesa?
3. Existem Pokémons com Mega Evolução e Ataque acima de 100?
4. Qual a porcentagem de Pokémons com Habilidade Oculta registrada?

Use comandos como:

```python
# Exemplo para porcentagem
total = len(df)
com_ha = df[df['Habilidade Oculta'] != 'Não Informado']
print((len(com_ha) / total) * 100)
```

------

### 5. 📄 **Entrega do Projeto**

- Crie uma célula de texto com um **resumo final**: o que você descobriu? Que tipo chamou mais sua atenção? Houve alguma surpresa?
- Salve seu notebook como `.ipynb` com seu nome: `projeto_uc22_pokemon_seunome.ipynb`
- Envie pelo **Google Classroom** até a data estipulada pelo professor.

------

## 📂 Conclusão da Aula

Hoje você aplicou:

- Leitura e exploração de dados com Pandas
- Filtros condicionais e seleção de colunas
- Gráficos descritivos com Matplotlib
- Agrupamentos, contagens e estatísticas
- Padronização e limpeza de dados reais

🔧 **Próximo passo:** Apresentar as análises ou conclusões para a turma em formato de exposição oral ou em um painel colaborativo.

💪 Parabéns! Você agora entende como analisar dados como um cientista de dados iniciante!

------