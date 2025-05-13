# 📘 UC22 – Aula 3 – Introdução aos Arquivos CSV

🎓 **Curso:** Ensino Médio Técnico em Informática – 3º Ano
 🗓️ **Semana 2 – Aula 3 do 2º Trimestre**
 ⏱️ **Duração:** 45 minutos

------

## ✨ Frase motivadora

> “Se os dados são o novo petróleo, o CSV é o barril onde eles são transportados.” – Anônimo da TI

------

## 🎯 Objetivos da Aula

- Compreender o que é um arquivo CSV e como ele armazena dados.
- Identificar e interpretar colunas, linhas e separadores em arquivos CSV.
- Abrir arquivos `.csv` corretamente em diferentes ferramentas: bloco de notas, Excel e Google Planilhas.
- Identificar problemas comuns (acentuação, separadores, cabeçalhos) ao abrir arquivos CSV.

------

## 🧠 Parte Teórica – O que é um CSV?

### 📌 Definição

**CSV** significa **Comma-Separated Values** (Valores Separados por Vírgula). É um tipo de arquivo **simples, leve e muito usado em ciência de dados** para armazenar **tabelas de dados**.

- Cada linha do arquivo representa **um registro (linha da tabela)**
- Cada valor é separado por **vírgulas** (ou ponto e vírgula em alguns casos)
- A primeira linha geralmente contém o **nome das colunas** (cabeçalho)

------

### 🧩 Exemplo de arquivo `.csv`:

```csv
nome,idade,nota_final,frequente
João,18,7.5,sim
Larissa,17,9.1,sim
Carlos,19,4.5,não
```

| Linha | Conteúdo da Linha                 | Explicação                   |
| ----- | --------------------------------- | ---------------------------- |
| 1     | `nome,idade,nota_final,frequente` | Cabeçalho: nomes das colunas |
| 2     | `João,18,7.5,sim`                 | Registro 1 (aluno João)      |
| 3     | `Larissa,17,9.1,sim`              | Registro 2                   |
| 4     | `Carlos,19,4.5,não`               | Registro 3                   |

------

### 📌 Variações e problemas comuns

| Situação                                       | Causa provável                            |
| ---------------------------------------------- | ----------------------------------------- |
| Os dados aparecem em uma única coluna no Excel | Separador incorreto (ponto e vírgula `;`) |
| Acentos aparecem como “Ã”, “Õ”                 | Problema de codificação (UTF-8 vs ANSI)   |
| Falta de cabeçalho                             | Arquivo exportado sem linha de títulos    |
| Colunas desorganizadas                         | Separador ausente ou errado               |

------

## 💬 Atividade Teórica – Interpretação de Estrutura CSV

Leia o trecho abaixo de um arquivo `.csv` fictício:

```csv
id,nome,série,nota_final,aprovado
101,Ana Paula,3ºA,8.6,True
102,Breno Santos,3ºB,4.9,False
103,Carla Dias,3ºA,6.2,True
```

**Responda no caderno:**

1. Quantas colunas existem?
2. Qual o tipo de dado de cada coluna? (int, string, float, boolean)
3. Qual coluna representa a turma do aluno?
4. Qual aluno não foi aprovado?
5. A coluna "nota_final" representa qual tipo de variável? (quantitativa discreta ou contínua?)
6. A coluna "aprovado" representa qual tipo de dado e de variável?
7. Existe alguma informação categórica? Qual?
8. Quantas linhas de dados existem (sem contar o cabeçalho)?
9. Qual é o identificador único de cada aluno neste exemplo?
10. Se fosse representar esses dados graficamente, qual gráfico seria adequado para “nota_final” por “série”?

------

## 💻 Atividade Prática – Visualizando e Explorando CSV Manualmente

### 📝 Enunciado:

Você irá abrir **um arquivo CSV real** utilizando diferentes ferramentas para analisar a estrutura e organização dos dados. Use um dos arquivos baixados da aula anterior ou utilize um exemplo fornecido pelo professor.

### 🧩 Passos:

#### Parte 1 – Bloco de Notas (ou Editor de Texto)

1. Clique com o botão direito sobre o arquivo `.csv` e selecione **“Abrir com > Bloco de Notas”**.
2. Observe:
   - Como os valores estão separados?
   - Há aspas? Acentos? Títulos?

#### Parte 2 – Excel ou Google Planilhas

1. Abra o mesmo arquivo com o Excel ou Google Planilhas.
2. Verifique:
   - Os dados foram organizados corretamente em colunas?
   - Há problemas com acentuação ou caracteres especiais?
   - As colunas possuem nomes significativos?

#### Parte 3 – Preenchimento no Caderno (ou planilha)

Anote os seguintes pontos:

- Nome do arquivo
- Ferramenta usada para abrir
- Quantas colunas e linhas tem o arquivo?
- Cite 3 colunas com seus tipos de dados.
- Identifique pelo menos 1 problema ou dificuldade que você notou.
- Sugira um nome melhor para uma coluna que ficou pouco clara.

------

## 📎 Conclusão da Aula

- O formato `.csv` é fundamental na ciência de dados por ser simples, leve e compatível com quase todas as ferramentas.
- Compreender sua estrutura é essencial para preparar dados antes de análises.
- Na próxima aula, você irá **carregar e manipular esses arquivos usando Python com a biblioteca Pandas.**

------

## 📚 Para a próxima aula...

> Crie uma pasta chamada `dados_uc22` no seu computador ou Drive e mova o arquivo `.csv` trabalhado hoje para essa pasta.
>  Também leve seu notebook (se tiver) e instale o **Google Chrome** para usar o **Google Colab**.

------
