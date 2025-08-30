# 📝 Resolução dos Exercícios Lista 2

## Exercício 1

Enunciado: <b> Encontrar o nome de todos os alunos matriculados em 2024. </b>

```
A = σAno=2024(Matriculas)
B = πNomeAluno(A⨝Aluno)
B
```

---

## Exercício 2

Enunciado: <b> Encontrar o nome dos cursos que possuem alunos matriculados em 2024. </b>

```
A = σAno=2024(Matriculas)
B = πNomeCurso(A⨝Curso)
B
```

---

## Exercício 3

Enunciado: <b> Encontrar o nome dos cursos que possuem alunos matriculados em 2024 e que
são oferecidos pelo departamento de Exatas. </b>

```
A = σAno=2024(Matriculas)
B = σNomeDepto='Exatas'(Depto)
C = B⨝Curso
D = πNomeCurso(A⨝C)
D
```

---

## Exercício 4

Enunciado: <b> Encontrar o nome de todos os alunos matriculados no curso de 'Matemática'
em 2024. </b>

```
A = σNomeCurso='Matematica'(Curso)
B = A⨝Matriculas
C = σAno=2024(B)
D = πIdAluno(C)
E = D⨝Aluno
F = πNomeAluno(E)
F
```

---

## Exercício 5

Enunciado: <b> Encontrar o nome dos cursos que não possuem nenhum aluno matriculado em 2024. </b>

```
A = σAno=2024(Matriculas)
B = πIdAluno(A)
C = πIdCurso(Curso)
D = C-B
E = D⨝Curso
F = πNomeCurso(E)
F
```

---

## Exercício 6

Enunciado: <b> Encontrar o nome dos alunos que se matricularam tanto em ‘Matemática’
quanto em ‘História’ em 2023. </b>

```
A = σAno=2024(Matriculas)
B = σNomeCurso='Historia'(Curso)
C = σNomeCurso='Matematica'(Curso)
D = πIdAluno(A⨝B)
E = πIdAluno(A⨝C)
F = D∩E
G = πNomeAluno(F⨝Aluno)
G
```

---

## Exercício 7

Enunciado: <b> Listar o nome dos alunos, o nome de seus cursos matriculados em 2023 e o
nome dos departamentos de seus cursos, mesmo aqueles que não se matricularam em nenhum curso em 2023. </b>

```
A = σAno=2023(Matriculas)
B = πIdAluno,NomeCurso,NomeDepto(A⨝Curso⨝Depto)
C = (Matriculas - A)⨝ πIdCurso,IdDepto(Curso)⨝ Depto
D = πIdAluno,NomeDepto(C)⨝Aluno
E = πIdAluno,NomeDepto,NomeAluno(D)
F = πIdAluno,NomeDepto,NomeAluno(B⨝Aluno)
G = E∪F
H = πNomeAluno,NomeCurso,NomeDepto,IdAluno(B⨝Aluno)
I = G⟕H
I
```

---

## Exercício 8

Enunciado: <b> Mostrar o nome dos professores e o nome dos departamentos aos quais eles
pertencem, incluindo aqueles professores que não pertencem a nenhum
departamento. </b>

```
A = Professor ⟕ Depto
B = πNomeProf,NomeDepto(A)
B
```

---

## Exercício 9

Enunciado: <b> Listar o nome de todos os cursos e o nome de seus respectivos alunos
matriculados em 2024, incluindo aqueles cursos que não têm alunos matriculados em 2024. </b>

```
A = σAno=2024(Matriculas)
B = A ⟕ Aluno
C = πIdCurso,NomeAluno(B)
D = Curso ⟕ C
E = πNomeCurso,NomeAluno(D)
E
```

---

## Exercício 10

Enunciado: <b> Encontrar cursos sem alunos matriculados em 2024. </b>

```
A = σAno=2024(Matriculas)
B = πIdCurso(A) /* cursos com matriculas em 2024 */
C = πIdCurso(Curso) /* todos os cursos */
D = C - B
E = πNomeCurso(D⨝Curso)
E
```

---

## Exercício 11

Enunciado: <b> Verificar se os cursos de 'Matemática' e 'Química' são oferecidos pelo mesmo
departamento. </b>

```
A = πIdDepto(σNomeCurso='Matematica'(Curso))
B = πIdDepto(σNomeCurso='Quimica'(Curso))
C = A∩B
C
```
