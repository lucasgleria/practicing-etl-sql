## Fase 3: Análise com SQL e Documentação

### O que foi feito?

- Prática de consultas sql: Acesse o <a href="../projeto_etl_notas/notebooks/note2.ipynb">notebook</a> para review completa
```sql
SELECT curso, AVG(nota) as media_notas FROM tabela_notas GROUP BY curso -- Média de notas por curso

SELECT IdAluno, AVG(nota) as media_notas_por_aluno FROM tabela_notas GROUP BY IdAluno ORDER BY media_notas_por_aluno DESC -- Alunos com a maior média

SELECT nota, count(nota) FROM tabela_notas WHERE curso = 'matematica' GROUP BY nota -- Distribuição de notas em uma matéria específica
```


## Processo de Desenvolvimento, passo a passo:
<a href="conclusion.md"><img src="../readme-imgs/seta-verde.png" width="200"/></a>
