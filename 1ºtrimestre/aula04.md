# 🛠️ Aula 04 – Pipeline de Dados: Como Organizar a Jornada dos Dados

> "Sem organização, até os dados mais valiosos se tornam confusão."  

---

## 🎯 Objetivos da Aula

- Entender o que é um **Pipeline de Dados** e sua importância.
- Conhecer as etapas de um pipeline: ingestão, transformação, armazenamento e análise.
- Visualizar como dados fluem em projetos de Ciência de Dados e Engenharia de Dados.
- Reconhecer boas práticas na construção de pipelines eficientes.
- Aplicar os conceitos em situações reais do ambiente escolar e cotidiano.

---

## 📌 Introdução Didática

Imagine a linha de montagem de uma fábrica: peças entram em uma ponta, passam por processos de ajuste, pintura, verificação, até saírem prontas para uso.

👉 Com os **dados** acontece o mesmo! Eles saem de diversas fontes, são transformados, armazenados e analisados.  
Esse caminho é chamado de **Pipeline de Dados**.

Na aula de hoje, vamos entender como construir e organizar **essa linha de produção de dados**!

---

## 🏗️ 1. O que é um Pipeline de Dados?

Um **Pipeline de Dados** é o conjunto de **processos automáticos e organizados** que capturam, transformam, armazenam e analisam dados de forma eficiente.

É a **espinha dorsal** de qualquer projeto de Ciência de Dados ou Engenharia de Dados.

---

### 💬 Analogias do Dia a Dia:

- Linha de montagem de um carro 🚗
- Processamento de fotos para postar no Instagram 📷
- Atualização automática de presenças no sistema escolar 🏫

---

## 🔄 2. Estágios do Pipeline de Dados

### 2.1 🚰 Ingestão de Dados (Data Ingestion)

**O que é:**  
Capturar dados de diversas fontes e levar para um ambiente de processamento.

**Exemplos:**

- Importar notas de uma planilha do Google Sheets para um banco de dados.
- Receber dados de presença em tempo real via aplicativo escolar.

**Formas de ingestão:**

- **Batch (em lote):** Captura em grandes blocos, ex: todo final de dia.
- **Streaming (contínuo):** Captura em tempo real, ex: chamada em sala online.

**Ferramentas comuns:**

- Apache Nifi
- Apache Kafka
- Logstash
- Python (scripts de coleta)

---

### 2.2 🛠️ Transformação de Dados (Data Transformation)

**O que é:**  
Preparar os dados para uso, corrigindo, limpando e organizando.

**Exemplos práticos:**

- Corrigir datas que estavam no formato errado (`01/03/25` ➔ `2025-03-01`).
- Remover registros duplicados de chamadas.
- Converter "Sim" / "Não" para `True` / `False` (booleano).

**Ferramentas comuns:**

- Python (Pandas)
- SQL
- Apache Spark
- dbt (data build tool)

---

### 2.3 💾 Armazenamento de Dados (Data Storage)

**O que é:**  
Guardar os dados de forma segura e eficiente para serem consultados ou analisados.

**Tipos de armazenamento:**

- **Bancos de dados relacionais:** MySQL, PostgreSQL (dados estruturados)
- **Data Warehouses:** BigQuery, Redshift (grandes volumes organizados para análise)
- **Data Lakes:** Amazon S3, Hadoop HDFS (armazenam dados em qualquer formato)

**Critérios importantes:**

- Segurança
- Rapidez nas consultas
- Capacidade de crescimento (escalabilidade)

---

### 2.4 📈 Análise de Dados (Data Analysis)

**O que é:**  
Extrair conhecimento útil dos dados armazenados.

**Tipos de análise:**

- **Descritiva:** O que aconteceu? (ex: "Quantos alunos faltaram em março?")
- **Diagnóstica:** Por que aconteceu? (ex: "As faltas aumentaram após uma semana de provas?")
- **Preditiva:** O que pode acontecer? (ex: "Quais alunos estão em risco de reprovação?")
- **Prescritiva:** O que devemos fazer? (ex: "Aplicar reforço escolar?")

**Ferramentas comuns:**

