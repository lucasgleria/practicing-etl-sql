# Projeto de Engenharia de Dados: Análise de Notas Acadêmicas

## 1\. Visão Geral do Projeto

Este documento detalha o planejamento e os requisitos para um projeto prático de engenharia de dados, com foco em **SQL** e **ETL (Extração, Transformação, Carga)**, utilizando Python e tecnologias gratuitas. O objetivo é simular um pipeline de dados, partindo de um dataset bruto de notas acadêmicas e transformando-o em uma base de dados limpa e pronta para análise.

-----

## 2\. Requisitos do Projeto

### 2.1 Requisitos do Negócio (Objetivo)

  * **Objetivo Principal:** Criar um banco de dados limpo e organizado com informações de notas acadêmicas para permitir análises. O objetivo é simular um processo real de ETL, onde você pega dados brutos e os prepara para serem consultados.
  * **Resultados Esperados:**
    1.  Um script Python que execute todo o processo de ETL, desde a extração até a carga dos dados.
    2.  Um banco de dados populado (usando SQLite) com uma tabela de `notas` limpa e pronta para uso.
    3.  Consultas SQL de exemplo para demonstrar a utilidade da base de dados.

### 2.2 Requisitos Funcionais (O que o sistema deve fazer)

  * **Extração (E):** O script Python deve ser capaz de ler os dados de um arquivo CSV (ou de múltiplos arquivos).
  * **Transformação (T):**
      * Lidar com valores nulos nas colunas de notas ou IDs.
      * Normalizar as colunas de texto (ex: nomes de cursos) para garantir consistência.
      * Garantir que as colunas de notas e IDs sejam do tipo numérico.
  * **Carga (L):** O script deve criar uma tabela no banco de dados SQLite e carregar os dados transformados nela. A tabela pode se chamar `notas_tratadas`.
  * **Análises (SQL):** Você deve ser capaz de responder a perguntas como:
      * Qual a média de notas por curso?
      * Quais alunos tiveram a maior média geral?
      * Quais cursos têm a maior taxa de reprovação?
      * Qual a distribuição de notas em uma matéria específica?

### 2.3 Requisitos de Tecnologia (Ferramentas)

  * **Linguagem:** Python
  * **Bibliotecas Python:** `pandas` (para ETL) e `sqlite3` (para o banco de dados).
  * **Banco de Dados:** **SQLite**.
  * **Ambiente:** Jupyter Notebook (para desenvolvimento e documentação).

-----

## 3\. Plano de Implementação Completo

A implementação será dividida em três fases principais, usando a abordagem "dividir para conquistar".

### Fase 1: Configuração e Análise Inicial

  * **Etapa 1.1: Configuração do Ambiente**
      * Instalar Python.
      * Instalar as bibliotecas necessárias: `pip install pandas jupyter`.
      * Criar a estrutura de pastas do projeto: `projeto_etl_notas/data`, `projeto_etl_notas/notebooks`, `projeto_etl_notas/database`.
  * **Etapa 1.2: Aquisição e Exploração dos Dados**
      * Baixar o dataset do Kaggle (com temática de notas acadêmicas) e salvar na pasta `data`.
      * Abrir um novo **Jupyter Notebook**.
      * Carregar o arquivo CSV para um `DataFrame` do `pandas`.
      * Realizar uma análise exploratória inicial para entender a estrutura dos dados, tipos de colunas e presença de valores nulos.

### Fase 2: Construção da Lógica de ETL

  * **Etapa 2.1: Implementação da Transformação (T)**
      * Usar `pandas` para tratar valores nulos nas colunas de notas.
      * Normalizar os nomes dos cursos para um formato consistente.
      * Converter colunas de notas e IDs para o tipo numérico correto.
  * **Etapa 2.2: Implementação da Carga (L)**
      * Criar uma conexão com o banco de dados **SQLite**.
      * Carregar o `DataFrame` tratado para uma nova tabela (`notas_tratadas`) no banco de dados.
      * Verificar a carga com uma consulta SQL simples (`SELECT * FROM notas_tratadas LIMIT 5;`).

### Fase 3: Análise com SQL e Documentação

  * **Etapa 3.1: Execução das Análises (SQL)**
      * Escrever e executar as consultas SQL para responder às perguntas-chave definidas nos requisitos funcionais.
      * Analisar os resultados de cada consulta.
  * **Etapa 3.2: Finalização e Documentação**
      * Adicionar comentários detalhados ao longo do Notebook explicando cada etapa do ETL e as consultas SQL.
      * Escrever uma introdução e conclusão para o projeto, descrevendo o objetivo, a metodologia e os resultados.
      * Salvar o Notebook final e o banco de dados SQLite.

-----

### Exemplo de Estrutura de Pastas

```
projeto_etl_notas/
├── data/
│   └── notas_brutas.csv
├── notebooks/
│   └── etl_analise.ipynb
├── database/
│   └── notas.db
├── README.md
└── .gitignore
```