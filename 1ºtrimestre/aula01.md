# 📊 Aula 01 – Tipos de Dados: O Alicerce da Ciência de Dados

> "Entender os dados é o primeiro passo para mudar o mundo com tecnologia."  
> — Adaptado de Tim Berners-Lee

---

## 🎯 Objetivos da Aula

- Compreender o que são dados no contexto da Ciência de Dados.
- Classificar os dados em estruturados, semiestruturados e não estruturados.
- Identificar os tipos de dados primitivos: integer, float, string, boolean e datetime.
- Interpretar estruturas de tabelas de dados reais.
- Aplicar corretamente os conceitos por meio de atividades teóricas e práticas.

---

## 📌 Introdução Didática

Se você já preencheu um formulário online, analisou uma planilha com notas da escola ou usou um app que registra sua frequência, você já trabalhou com **dados**. A **Ciência de Dados** é uma área que transforma essas informações brutas em conhecimento prático.

Mas para que a mágica da ciência de dados aconteça, precisamos de uma base sólida. Nesta aula, vamos aprender a **identificar e classificar os tipos de dados**, algo fundamental para manipular informações com qualidade e precisão.

---

## 🔍 1. O que são Dados?

**Dados** são representações digitais de informações do mundo real. Eles podem ser:

- Um número de matrícula 🧾
- Um nome completo 📛
- Uma data de nascimento 📆
- Uma resposta sim ou não ❓
- Um vídeo de aula 📹

Em Ciência de Dados, os dados são o combustível. Eles alimentam sistemas que ajudam empresas a tomar decisões, médicos a prever doenças, professores a analisar o desempenho da turma, e até mesmo aplicativos a recomendar a próxima música que você vai ouvir.

---

## 🧱 2. Classificação Geral dos Dados

### 2.1 📊 Dados Estruturados

São dados organizados **em tabelas com linhas e colunas**, onde cada coluna possui um tipo fixo. São comuns em bancos de dados e planilhas.

#### 💡 Exemplos:

- Uma planilha com as notas dos alunos da turma
- O histórico de presença armazenado em um sistema escolar
- Tabelas do MySQL com cadastro de usuários e senhas

#### ✅ Características:

- Fácil de consultar com SQL
- Excelente para análise com Pandas (Python)
- Armazenados em: MySQL, PostgreSQL, Google Sheets

---

### 2.2 🧾 Dados Semiestruturados

São dados que possuem **alguma organização interna**, como marcadores ou chaves, mas **não seguem um esquema fixo** como uma tabela.

#### 💡 Exemplos:

- Um arquivo JSON com dados de um aluno:

```json
{
  "nome": "Bruna Costa",
  "idade": 17,
  "curso": "Informática"
}
```

- Logs de acesso ao sistema escolar com timestamp e mensagem
- XML de dados da chamada da aula

#### ✅ Características:

- Flexíveis, mas ainda legíveis por máquina
- Comuns em APIs e integração entre sistemas

------

### 2.3 🌀 Dados Não Estruturados

Esses dados **não têm estrutura definida** e exigem técnicas avançadas para análise.

#### 💡 Exemplos:

- Uma imagem da sala de aula capturada por câmera
- Um vídeo de uma aula gravada
- Comentários dos alunos sobre a aula em redes sociais
- Arquivos PDF com contratos escolares

#### ✅ Características:

- Difíceis de indexar
- Demandam ferramentas como IA e aprendizado profundo (Deep Learning)

------

## 🔢 3. Tipos Primitivos de Dados

Agora que você já sabe o formato estrutural, vamos detalhar os **tipos primitivos**, que são a forma básica de representação dos dados.

### 🧮 Integer (Inteiro)

- Representa números **sem casas decimais**
- Usado para contagem, códigos, identificação

#### Exemplos:

- Número de faltas: `3`
- ID do aluno: `1024`
- Total de aulas: `40`

------

### 📐 Float (Ponto Flutuante)

- Representa números com **casas decimais**
- Usado para medidas e valores fracionários

#### Exemplos:

- Nota de avaliação: `8.5`
- Altura: `1.73`
- Temperatura: `24.7`

------

### 🔤 String (Texto)

- Representa **sequências de caracteres**
- Usado para nomes, códigos, endereços

#### Exemplos:

- Nome: `"Carlos Eduardo"`
- Curso: `"Informática"`
- CPF: `"123.456.789-00"`

------

### 🔘 Boolean (Lógico)

- Representa dois estados possíveis: **True/False**, **1/0**, **Sim/Não**

#### Exemplos:

- Entregou o trabalho? `True`
- Está ativo no sistema? `False`
- Compareceu à aula? `1`

------

### 📅 Datetime (Data e Hora)

- Representa **datas, horários ou ambos**
- Usado para registros temporais

#### Exemplos:

- Data de nascimento: `2007-03-15`
- Horário da chamada: `08:05:00`
- Registro: `2025-04-01T13:40:00`

------

## 🗂️ 4. Estrutura Típica de uma Tabela de Dados

| ID   | Nome             | Data Nasc. | Presente? | Nota Final |
| ---- | ---------------- | ---------- | --------- | ---------- |
| 1    | Ana Carolina     | 2006-09-14 | True      | 8.3        |
| 2    | Felipe dos Anjos | 2007-01-22 | False     | 5.0        |

🔎 Classificação por coluna:

- `ID` → Integer
- `Nome` → String
- `Data Nasc.` → Datetime
- `Presente?` → Boolean
- `Nota Final` → Float

------

## 🧠 Conclusão

Saber o tipo certo para cada dado evita erros como:

- Tentar somar nomes (!)
- Comparar datas como se fossem textos (!)
- Usar textos em gráficos numéricos (!)

Dominar esses conceitos é **essencial para tudo que vem depois**: análise, visualização, aprendizado de máquina, dashboards e muito mais!

------

## 🧪 Atividade Prática (em dupla ou trio)

Crie uma tabela no seu caderno ou Google Sheets com **10 registros simulados** da sua sala contendo as seguintes colunas:

- ID (Integer)
- Nome (String)
- Idade (Integer)
- Nota Final (Float)
- Compareceu na última aula? (Boolean)
- Data da Avaliação (Datetime)

Depois, classifique **cada coluna** quanto ao **tipo de dado**.

------

## 📚 Atividade Teórica

Responda com atenção:

1. Explique com suas palavras o que são dados estruturados e dê 2 exemplos reais.
2. Por que não é possível aplicar a função `média()` em uma coluna `String`?
3. Um arquivo `.json` pode ser considerado estruturado? Justifique.
4. Associe corretamente:

| Tipo de Dado | Exemplo Real no Colégio |
| ------------ | ----------------------- |
| Float        | Nota da prova           |
| Boolean      | Compareceu à aula?      |
| String       | Nome do aluno           |
| Integer      | Número de chamada       |
| Datetime     | Data da entrega do TCC  |

------

## 🧩 Fixação com Modelo de Questões

🔜 Será abordado após revisão do professor.

------

## 🔗 Referências e Recursos

- 📘 [Curso em Vídeo – Tipos de Dados](https://www.youtube.com/watch?v=4tf2uA9R1gA)
- 🐍 [Documentação Python – Tipos de Dados](https://docs.python.org/pt-br/3/library/stdtypes.html)
- 📄 [Artigo Alura – Classificando Dados](https://www.alura.com.br/artigos/o-que-e-estrutura-de-dados)

------

#### ⏪ Voltar ao README do Trimestre

#### ⏩ Próxima Aula: Variáveis e Algoritmos de Aprendizado de Máquina
