# 📝 Resolução dos Exercícios Lista 1

## Exercício 1

Enunciado: <b> Liste o código dos Projetos e os dados das Pessoas que estão alocadas a esses Projetos.
Para o Projeto aparecer na listagem é necessário ter pelo menos uma Pessoa alocada </b>

```
A = Aloca⨝Pessoa
A
```

---

## Exercício 2

Enunciado: <b> Liste os dados dos projetos que alocam a Pessoa com CPF = 123 </b>

```
A = σCPF=123(Aloca)
B = A⨝Projeto
B
```

---

## Exercício 3

Enunciado: <b> Liste o CPF das pessoas que não participam de nenhum projeto </b>

```
A = πCPF(Pessoa)  /* CPF de todas as pessoas */
B = πCPF(Aloca) /* CPF dos alocados em projetos */
C = A - B
C
```

## Exercício 4

Enunciado: <b> Liste os dados das Pessoas que estão alocadas ao Projeto 3344 ou Projeto 5566 </b>

```
A = σProjeto_Codigo=3344∨Projeto_Codigo=5566(Aloca)
B = A⨝Pessoa
B
```

## Exercício 5

Enunciado: <b> Liste os dados das Pessoas que estão alocadas ao Projeto 3344 e ao Projeto 5566 </b>

```
A = πCPF((σProjeto_Codigo=3344(Aloca)))
B = πCPF((σProjeto_Codigo=5566(Aloca)))
C = A ∩ B
D = C ⨝ Pessoa
D
```

## Exercício 6

Enunciado: <b> Liste os dados das Pessoas que estão alocadas ao Projeto 3344, mas não estão alocadas
ao Projeto 5566 </b>

```
A = πCPF((σProjeto_Codigo=3344(Aloca)))
B = πCPF((σProjeto_Codigo=5566(Aloca)))
C = A - B
D = C ⨝ Pessoa
D
```

## Exercício 7

Enunciado: <b> Liste os dados dos Projetos, de Aloca e das Pessoas que estão alocadas a esses Projetos </b>

```
A = Aloca⨝Projeto⨝Pessoa
A
```

## Exercício 8

Enunciado: <b> Liste a descrição dos Projetos e o nome das Pessoas que estão alocadas a esses Projetos </b>

```
A = Projeto⨝Aloca⨝Pessoa
B = πDescricao,Nome(A)
B
```

## Exercício 9

Enunciado: <b> Liste o nome de todas as Pessoas, independente delas estarem alocadas a projetos, e a descrição do projeto a qual está alocada, quando houver </b>

```
A = Pessoa⟕Aloca
B = A⟕Projeto
B
```

## Exercício 10

Enunciado: <b> Liste o código dos projetos que não tem participantes </b>

```
A = πProjeto_Codigo(Projeto) /* todos os codigos */
B = A⟕Aloca /* CPFs participantes e null*/
C = B - Aloca
D = πProjeto_Codigo(C)
D
```
