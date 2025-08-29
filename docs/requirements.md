_Primeiro passo foi trackear os requisitos do nosso caso de uso, tanto os de negócio, como funcionais e tecnologias_

---

### 1. Requisitos do Negócio (Objetivo)

* **Objetivo Principal:** Criar um banco de dados limpo e organizado com informações de notas acadêmicas para permitir análises. O objetivo é simular um processo real de **ETL**, onde você pega dados brutos e os prepara para serem consultados.
* **Resultados Esperados:**
    1.  Um script Python que execute todo o processo de ETL, desde a extração até a carga dos dados.
    2.  Um banco de dados populado (usando SQLite) com uma tabela de `notas` limpa e pronta para uso.
    3.  Algumas consultas SQL de exemplo para demonstrar a utilidade da base de dados.

---

### 2. Requisitos Funcionais (O que o sistema deve fazer)

* **Extração (E):** O script Python deve ser capaz de ler os dados de um arquivo CSV (ou de múltiplos arquivos, se o dataset tiver essa estrutura).
* **Transformação (T):**
    * **Limpeza:** Lidar com possíveis valores nulos nas colunas de notas ou IDs.
    * **Normalização:** Garantir que o formato das notas (por exemplo, de 0 a 10 ou de A a F) seja consistente. Se houver nomes de cursos inconsistentes (`Algoritmos` vs `algoritmos`), normalizá-los.
    * **Tipagem de Dados:** Garantir que as colunas de notas e IDs sejam do tipo numérico.
* **Carga (L):** O script deve criar uma tabela no banco de dados SQLite e carregar os dados transformados nela. A tabela pode se chamar `notas_tratadas` ou algo similar, para indicar que já passou pelo processo de ETL.
* **Análises (SQL):** Você deve ser capaz de responder a perguntas como:
    * Qual a média de notas por curso?
    * Quais alunos tiveram a maior média geral?
    * Quais cursos têm a maior taxa de reprovação (assumindo uma nota de corte)?
    * Qual a distribuição de notas em uma matéria específica?

---

### 3. Requisitos de Tecnologia (Ferramentas)

* **Linguagem:** Python
* **Bibliotecas Python:**
    * **`pandas`:** Essencial para a fase de **Transformação**. É a ferramenta padrão para manipulação e limpeza de dados.
    * **`sqlite3`:** Biblioteca nativa do Python para interagir com bancos de dados SQLite. Você pode usar também o `sqlalchemy` para uma abordagem mais flexível.
* **Banco de Dados:** **SQLite**. É a melhor escolha para este projeto de prática, pois é um banco de dados embutido em um arquivo, leve e não requer configuração de servidor.
* **Ambiente de Desenvolvimento:** Um **Notebook Jupyter** é altamente recomendado. Ele permite que você execute cada passo do seu ETL e documente a lógica e os resultados de forma visual, o que é ótimo para o aprendizado e para mostrar seu projeto.



## Processo de Desenvolvimento, passo a passo:
<a href="implementation.md"><img src="../readme-imgs/seta-verde.png" width="200"/></a>
