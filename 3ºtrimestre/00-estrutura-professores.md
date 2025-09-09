# 📊 Estrutura Geral do Curso – 3º Trimestre

**UC22 – Ciências de Dados**
 🎓 **Turma:** 3º Ano do Ensino Médio Técnico em Informática
 👨‍🏫 **Professor:** André Ricardo

------

## ⏱️ **Carga horária total**

- **20 aulas** de **90 minutos cada** (equivalente a 40 aulas de 45 minutos).
- Estrutura modular progressiva: **Revisão → Manipulação → Higienização → Consolidação → Projeto Final**.

------

## 🔹 **Módulo 1 – Revisão e Introdução ao Universo dos Dados (Aulas 1 a 3)**

🎯 **Objetivo:** Revisitar conceitos do 1º trimestre, introduzir dados abertos e primeiros contatos com CSV e Pandas.

### **Aula 1 – Revisão + Introdução a Dados Abertos**

- Relembrar: tipos de dados, variáveis, noções de Big Data.
- Introdução a **dados abertos** (IBGE, dados.gov.br, Kaggle).
- Analogia Pokémon: *“Se fôssemos cientistas da Pokémon Company, que dados seriam públicos e úteis?”*.
- **Atividade prática:** abrir um CSV simples no Google Colab (pode ser de transporte público ou ENEM).
- 🧩 **Missão Pokémon:** descubra quantos Pokémon existem no dataset inicial.

### **Aula 2 – Estrutura de Arquivos CSV**

- O que é um **CSV** (separadores, cabeçalhos, acentuação).
- Mostrar diferenças entre abrir no **Bloco de Notas**, **Excel** e **Colab**.
- **Atividade prática:** abrir `pokemons_pokedex.csv` no Colab, identificar colunas e linhas.
- 🔎 **Reflexão:** “Se os separadores mudarem, como ajustamos o código no Pandas?”.

### **Aula 3 – Primeiros Passos com Pandas**

- Comandos básicos:
  - `pd.read_csv()` → carregar dataset.
  - `df.head()` → visualizar primeiras linhas.
  - `df.info()` e `df.shape` → conhecer estrutura dos dados.
- **Atividade prática:** listar colunas do dataset Pokémon e comentar em duplas o que cada uma significa.
- 🧩 **Missão Pokémon:** descubra quantos Pokémon são Lendários.

------

## 🔹 **Módulo 2 – Manipulação de Dados (Aulas 4 a 9)**

🎯 **Objetivo:** Aprender a selecionar, filtrar, agrupar, ordenar e visualizar dados.

### **Aula 4 – Seleção de Colunas**

- Sintaxe: `df['coluna']`, `df[['colunas']]`.
- Exemplo: selecionar apenas `['Name', 'Type 1', 'Attack']`.
- **Atividade prática:** montar tabela só com `Name`, `Type 1` e `Speed`.
- 🧩 **Missão Pokémon:** descubra qual é o Pokémon mais rápido só olhando a coluna `Speed`.

### **Aula 5 – Filtros Simples**

- Operadores: `==`, `>`, `<`.
- Exemplo: selecionar todos os Pokémon do tipo Elétrico com Speed > 80.
- **Atividade prática:** montar um time de Pokémons elétricos rápidos.
- Conexão real: comparar com um filtro de planilha de notas escolares.
- 🧩 **Missão Pokémon:** quantos Pokémon do tipo Fogo têm Attack maior que 90?

### **Aula 6 – Filtros Compostos**

- Operadores: `&` (E), `|` (OU).
- Exemplo: selecionar Pokémon do tipo Água com Speed > 70 **e** Defense < 60.
- **Atividade prática:** descobrir Pokémon que têm alta defesa mas ataque baixo.
- 🧩 **Missão Pokémon:** monte um time defensivo para “segurar a batalha”.

### **Aula 7 – Agrupamentos com `groupby()`**

