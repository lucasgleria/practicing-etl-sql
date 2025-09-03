
### Fase 1: Configuração e Análise Inicial

O objetivo desta fase é preparar o ambiente e entender os dados que você irá trabalhar.

#### Etapa 1.1: Configuração do Ambiente
* **Subetapa 1.1.1:** Instalar o Python (se ainda não tiver).
* **Subetapa 1.1.2:** Instalar as bibliotecas necessárias: `pandas` e `Jupyter Notebook`.
    * Comando no terminal: `pip install pandas jupyter`
* **Subetapa 1.1.3:** Criar a estrutura de pastas do projeto (por exemplo, uma pasta principal `projeto_etl_notas` com subpastas `data` e `notebooks`).

#### Etapa 1.2: Aquisição e Exploração dos Dados
* **Subetapa 1.2.1:** Baixar o dataset do Kaggle e salvá-lo na pasta `data`.
* **Subetapa 1.2.2:** Abrir um novo **Jupyter Notebook** na pasta `notebooks`.
* **Subetapa 1.2.3:** Carregar o(s) arquivo(s) CSV para um `DataFrame` do `pandas`.
* **Subetapa 1.2.4:** Fazer uma análise exploratória inicial:
    * Verificar as primeiras linhas do DataFrame (`df.head()`).
    * Verificar o tipo de dados de cada coluna (`df.info()`).
    * Verificar se há valores nulos (`df.isnull().sum()`).
    * Analisar estatísticas básicas das colunas numéricas (`df.describe()`).

---

Essa Etapa foi bem simples, é mais uma fase de preparação e configuração.

### O que foi feito?

- Instalações das devidas tecnologias
- Dataset adicionado ao projeto
- Testes iniciais:
```python
import pandas as pd

dataset = '../data/student_grades.csv'
pd.read_csv(dataset)
```
- Análise exploratória inicial 
Para observar o que foi feito nessa etapa diretamente no notebook, clique <a href="../projeto_etl_notas/notebooks/note1.ipynb">aqui</a>


## Processo de Desenvolvimento, passo a passo:
<a href="fase2.md"><img src="../readme-imgs/seta-verde.png" width="200"/></a>
