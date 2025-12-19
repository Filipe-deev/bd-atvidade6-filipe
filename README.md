# bd-atvidade6-filipe

create database Grau;
USE Grau;

create table Cursos(
	id INT PRIMARY KEY,
    nome VARCHAR(100),
    carga_horaria INT,
    professores_cadastrados VARCHAR(100),
    alunos_cadastrados VARCHAR(100)
);

create table professores(
	id INT PRIMARY KEY,
    nome VARCHAR(100),
    telefone VARCHAR(24),
    data_de_entrada DATE
);

create table alunos(
	id_aluno INT auto_increment,
    telefone INT,
    nome VARCHAR (150),
    data_matricula DATE,
    turma VARCHAR(100),
    curso VARCHAR(100),
    notas INT
);

create table disciplinas(
	id INT PRIMARY KEY,
    nome VARCHAR (100),
    carga_horaria VARCHAR (100)
);

UPDATE INTO alunos (nome, telefone, data_matricula, turma, curso, nota) VALUES
('Ana Clara', '11987654321', '2024-02-10', 'A1', 'Informática', 8.5),
('João Pedro', '11991234567', '2024-02-12', 'A1', 'Informática', 7.8),
('Lucas Henrique', '11999887766', '2024-02-15', 'B2', 'Administração', 6.9),
('Maria Eduarda', '11988776655', '2024-02-18', 'B2', 'Administração', 9.2),
('Gabriel Santos', '11993456789', '2024-02-20', 'C3', 'Enfermagem', 8.0),
('Beatriz Oliveira', '11994561234', '2024-02-22', 'C3', 'Enfermagem', 7.5),
('Rafael Almeida', '11995678901', '2024-03-01', 'D4', 'Engenharia', 6.8),
('Juliana Costa', '11996789012', '2024-03-03', 'D4', 'Engenharia', 8.9),
('Matheus Ferreira', '11997890123', '2024-03-05', 'E5', 'Sistemas de Informação', 7.2),
('Larissa Gomes', '11998901234', '2024-03-07', 'E5', 'Sistemas de Informação', 9.0);

UPDATE alunos SET telefone='11987654321', data_matricula='2024-02-10', turma='A1', curso='Informática', nota=8.5
WHERE nome='Ana Clara';

UPDATE alunos SET telefone='11991234567', data_matricula='2024-02-12', turma='A1', curso='Informática', nota=7.8
WHERE nome='João Pedro';

UPDATE alunos SET telefone='11999887766', data_matricula='2024-02-15', turma='B2', curso='Administração', nota=6.9
WHERE nome='Lucas Henrique';

UPDATE alunos SET telefone='11988776655', data_matricula='2024-02-18', turma='B2', curso='Administração', nota=9.2
WHERE nome='Maria Eduarda';

DELETE FROM alunos
WHERE nome IN ('Lucas Henrique', 'Maria Eduarda', 'João Pedro');
 
