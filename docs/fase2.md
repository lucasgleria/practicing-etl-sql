
## Fase 2: Construção da Lógica de ETL (O Coração do Projeto)

### O que foi feito?

- Processos de Transofmração (T) e Carga (L) dos dados: Acesse o <a href="../projeto_etl_notas/notebooks/note2.ipynb">notebook</a> para review completa
  - Exemplos de Tratamento de dados:
  ```python
  df.fillna(0) # Preenche todos os valores nulos com "0" 
  df = df.rename(columns= dc_col_names) # Renomeia as colunas
  df['nota'] = df['nota'].astype(float) # Convertendo o tipo da coluna para float
  ```
  - Exemplos de Carga de dados:
  ```python
  import sqlite3 as sql # Utilizando biblioteca sqlite3 para conectar e criar o banco de dados
  conn = sql.connect('../db/dev.db') # Cria a conexão com o banco de dados sqlite na pasta db, gerando autmomaticamente o dev.db
  df.to_sql('tabela_notas', conn, if_exists='replace', index=False) # Converte nosso DataFrame do arquivo csv em uma tabela no banco de dados SQLite
  cursor.execute("SELECT * FROM tabela_notas LIMIT 5").fetchall() # Testando se a população foi feita corretamente
  ``` 

## Processo de Desenvolvimento, passo a passo:
<a href="fase3.md"><img src="../readme-imgs/seta-verde.png" width="200"/></a>
