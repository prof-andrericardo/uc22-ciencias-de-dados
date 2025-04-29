# 🤖 Aula 02 – Variáveis e Algoritmos de Aprendizado de Máquina

> "A máquina aprende como nós: com exemplos. Mas ela nunca esquece."  

---

## 🎯 Objetivos da Aula

- Compreender o conceito de **variáveis** dentro de conjuntos de dados.
- Identificar os tipos de variáveis: quantitativas (discretas e contínuas) e qualitativas (nominais e ordinais).
- Entender o que é **aprendizado de máquina** (machine learning) e como ele é aplicado.
- Diferenciar os tipos de aprendizado: supervisionado, não supervisionado e por reforço.
- Reconhecer os principais **algoritmos de machine learning** e suas aplicações.

---

## 📌 Introdução Didática

Você já percebeu que serviços como Spotify, Netflix e YouTube recomendam conteúdos cada vez mais parecidos com seu gosto? Ou que apps escolares conseguem prever se um aluno vai reprovar com base nas notas e faltas?

Tudo isso acontece graças a **algoritmos de aprendizado de máquina (machine learning)**, que aprendem com os dados. Mas para que esses algoritmos funcionem corretamente, eles precisam de **variáveis bem definidas**.

Nesta aula, vamos entender como classificar essas variáveis e como diferentes tipos de aprendizado funcionam na prática.

---

## 🔢 1. O que são Variáveis em Ciência de Dados?

Em um conjunto de dados (como uma planilha ou tabela de banco de dados), cada **coluna é uma variável**.

**Variáveis** são características observadas que **podem mudar de valor** entre os registros.

### 🔍 Exemplo prático (tabela de alunos):

| Nome    | Idade | Curso       | Nota Final | Aprovado |
| ------- | ----- | ----------- | ---------- | -------- |
| Carla   | 17    | Informática | 8.5        | Sim      |
| Marcelo | 18    | Informática | 5.0        | Não      |

- `Nome` → variável qualitativa
- `Idade` → variável quantitativa (discreta)
- `Nota Final` → variável quantitativa (contínua)
- `Aprovado` → variável qualitativa (booleana)
- `Curso` → qualitativa nominal

---

## 🧮 2. Tipos de Variáveis

### 2.1 🎯 Variáveis Quantitativas

Representam **valores numéricos** e podem ser divididas em dois tipos:

#### 📌 a) Variáveis Discretas

- Assumem **valores inteiros e contáveis**
- Não possuem casas decimais

**Exemplos:**

- Número de faltas
- Quantidade de dispositivos na rede
- Quantidade de commits em um projeto Git

#### 📌 b) Variáveis Contínuas

- Podem assumir **qualquer valor dentro de um intervalo**
- Possuem casas decimais

**Exemplos:**

- Altura (1.73 m)
- Temperatura (23.6 ºC)
- Velocidade da internet (30.5 Mbps)

---

### 2.2 🏷️ Variáveis Qualitativas (Categóricas)

Representam **categorias ou rótulos**, que classificam os dados em grupos.

#### 📌 a) Variáveis Nominais

- Não têm ordem entre as categorias

**Exemplos:**

- Nome do aluno
- Curso (Informática, Enfermagem, Administração)
- Cor do uniforme

#### 📌 b) Variáveis Ordinais

- Possuem **ordem ou hierarquia**

**Exemplos:**

- Grau de satisfação (Ruim, Regular, Bom, Ótimo)
- Nível de conhecimento (Básico, Intermediário, Avançado)
- Série escolar (1º, 2º, 3º ano)

---

## 🤖 3. O que é Aprendizado de Máquina (Machine Learning)?

É uma área da **Inteligência Artificial** que permite aos computadores **aprenderem a partir de dados**, sem serem explicitamente programados para cada situação.

### 💭 Analogia:

Assim como um aluno aprende a resolver problemas vendo exemplos e fazendo exercícios, a máquina aprende **com dados históricos** e **gera previsões ou decisões** com base nisso.

---

## 🧩 4. Etapas de um Projeto de Machine Learning