- Power BI
- Tableau
- Python (Pandas, Seaborn, Scikit-Learn)

---

## 🗺️ 3. Representação Visual de um Pipeline

```text
[Fonte de Dados] 
    ↓
[Ingestão] → [Transformação] → [Armazenamento] → [Análise]
```

### 🎯 Ferramentas para automação:

- **Apache Airflow**
- **Prefect**

------

## 🛡️ 4. Boas Práticas na Criação de Pipelines

- **Automatizar:** Evita erros humanos e acelera o processo.
- **Monitorar:** Use alertas para detectar falhas rapidamente.
- **Documentar:** Anote as transformações feitas para facilitar a manutenção.
- **Validar em cada etapa:** Impede que erros pequenos virem problemas grandes.
- **Dividir em módulos:** Torna o pipeline mais fácil de entender e corrigir.

------

## 🧩 5. Pipeline x ETL x ELT

| Característica         | ETL (Tradicional)             | ELT (Moderno)                 | Pipeline de Dados        |
| ---------------------- | ----------------------------- | ----------------------------- | ------------------------ |
| Ordem                  | Extrai ➔ Transforma ➔ Carrega | Extrai ➔ Carrega ➔ Transforma | Flexível e personalizado |
| Local da transformação | Fora do banco                 | Dentro do banco               | Pode ser híbrido         |
| Melhor para            | Pequenos/ médios volumes      | Grandes volumes e nuvem       | Qualquer cenário         |

------

## 📚 6. Exemplo Prático Aplicado

**Cenário:**
 A escola quer analisar a frequência dos alunos.

**Pipeline:**

1. **Ingestão:** Captura de dados de presença via Google Forms.
2. **Transformação:** Conversão de "Presente/Ausente" para 1/0.
3. **Armazenamento:** Dados salvos em uma base MySQL.
4. **Análise:** Dashboard no Power BI mostrando a frequência semanal.

**Resultado:**
 A direção pode agir rapidamente para apoiar as turmas com maior índice de faltas.

------

## 🧪 Atividade Prática

🎯 **Desafio: Monte um Pipeline Escolar**

1. Escolha um cenário, exemplo: controle de tarefas entregues.
2. Defina:
   - Fonte de dados
   - Etapa de ingestão
   - Que transformações seriam necessárias
   - Onde armazenaria
   - Que tipo de análise faria

Apresente o seu pipeline usando o esquema:

```text
[Fonte de Dados] → [Ingestão] → [Transformação] → [Armazenamento] → [Análise]
```

------

## 📚 Atividade Teórica

1. Explique a diferença entre um pipeline de dados e um simples upload manual de arquivos.
2. Por que a etapa de transformação é tão importante antes de armazenar os dados?
3. Associe:

| Etapa do Pipeline | Exemplo                       |
| ----------------- | ----------------------------- |
| Ingestão          | Importar notas via formulário |
| Transformação     | Corrigir erros de digitação   |
| Armazenamento     | Salvar em banco MySQL         |
| Análise           | Criar relatório no Power BI   |

1. Cite duas ferramentas para cada etapa de um pipeline:

| Etapa         | Ferramenta 1 | Ferramenta 2    |
| ------------- | ------------ | --------------- |
| Ingestão      | Apache Nifi  | Python (Pandas) |
| Transformação | dbt          | Apache Spark    |
| Armazenamento | MySQL        | BigQuery        |
| Análise       | Power BI     | Tableau         |

------

## 🔗 Referências e Recursos

- 📘 [O que é Pipeline de Dados? – Alura](https://www.alura.com.br/artigos/o-que-e-pipeline-de-dados)
- 📺 [Data Pipeline explicado em 10 minutos – Canal Código Fonte TV](https://www.youtube.com/watch?v=3fF4srz5saY)
- 📚 [Guia Completo sobre ETL vs ELT – Data Science Academy](https://www.datascienceacademy.com.br/blog/etl-vs-elt-diferencas/)

------

#### ⏪ Voltar: Aula 03 – Big Data e os 4 Vs

#### ⏩ Próxima Aula: Visualização de Dados

