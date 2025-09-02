# 📘 UC22 – Aula 7 – Revisão Teórica Avaliativa  

[![Python](https://img.shields.io/badge/Python-3.11+-blue?logo=python&logoColor=white)](https://www.python.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Review-green?logo=pandas)](https://pandas.pydata.org/)  
[![Google Colab](https://img.shields.io/badge/Google%20Colab-Prática-yellow?logo=googlecolab)](https://colab.research.google.com/)  
[![Tempo](https://img.shields.io/badge/Duração-90%20min-red)]()  
[![Nível](https://img.shields.io/badge/Nível-Revisão%20Intermediária-purple)]()  

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano  
🗓️ **Semana 5 – Aula 7 do 3º Trimestre**  
⏱️ **Duração:** 90 minutos  
📍 **Tema:** Revisão teórica e avaliativa dos conceitos de Pandas  
🐍 **Ferramenta principal:** Google Colab  

---

## ✨ Frase motivadora  

> “Antes de praticar com excelência, é preciso entender com clareza.” – IAra 💡  

---

## 🎯 Objetivos da Aula  

- Revisar todos os conceitos aprendidos até agora.  
- Exercitar a **interpretação de códigos** em Pandas.  
- Resolver questões teóricas, reflexivas e de múltipla escolha.  
- Preparar os alunos para o **projeto prático final**.  

---

## 🧠 Parte 1 – Interpretação de Código  

Leia o código e responda às perguntas.  

### 🔹 Exemplo 1  

```python
df[['Nome','Tipo 1','Velocidade']].sort_values(by='Velocidade', ascending=False).head(3)
```

1. O que esse comando retorna?
2. Em qual ordem os resultados aparecem?
3. Que conclusão podemos tirar dessa análise?

------

### 🔹 Exemplo 2

```python
df['Habilidade Oculta'].fillna('Não informado', inplace=True)
df['Tipo 1'] = df['Tipo 1'].str.capitalize()
```

1. O que a primeira linha faz?
2. O que muda ao aplicar `.capitalize()`?
3. Por que é importante padronizar valores textuais?

------

### 🔹 Exemplo 3

```python
df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 90)][['Nome','Velocidade']]
```

1. Qual é o objetivo desse filtro?
2. Quantas colunas o resultado tem?
3. Escreva uma **nova condição** que poderia ser aplicada.

------

## 🧠 Parte 2 – Questões Reflexivas

1. O que é um **DataFrame** e por que ele é tão importante?
2. Explique com suas palavras o que significa **limpar os dados**.
3. Quando é melhor usar `fillna()` em vez de `dropna()`?
4. Qual gráfico melhor representa proporções: barras ou pizza? Por quê?
5. Se você fosse criar um dataset da sua turma, que colunas ele teria?

------

## ✅ Parte 3 – Questões de Múltipla Escolha

1. Qual comando mostra as **5 primeiras linhas** de um DataFrame?
   -  `df.start()`
   -  `df.show()`
   -  `df.head()`
   -  `df.top()`
2. O que faz o comando `df['Tipo 1'].value_counts()`?
   -  Soma os valores da coluna
   -  Conta quantas vezes cada tipo aparece
   -  Remove valores nulos
   -  Ordena os valores da coluna
3. Qual comando usamos para **ler um arquivo CSV** no Pandas?
   -  `csv.load('arquivo.csv')`
   -  `pd.read_csv('arquivo.csv')`
   -  `open_csv('arquivo.csv')`
   -  `df.import_csv('arquivo.csv')`

------

## 📦 Parte 4 – Caixa de Seleção

1. Quais comandos podem ser usados para filtrar linhas? (marque todas as corretas)
   -  `df[df['HP'] > 100]`
   -  `df[df['Tipo 1'] == 'Fogo']`
   -  `df['HP'] == 100`
   -  `df.head(10)`
   -  `df[(df['Velocidade'] > 90) & (df['Tipo 1'] == 'Água')]`
2. Quais etapas fazem parte da limpeza de dados?
   -  Remover nulos
   -  Padronizar texto
   -  Criar gráfico de pizza
   -  Substituir valores inconsistentes
   -  Alterar tipo de dados (texto → número)

------

## 🔄 Parte 5 – Associação de Colunas

Associe corretamente os comandos e suas funções:

| Comando                                    | Função                                    |
| ------------------------------------------ | ----------------------------------------- |
| `df.info()`                                | (   ) Mostra tipos de dados e colunas     |
| `df.head()`                                | (   ) Mostra os primeiros registros       |
| `df['Tipo 1'].value_counts()`              | (   ) Conta ocorrências por categoria     |
| `df.sort_values(by='HP', ascending=False)` | (   ) Ordena os dados do maior para menor |

------

## ✔️ Parte 6 – Verdadeiro ou Falso

### Questão A

1. O comando `df.dropna()` remove linhas com nulos.
2. O método `groupby()` serve para gerar gráficos.
3. `df[['Nome','Tipo 1']]` retorna apenas duas colunas.
4. `plot(kind='bar')` cria um gráfico de barras.

-  V V V F
-  V F V V
-  F V F V
-  V F F V

------

## 📊 Atividade Extra – Estudo de Caso

Imagine que você recebeu o seguinte pedido:

> “Descubra qual tipo de Pokémon tem maior média de ataque, quais os 5 mais rápidos e quantos são do tipo Água.”

1. Que **comandos em Pandas** você usaria para responder?
2. Que tipo de **gráfico** poderia representar esses dados?
3. O que você verificaria antes de gerar os gráficos (valores nulos, consistência etc.)?

------

## 📎 Conclusão da Aula

✅ Hoje você consolidou:

- Como interpretar códigos em Pandas.
- Os principais conceitos de manipulação de dados.
- A importância da limpeza antes da análise.
- A habilidade de **raciocinar sobre dados**, não apenas rodar códigos.

🔮 **Na próxima aula**: começaremos a trabalhar em **situações-problema práticas** e aplicar os conceitos em análises mais completas.

------

#### ⏪ Voltar: Limpeza e Padronização de Dados

#### ⏩ Próxima Aula: Estudo de Caso Prático

#### 🏠 Início