- Usar `groupby()` para calcular médias por tipo.
- Exemplo: média de Attack, Speed e HP por `Type 1`.
- **Atividade prática:** criar ranking de tipos mais fortes em média de Attack.
- 🧩 **Missão Pokémon:** qual tipo tem a maior média de HP?

### **Aula 8 – Ordenação com `sort_values()`**

- Sintaxe: `df.sort_values(by='coluna', ascending=False)`.
- Exemplo: ranking dos 10 Pokémon mais rápidos.
- **Atividade prática:** descobrir o Top 10 em Defense.
- Conexão real: comparar com ranking de notas na sala.
- 🧩 **Missão Pokémon:** quem é o Pokémon com maior Attack do dataset?

### **Aula 9 – Gráficos (Matplotlib)**

- Gráficos básicos:
  - Barras → comparar valores.
  - Pizza → proporções.
  - Linhas → evolução (gerações).
- **Atividade prática:** criar gráfico de barras com tipos mais comuns.
- 🧩 **Missão Pokémon:** monte um gráfico comparando Speed médio entre os tipos.

------

## 🔹 **Módulo 3 – Higienização e Padronização (Aulas 10 a 12)**

🎯 **Objetivo:** Aprender a lidar com dados nulos e padronizar informações.

### **Aula 10 – Detecção de Nulos**

- Comandos: `df.isnull().sum()`.
- **Atividade prática:** identificar colunas com valores ausentes no dataset Pokémon.
- Debate: “É melhor excluir ou preencher?”.

### **Aula 11 – Tratamento de Nulos**

- Técnicas: `dropna()` (remover) e `fillna()` (preencher).
- Exemplo: preencher valores ausentes de Speed com a média da coluna.
- **Atividade prática:** corrigir colunas incompletas do dataset.

### **Aula 12 – Padronização de Texto**

- Funções: `.str.lower()`, `.str.capitalize()`, `.replace()`.
- Exemplo: normalizar colunas `Type 1` e `Type 2`.
- **Atividade prática:** corrigir tipos inconsistentes (ex.: “fire” → “Fire”).
- 🧩 **Missão Pokémon:** padronize os nomes dos tipos e verifique quantos únicos existem.

------

## 🔹 **Módulo 4 – Consolidação e Avaliação (Aulas 13 a 16)**

🎯 **Objetivo:** Revisar, avaliar e aplicar estudo de caso.

### **Aula 13 – Revisão Geral**

- Exercícios práticos em Colab com todos os comandos vistos.
- Trabalho em duplas → cada dupla resolve 3 desafios diferentes.

### **Aula 14 – Avaliação Teórica**

- Questões objetivas e dissertativas (baseadas no modelo oficial de avaliação).
- Avaliar compreensão sobre conceitos e sintaxe.

### **Aula 15 – Estudo de Caso Pokémon**

- Questões abertas:
  - Qual geração tem mais Pokémon?
  - Quem são os 5 mais rápidos?
  - Quais tipos aparecem com maior frequência?

### **Aula 16 – Discussão Coletiva**

- Apresentação dos resultados em grupo.
- Debate sobre erros, descobertas e interpretações.

------

## 🔹 **Módulo 5 – Projeto Final: Pokédex Científica (Aulas 17 a 20)**

🎯 **Objetivo:** Produzir e apresentar o **projeto integrador** aplicando todo o conteúdo aprendido.

### **Aula 17 – Preparação**

- Explicação do projeto.
- Divisão em grupos temáticos (Ataque, Defesa, Velocidade, Tipos, Evoluções).
- Definição de papéis no grupo: programador, analista, apresentador.

### **Aula 18 – Produção das Análises**

- Cada grupo gera tabelas, gráficos e insights no Colab.
- Professor acompanha como orientador de pesquisa.

### **Aula 19 – Redação e Conclusões**

- Escrita de resultados em **linguagem natural**.
- Conexão com vida real: *como um cientista de dados escreve relatórios*.

### **Aula 20 – Apresentação Final**

- Cada grupo apresenta sua **Pokédex Científica**.
- Debate coletivo com feedback entre colegas.
- Avaliação final: conteúdo + apresentação + colaboração.
