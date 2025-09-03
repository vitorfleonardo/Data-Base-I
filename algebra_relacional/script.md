https://dbis-uibk.github.io/relax/calc/local/uibk/local/0

Exercícios parte #1
group: Projeto, Aloca, Pessoa

Projeto = {
Projeto_Codigo:number, Descricao:string
1122, BI
3344, GTI
5566, SIG
}

Aloca = {
Projeto_Codigo:number, CPF:number
1122, 123
3344, 123
5566, 123
3344, 147
1122, 456
5566, 456
}

Pessoa = {
CPF:number, Nome:string, Sexo:string, Idade:number, Gerente_CPF:number
123, Rubi, F, 35, null
147, Maria, F, 42, 123
258, Edu, M, 45, 147
456, Igor, M, 40, 123
789, Luiz, M, 38, 456
}

---

Exercícios parte #2
group: Depto, Curso, Aluno, Professor, Matriculas

Depto = {
IdDepto:number, NomeDepto:string
1, Exatas
2, Biociencias
3, Humanas
}

Curso = {
IdCurso:number, NomeCurso:string, IdDepto:number
101, Matematica, 1
102, Biologia, 2
103, Historia, 3
104, Quimica, 2
}

Aluno = {
IdAluno:number, NomeAluno:string, IdDepto:number
1, JoaoSilva, 1
2, MariaOliveira, 1
3, PedroCosta, 2
4, AnaSouza, 1
5, LucasSantos, 3
6, JoseSilveira, 2
}

Professor = {
IdProf:number, NomeProf:string, IdDepto:number
1, CarlosMagno, 1
2, JulianaMenezes, 2
3, RenatoSoares, 1
4, SimoneRocha, 3
5, MarcosGomes, null
}

Matriculas = {
IdAluno:number, IdCurso:number, Ano:number
1, 101, 2023
2, 102, 2023
3, 103, 2023
4, 101, 2024
5, 103, 2024
1, 103, 2023
3, 102, 2024
5, 101, 2024
}

# para lsita 3

Cidade = {
codCidade:number, nomeCidade:string
1, Brasilia
2, SaoPaulo
3, RiodeJaneiro
4, BeloHorizonte
5, Salvador
}

Funcionario = {
codFunc:number, nomeFunc:string, dataAdmissao:string, codCidade:number
101, JoaoSilva, 2020-01-15, 1
102, MariaSantos, 2019-05-20, 2
103, PedroCosta, 2021-03-10, 1
104, AnaOliveira, 2018-11-25, 3
105, CarlosLima, 2022-02-18, 2
}

Carro = {
codCarro:number, tipo:string, cor:string, codCidade:number
201, SUV, Prata, 1
202, Sedan, Preto, 2
203, SUV, Branco, 1
204, Hatch, Prata, 3
205, SUV, Azul, 2
206, SUV, Prata, 2
207, Sedan, Vermelho, 1
208, SUV, Preto, 1
209, Hatch, Branco, 4
210, SUV, Prata, 1
}

Cliente = {
codCliente:number, nomeCliente:string, idade:number, codCidade:number
301, RobertoMendes, 25, 1
302, FernandaAlves, 19, 2
303, LuisCarlos, 35, 1
304, CarlaRocha, 28, 3
305, BrunoTeixeira, 45, 2
306, JulianaFerreira, 22, 1
307, MarcosPereira, 31, 1
308, PatriciaSilva, 18, 4
309, AndreSouza, 40, 2
310, BeatrizLima, 33, 1
}

Reserva = {
codCarro:number, codCliente:number, codFunc:number, data:string
201, 301, 101, 2025-08-15
203, 303, 103, 2025-08-20
205, 305, 102, 2025-08-22
206, 304, 102, 2025-08-25
208, 307, 101, 2025-08-28
210, 309, 105, 2025-08-30
202, 306, 103, 2025-09-01
}
