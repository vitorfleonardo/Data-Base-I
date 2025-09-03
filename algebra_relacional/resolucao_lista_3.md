# 📝 Resolução dos Exercícios Lista 3

## Exercício 1

Enunciado: <b> Liste os nomes dos clientes com idade >= 20 anos. </b>

```
A = σ idade >= 20 (Cliente)
B = π nomeCliente (A)
B
```

---

## Exercício 2

Enunciado: <b> Liste o código dos carros do tipo ‘SUV’ que são da cor ‘Prata </b>

```
A = σ tipo = 'SUV' (Carro)
B = σ cor = 'Prata' (A)
C = π codCarro (B)
C
```

---

## Exercício 3

Enunciado: <b> Liste os tipos de carros de Brasília </b>

```
A = σ nomeCidade = 'Brasilia' (Cidade)
B = A ⨝ Carro
C = π tipo (B)
C

```

---

## Exercício 4

Enunciado: <b> Liste o nome dos clientes de Brasília que tem mais de 30 anos (>= 30) </b>

```
A = σ nomeCidade = 'Brasilia' (Cidade)
B = A ⨝ Cliente
C = σ idade >= 30 (B)
D = π nomeCliente (C)
D
```

---

## Exercício 5

Enunciado: <b> Liste o código dos carros do tipo "SUV" da cidade de Brasília e da cidade de
São Paulo </b>

```
A = σ nomeCidade = 'Brasilia' (Cidade)
B = σ nomeCidade = 'Sao Paulo' (Cidade)
C = A ∪ B
D = σ tipo = 'SUV' (Carro)
E = C ⨝ D
F = π codCarro (E)
F
```

---

## Exercício 6

Enunciado: <b> Mostre a data da reserva e o nome dos clientes que reservaram carros do
tipo 'SUV' </b>

```
A = σ tipo = 'SUV' (Carro)
B = A ⨝ Reserva
C = π data, codCliente (B)
D = C ⨝ Cliente
E = π data, nomeCliente (D)
E
```

---

## Exercício 7

Enunciado: <b> Mostre o nome e idade dos clientes, e data de suas reservas. Clientes sem
reserva também devem aparecer no resultado </b>

```
A = Cliente ⟕ Reserva
B = π nomeCliente, idade, data (A)
B
```

---

## Exercício 8

Enunciado: <b> Liste o nome dos clientes de Brasília que nunca fizeram reserva </b>

```
A = σ nomeCidade = 'Brasilia' (Cidade)
B = A ⨝ Cliente /* clientes de brasilia */
C = π codCliente (B)
D = π codCliente (Reserva)
E = C - D
F = E ⨝ Cliente
G = π nomeCliente (F)
G
```

---

## Exercício 9

Enunciado: <b> Listar o nome de todos os funcionários e o código dos carros da cidade de
Brasília que eles já registaram reservas, se houver. </b>

```
A = σ nomeCidade = 'Brasilia' (Cidade)
B = A ⨝ Carro ⨝ Reserva
C = π codCarro, codFunc (B)
D = Funcionario ⟕ C
E = π nomeFunc,codCarro(D)
E
```

---

## Exercício 10

Enunciado: <b> Procure pelo nome dos clientes que nunca efetuaram reserva de carro
da cor ‘prata’ </b>

```
A = σ cor = 'Prata' (Carro)
B = A ⨝ Reserva /* Reservas de carro prata */
C = π codCarro (B)
D = π codCarro (Reserva)
E = D - C /* Reservas de carro nao prata */
F = E ⨝ Reserva
G = F ⨝ Cliente
H = π nomeCliente (G)
H
```

---
