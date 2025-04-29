# 📘 UC22 – Aula 8 – Análise Teórica e Avaliativa: Consolidando os Conceitos

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 5 – Aula 8 do 2º Trimestre**
 🕒 **Duração:** 45 minutos
 📍 **Tema:** Consolidação teórica dos conceitos de Pandas aplicados ao dataset Pokémon
 🧠 **Foco:** Interpretação, raciocínio lógico e capacidade analítica

------

## ✨ Frase motivadora

> “Antes de praticar com excelência, é preciso entender com clareza.” – IAra

------

## 🌟 Objetivos da Aula

- Revisar os principais conceitos das aulas anteriores.
- Desenvolver o raciocínio analítico por meio da interpretação de códigos e situações reais.
- Diagnosticar dúvidas e lacunas antes de iniciar o projeto prático.
- Promover reflexão crítica sobre o uso da ciência de dados com datasets estruturados.

------

> 📋 **Instrução geral:** Leia cada questão com atenção. Use seu caderno ou um documento digital para registrar suas respostas. Caso tenha dúvidas, marque para discussão em sala.

------

## 🧠 Parte 1 – Interpretação de Código

### ➤ Objetivo: Explicar o comportamento de comandos em Python

### Trecho 1:

```python
df = pd.read_csv('pokemons.csv')
df[['Nome', 'Tipo 1', 'Velocidade']].sort_values(by='Velocidade', ascending=False).head(3)
```

1. O que esse trecho retorna?
2. Qual a ordem dos resultados?
3. Que tipo de informação poderíamos extrair desses dados?

### Trecho 2:

```python
df['Habilidade Oculta'].fillna('Não Informado', inplace=True)
df['Tipo 1'] = df['Tipo 1'].str.capitalize()
```

1. Qual é a função da primeira linha?
2. O que muda com a aplicação de `.capitalize()`?
3. Por que essa padronização é importante em um dataset?

### Trecho 3:

```python
df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 90)][['Nome', 'Velocidade']]
```

1. Qual é o objetivo dessa filtragem?
2. Quantas colunas o resultado terá?
3. Escreva outra condição lógica que poderia ser usada aqui.

------

## 🧠 Parte 2 – Questões Reflexivas

### ➤ Objetivo: Compreensão crítica e contextualizada

1. O que é um DataFrame e por que ele é usado na ciência de dados?
2. Qual a importância da limpeza dos dados antes da análise?
3. Em que situações devemos preferir `fillna()` ao invés de `dropna()`?
4. Como podemos visualizar graficamente a distribuição de uma variável categórica?
5. Explique o que significa agrupar os dados por tipo e calcular a média de ataque.

------

## 📋 Parte 3 – Situação Problema (Estudo de Caso)

### ➤ Objetivo: Aplicar o raciocínio de análise exploratória

Imagine que você recebeu o seguinte pedido:

> *“Queremos saber qual tipo de Pokémon tem maior média de velocidade, quais os 3 Pokémons com maior ataque e quais tipos são mais frequentes.”*

Descreva:

1. Quais comandos você usaria para responder essa pergunta?
2. Qual tipo de gráfico seria o mais indicado para apresentar os resultados?
3. O que você verificaria antes de gerar os gráficos (ex: dados faltantes, inconsistência)?

------

## 🔪 Parte 4 – Questões Dissertativas

🖊️ 1. Explique, com suas palavras, a diferença entre um `DataFrame` e um arquivo `.csv`. Destaque o papel da biblioteca Pandas e os tipos de operações que podemos fazer com um DataFrame.
 🖊️ 2. Por que é importante limpar os dados antes de analisá-los? Cite pelo menos três tipos de problemas que podem existir em um dataset e como isso pode afetar a análise.

------

## ✅ Parte 5 – Questões de Múltipla Escolha (Apenas uma correta)

1. Qual comando é utilizado para **visualizar as 5 primeiras linhas** de um DataFrame?
   - [ ] `df.tail()`
   - [ ] `df.start()`
   - [ ] `df.show()`
   - [ ] `df.head()`
