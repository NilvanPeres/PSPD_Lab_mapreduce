# PSPD_Lab_mapreduce


## Ingegrantes do grupo
| Nome | Matricula  |
|------------|-----------
|Leonardo da Silva Gomes |180021974
|Nilvan Peres | 170122468
|Paulo Gonçalves Lima |170122549
|Pedro Vitor de Salles Cella |170113060
|Sofia Costa Patrocinio |170114333


## Explicação


### Versão Normal - Letra A

Na versão normal foi utilizado a lógica de pensamento que um usuário viu mais de um filme e realizou uma avaliação para cada filme, com isso em mente, lemos os dados de um arquivo txt, contendo os números na seguinte ordem:

| user_id | movie_id  | movie_rate | 
|------------|----------- |-----------

Dessa forma foi utilizado a leitrua do arquivo txt, logo mais uma iteração por linha que pega os dados supracitados anteriormente, logo o resultado dessa iteração é uma lista contendo um dicionário, onde a chave representa o user_id e a chave é uma lista com movie_id e o rate dado pelo usuário

### MapReduce - Letra B

Na versão do MapReduce, utilizamos o pensamento da versão normal, porém são usadosa partir do retorno, onde temos as etapas de Map, Sort e Reduce:

- Map:
  Juntamos todas as linhas retiradas de um arquivo txt, ordenamos pelo id do usuario e retornamos o k, v[] em exemplo de (244, [51, 2])

- Sort:
  O sort agrupa ordena os usuários e os agrupa a partir do user_id

- Reduce:
  Para finalizar o reduce agrupo para um mesmo usuário, sendo este tratado como chave, com movie_id e rate sendo valores dentro de uma lista. 

