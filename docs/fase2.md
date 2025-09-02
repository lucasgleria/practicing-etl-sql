
### Fase 2: Construção da Lógica de ETL (O Coração do Projeto)

Esta é a fase mais importante, onde você irá manipular os dados de acordo com os requisitos.

#### Etapa 2.1: Implementação da Transformação (T)
* **Subetapa 2.1.1:** Lidar com dados nulos. Por exemplo, preencher valores nulos de notas com `0` ou a média.
* **Subetapa 2.1.2:** Normalizar as colunas de texto (nomes de cursos, etc.) para evitar inconsistências (por exemplo, converter para letras maiúsculas ou minúsculas).
* **Subetapa 2.1.3:** Validar e corrigir os tipos de dados. Garantir que a coluna de notas seja do tipo numérico (float ou int).

#### Etapa 2.2: Implementação da Carga (L)
* **Subetapa 2.2.1:** Criar uma conexão com o banco de dados **SQLite** dentro do seu Notebook.
* **Subetapa 2.2.2:** Definir o nome da tabela que irá receber os dados, por exemplo, `tabela_notas`.
* **Subetapa 2.2.3:** Utilizar o `pandas` para carregar o DataFrame já tratado para a tabela SQLite.
    * `df_tratado.to_sql('tabela_notas', conn, if_exists='replace', index=False)`
* **Subetapa 2.2.4:** Verificar se a tabela foi criada e populada corretamente, executando uma simples consulta SQL (`SELECT * FROM tabela_notas LIMIT 5`).



## Processo de Desenvolvimento, passo a passo:
<a href="fase3.md"><img src="../readme-imgs/seta-verde.png" width="200"/></a>