2. O que faz o comando `df['Tipo 1'].value_counts()`?
   - [ ] Calcula a soma dos ataques por tipo
   - [ ] Retorna apenas os tipos numéricos
   - [ ] Conta quantas vezes cada valor aparece na coluna “Tipo 1”
   - [ ] Remove valores nulos da coluna “Tipo 1”
3. Qual dos seguintes comandos é usado para ler um arquivo CSV com Pandas?
   - [ ] `open_csv('arquivo.csv')`
   - [ ] `pd.read_csv('arquivo.csv')`
   - [ ] `csv.load('arquivo.csv')`
   - [ ] `import pandas as csv`

------

## 📦 Parte 6 – Caixa de Seleção (Várias respostas corretas)

1. Quais comandos abaixo podem ser usados para **filtrar linhas em um DataFrame**?
    ( ) `df[df['HP'] > 100]`
    ( ) `df[df['Tipo 1'] == 'Fogo']`
    ( ) `df['HP'] == 100`
    ( ) `df[(df['Tipo 1'] == 'Água') & (df['Velocidade'] > 80)]`
    ( ) `df.head(5)`
    ( ) `df.mean()`
2. Em uma análise de dados, **quais etapas fazem parte da limpeza de dados?**
    ( ) Remover valores nulos
    ( ) Padronizar texto (maiúsculas e minúsculas)
    ( ) Criar gráficos de pizza
    ( ) Substituir valores inconsistentes
    ( ) Executar loops com `for`
    ( ) Alterar tipos de dados (ex: de texto para número)

------

## 🔄 Parte 7 – Associação de Colunas

### Associação 1:

| Nº   | Comando                                    | Finalidade                                       |
| ---- | ------------------------------------------ | ------------------------------------------------ |
| A    | `df.info()`                                | (   ) Mostra os primeiros registros do DataFrame |
| B    | `df.head()`                                | (   ) Mostra os tipos de dados e colunas         |
| C    | `df['Tipo 1'].value_counts()`              | (   ) Conta ocorrências por categoria            |
| D    | `df.sort_values(by='HP', ascending=False)` | (   ) Ordena os dados do maior HP ao menor       |

### Associação 2:

| Nº   | Operação                                          | Propósito                                         |
| ---- | ------------------------------------------------- | ------------------------------------------------- |
| A    | `df['Tipo 1'].str.capitalize()`                   | (   ) Agrupa os dados e calcula valores médios    |
| B    | `df.groupby('Tipo 1')['HP'].mean()`               | (   ) Padroniza capitalização das strings         |
| C    | `df['Habilidade Oculta'].fillna('Não Informado')` | (   ) Cria gráfico de distribuição por categoria  |
| D    | `df['Tipo 1'].value_counts().plot(kind='bar')`    | (   ) Substitui valores ausentes com texto padrão |

------

## ✔️ Parte 8 – Verdadeiro ou Falso (Sequência única)

### Questão A:

1. O comando `df.dropna()` remove linhas com valores nulos.
2. O método `groupby()` serve para gerar gráficos.
3. `df[['Nome', 'Tipo 1']]` retorna apenas as colunas especificadas.
4. Um gráfico de barras pode ser criado com `plot(kind='bar')`.

Sequências:

- [ ] F V V F
- [ ] V F F V
- [ ] V F V V
- [ ] V V V F

### Questão B:

1. O método `fillna()` é utilizado para criar novas colunas com dados gerados.
2. O comando `groupby()` pode ser usado para calcular a média de uma coluna por categoria.
3. `df['Shiny'].str.lower()` transforma os valores da coluna em letras minúsculas.
4. `df[['HP', 'Velocidade']].mean()` calcula a média das colunas numéricas indicadas.

Sequências:

- [ ] V F F V
- [ ] F F V V
- [ ] F V F V
- [ ] F V V V

------

## 📂 Conclusão da Aula

✅ Hoje você consolidou:

- A lógica por trás de comandos em Pandas.
- A importância de estruturar mentalmente a análise antes de escrever o código.
- A relação entre código, intenção e resultado final.

📀 Esta aula servirá de base para o **Projeto Prático da próxima aula**, onde você irá aplicar os conceitos para realizar uma análise descritiva real com base nos Pokémons.