1. **Coleta de dados** – planilhas, bancos, sensores, APIs, etc.
2. **Limpeza e preparação** – tratar dados nulos, remover duplicatas, normalizar
3. **Escolha do algoritmo** – baseado no problema
4. **Treinamento** – a máquina "estuda" os dados
5. **Validação e Teste** – avaliar se aprendeu corretamente
6. **Implantação** – usar o modelo na prática (em apps, sistemas, dashboards)

---

## 🧠 5. Tipos de Aprendizado de Máquina

### 5.1 🎓 Aprendizado Supervisionado

- Os dados vêm **com rótulos já definidos**
- A máquina aprende **por exemplos**

**Exemplos:**

- E-mail é SPAM ou NÃO SPAM
- Prever se aluno será aprovado com base nas faltas e notas

**Algoritmos comuns:**

- Regressão linear, regressão logística
- Árvores de decisão, Random Forest
- KNN (k-vizinhos mais próximos)

---

### 5.2 🧭 Aprendizado Não Supervisionado

- Os dados **não têm rótulos**
- O sistema **descobre padrões ou agrupamentos sozinho**

**Exemplos:**

- Agrupar alunos com estilos de estudo semelhantes
- Descobrir padrões de compra em uma cantina escolar

**Algoritmos comuns:**

- K-means (agrupamento)
- PCA (análise de componentes principais)
- Apriori (regras de associação)

---

### 5.3 🧠 Aprendizado por Reforço

- O sistema **interage com o ambiente** e aprende por tentativa e erro
- Ganha **recompensas ou penalidades** com base nas ações

**Exemplos:**

- Robô que aprende a desviar de obstáculos
- Jogador automático em um jogo (IA jogando xadrez)
- Algoritmo que aprende a economizar energia em servidores escolares

---

## 🎯 6. Tarefas Comuns em Machine Learning

| Tarefa        | O que faz?                         | Exemplo escolar                    |
| ------------- | ---------------------------------- | ---------------------------------- |
| Classificação | Atribui categorias                 | Aprovado ou Reprovado              |
| Regressão     | Prediz valor numérico              | Prever nota com base em atividades |
| Clustering    | Agrupa dados parecidos             | Formar grupos de estudo            |
| Associação    | Descobre itens que aparecem juntos | Quem estuda mais → entrega tarefa  |

---

## 🧪 Atividade Prática

Crie um conjunto de dados fictício com os seguintes campos:

- Nome (String)
- Idade (Integer)
- Nota 1 e Nota 2 (Float)
- Aprovado? (Boolean)
- Curso (Qualitativa Nominal)
- Nível de Participação (Qualitativa Ordinal)

**Depois, responda:**

1. Classifique o tipo de variável de cada campo.
2. Quais dessas variáveis você usaria para prever se um aluno será aprovado?
3. Esse seria um problema de classificação ou regressão?

---

## 📚 Atividade Teórica

1. Explique a diferença entre uma variável discreta e uma contínua.
2. Dê 2 exemplos de variáveis qualitativas ordinais no ambiente escolar.
3. Associe:

| Variável                     | Tipo                  |
| ---------------------------- | --------------------- |
| Nota Final                   | Quantitativa contínua |
| Curso                        | Qualitativa nominal   |
| Frequência (%)               | Quantitativa contínua |
| Nível de satisfação          | Qualitativa ordinal   |
| Número de chamadas atendidas | Quantitativa discreta |

4. O que é aprendizado supervisionado? Dê um exemplo de aplicação em sistemas escolares.

---

## 🧩 Fixação com Modelo de Questões

🔜 Será incluído após revisão.

---

## 🔗 Referências e Recursos

- 📘 [Alura – Algoritmos de Machine Learning](https://www.alura.com.br/artigos/o-que-e-machine-learning)
- 📺 [IA na Prática – Canal YouTube](https://www.youtube.com/c/IAnaPratica)
- 📗 [Curso em Vídeo – Variáveis e Tipos de Dados](https://www.youtube.com/watch?v=2z0lmrP4Y9Q)

---

#### ⏪ [Voltar: Aula 01 – Tipos de Dados](aula01.md)  

#### ⏩ [Próxima Aula: Big Data e os 4 Vs](aula03.md)
