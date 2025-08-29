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
