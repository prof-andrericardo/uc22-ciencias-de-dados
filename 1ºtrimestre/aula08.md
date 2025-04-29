# 🔢 Aula 08 – Dados Booleanos e Classificação de Colunas: Organizando a Base dos Dados

> "Quem domina os tipos de dados tem a chave para interpretar o mundo digital."  

---

## 🎯 Objetivos da Aula

- Entender o que são **dados booleanos** e suas diversas representações.
- Aprender como identificar e padronizar **valores booleanos** em tabelas de dados.
- Compreender como classificar colunas em um conjunto de dados.
- Praticar a organização e a interpretação correta de dados para análises futuras.

---

## 📌 Introdução Didática

Você já respondeu "Sim" ou "Não" a uma pergunta online? Já viu campos como "Usuário ativo: True" ou "Presença: 1"?  
Esses são exemplos de **dados booleanos**!

No universo da Ciência de Dados, **saber identificar e classificar corretamente** cada tipo de informação é essencial para realizar análises corretas e tomar boas decisões.

Hoje vamos aprender a reconhecer os dados booleanos e a **classificar as colunas** dos conjuntos de dados que manipulamos, seja em projetos escolares, sistemas, bancos de dados ou aplicativos.

---

## ✅ 1. O que são Dados Booleanos?

**Dados booleanos** representam **dois estados possíveis**:  
🟢 Verdadeiro (True) ou 🔴 Falso (False)

Esses estados podem aparecer de diversas formas, dependendo do contexto.

---

### Exemplos de representações booleanas:

| Contexto                                   | Valor Verdadeiro | Valor Falso |
| ------------------------------------------ | ---------------- | ----------- |
| Python                                     | `True`           | `False`     |
| SQL (MySQL, PostgreSQL)                    | `1`              | `0`         |
| Excel                                      | `VERDADEIRO`     | `FALSO`     |
| Interfaces de usuário (sistemas escolares) | `Sim`            | `Não`       |
| Aplicativos de presença                    | `Presente`       | `Ausente`   |

---

### 📚 Aplicações práticas:

- 📅 **Presença ou falta** nas aulas.
- 🔒 **Conta ativa ou inativa** em sistemas acadêmicos.
- 🧾 **Pagamento realizado ou pendente** em mensalidades escolares.
- 🎯 **Tarefa entregue ou não entregue** em projetos de programação.

---

## 🧩 2. Como Representar e Padronizar Booleanos

🔵 Em projetos profissionais ou escolares é fundamental **padronizar** como o booleano será representado.

**Por quê?**  
Misturar "Sim/Não", "1/0" e "True/False" na mesma planilha pode gerar confusão e erros de análise!

**Dicas de padronização:**

- Escolha uma forma única (ex: sempre usar `1` para Verdadeiro e `0` para Falso).
- Documente no cabeçalho ou legenda o que cada valor significa.

---

## 🗂️ 3. Classificação de Colunas em Tabelas de Dados

Cada **coluna** de uma tabela representa **um tipo específico de dado**.  
Classificá-las corretamente facilita:

- Aplicar filtros
- Fazer cálculos corretos
- Treinar modelos de machine learning de forma eficaz

---

### Principais tipos de colunas:

| Nome da Coluna       | Tipo de Dado       | Justificativa                                 |
| -------------------- | ------------------ | --------------------------------------------- |
| Número do Pedido     | Categórico/String  | Identificador único, não para cálculos        |
| Data da Compra       | Data/Hora          | Representa um momento temporal                |
| Estado               | Categórico         | Categoria geográfica                          |
| Categoria do Produto | Categórico         | Classificação por tipo                        |
| Quantidade           | Numérico (Inteiro) | Valor contável (número inteiro)               |
| Valor da Compra      | Numérico (Float)   | Valor monetário com casas decimais            |
| Enviado              | Booleano           | Indica se foi enviado (Sim/Não ou True/False) |

---

## 🔍 4. Exemplos de Aplicação no Dia a Dia

### 🎒 Exemplo 1 – Identificar Coluna Boolean

| Número do Pedido | Categoria        | Enviado |
| ---------------- | ---------------- | ------- |
| 001              | Material Escolar | Yes     |
| 002              | Mochilas         | No      |

🧠 Pergunta: **Qual coluna é do tipo booleano?**  
Resposta: ✅ "Enviado" (porque só pode ser "Yes" ou "No").

---

### 📚 Exemplo 2 – Classificar Colunas em um Cadastro Escolar

| ID do Aluno | Nome do Aluno | Curso       | Nota Final | Presente? |
| ----------- | ------------- | ----------- | ---------- | --------- |
| 1           | Ana Beatriz   | Informática | 9.2        | Sim       |
| 2           | Lucas Vieira  | Enfermagem  | 7.8        | Não       |

**Classificação:**

- ID do Aluno → Categórico (String ou código)
- Nome do Aluno → String
- Curso → Categórico
- Nota Final → Float
- Presente? → Booleano

---

## 🎯 5. Boas Práticas com Dados Booleanos

- Evite misturar representações ("1/0", "Sim/Não", "Ativo/Inativo") em uma mesma tabela.
- Documente claramente o que cada valor representa.
- Prefira usar tipos booleanos nativos nas ferramentas, em vez de textos.
- Valide se os valores realmente representam apenas duas possibilidades.

---

## 🧠 6. Conclusão

Saber **identificar, padronizar e classificar** dados booleanos é crucial para garantir a integridade dos projetos de Ciência de Dados.

🔍 Desde uma chamada de aula, um cadastro em sistema, até grandes análises de vendas, **os booleanos estão em todo lugar!**

**Quem domina a organização dos dados já está um passo à frente na Ciência de Dados.**

---

## 🧪 Atividade Prática

🎯 **Desafio: Detectando Booleanos**

Dada a tabela abaixo:

| Produto | Estoque | Disponível para Venda |
| ------- | ------- | --------------------- |
| Livro   | 20      | Yes                   |
| Caderno | 0       | No                    |
| Mochila | 5       | Yes                   |

1. Classifique o tipo de dado de cada coluna.
2. Qual coluna representa um dado booleano?
3. Se você fosse padronizar "Disponível para Venda", como faria?

---

## 📚 Atividade Teórica

1. Defina o que são dados booleanos.
2. Associe corretamente:

| Dado Representado    | Tipo de Dado       |
| -------------------- | ------------------ |
| "Presente"/"Ausente" | Booleano           |
| 15 faltas            | Numérico (Inteiro) |
| "Curso: Informática" | Categórico         |
| 9.75 (nota)          | Numérico (Float)   |

3. Explique a importância de padronizar dados booleanos em uma base de dados.

4. Dê dois exemplos de erros que podem ocorrer se os dados booleanos não forem padronizados.

---

## 🔗 Referências e Recursos

- 📘 [Documentação SQL – Tipos de Dados Booleanos](https://dev.mysql.com/doc/refman/8.0/en/boolean-type.html)
- 📺 [Booleanos em Python – Canal Curso em Vídeo](https://www.youtube.com/watch?v=_uQrJ0TkZlc)
- 📚 [Artigo Alura – Tipos de Dados na Análise de Dados](https://www.alura.com.br/artigos/tipos-de-dados-na-analise-de-dados)

---

#### ⏪ [Voltar: Aula 07 – Habilidades e Ferramentas em Ciência de Dados](aula07.md)  

#### ⏩ [Próxima Aula: Guia de Estudo para Avaliação Trimestral](aula09.md)
