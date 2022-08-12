# Estudo Pandas

## Aula 01 - Nessa aula:

Lemos um json com a função read_json() para buscar os nomes das alunas e alunos

Juntamos os nomes masculinos e femininos com a função concat() e transformamos em um novo DataFrame com o comando to_frame()

Inserimos um id para identificar melhor cada pessoa

## Aula 02 - Nessa aula:

Lemos uma tabela de uma página html com a função read_html(), passando a url como parâmetro para buscar os nomes dos cursos

Transformamos o retorno dessa função em um DataFrame com o código cursos = cursos[0]

Criamos um ID para cada curso e setamos o index para ser o id com o código cursos = cursos.set_index('id')

## Aula 03 - Nessa aula:

Criamos uma nova coluna no DataFrame nomes chamada matriculas para representar quantos cursos cada pessoa está matriculada

Geramos um novo DataFrame matriculas para representar qual curso cada aluno está matriculado

Fizemos um join dos DataFrames matriculas e cursos para exibir a quantidade de alunos em cada curso

Vimos como ler e escrever um DataFrame em diferentes tipos: csv, json e html

## Aula 04 - Nessa aula:

Aprendemos como utilizar o pandas para ler e escrever em um banco sql

Utilizamos o banco SQLite que vem com o pandas e criamos um banco local

Salvamos o DataFrame de matriculas com o comando matriculas_por_curso.to_sql('matriculas', engine)

Lemos uma tabela do banco com a função read_sql_table() e exibimos o resultado de uma query com o comando read_sql(), passando a query como parâmetro

## Aula 05 - Nessa aula:

Escolhemos um curso e selecionamos todas as pessoas matriculadas nele

Exportamos o DataFrame para o tipo excel com o comando proxima_turma.to_excel('proxima_turma.xlsx', index=False)

Para verificar se o DataFrame estava certo, lemos o arquivo excel com o comando pd.read_excel('proxima_turma.xlsx')