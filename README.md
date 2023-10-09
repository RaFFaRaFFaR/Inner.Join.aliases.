# INNER JOIN E ALIASES
## Descrição
Crie duas tabelas conforme o modelo apresentado nos slides 61 e 62, no material da AULA 7;

Preste atenção aos campos que estão no exemplo;

Insira os valores conforme os slides;

Aplique o exemplo sobre inner join dado no slide 67, do material indicado acima;

Execute essas atividades dentro o Oracle Workbench;

Crie um repositório remoto e envie o script em SQL;

Produza o Readme do repositório remoto e tire um print da tela após o término da atividade;

Coloque comentários em seu código.

## Codigo

    \\-- Criação da tabela Cidades
    CREATE TABLE Cidades (
    id INT PRIMARY KEY AUTO_INCREMENT, -- Identificador único da cidade
    nome VARCHAR(60) NOT NULL, -- Nome da cidade (não pode ser nulo)
    populacao INT -- População da cidade
    );

    -- Criação da tabela Alunos
    CREATE TABLE Alunos (
    id INT PRIMARY KEY AUTO_INCREMENT, -- Identificador único do aluno
    nome VARCHAR(60) NOT NULL, -- Nome do aluno (não pode ser nulo)
    data_nasc DATE, -- Data de nascimento do aluno
    cidade_id INT, -- Chave estrangeira que referencia o id na tabela Cidades
    FOREIGN KEY (cidade_id) REFERENCES Cidades(id) -- Restrição de chave estrangeira
    );
    -- Inserção de dados na tabela Cidades
    INSERT INTO Cidades VALUES (1, 'Arraial dos Tucanos', 42632);
    INSERT INTO Cidades VALUES (2, 'Springfield', 13820);
    INSERT INTO Cidades VALUES (3, 'Hill Valley', 27383);
    INSERT INTO Cidades VALUES (4, 'Coruscant', 19138);
    INSERT INTO Cidades VALUES (5, 'Minas Tirith', 31394);



    -- Inserção de dados na tabela Alunos
    INSERT INTO Alunos VALUES (1, 'Immanuel Kant', '1724-04-22', 1);
    INSERT INTO Alunos VALUES (2, 'Alan Turing', '1912-06-23', 3);
    INSERT INTO Alunos VALUES (3, 'George Boole', '2002-01-01', 1);
    INSERT INTO Alunos VALUES (4, 'Lynn Margulis', '1991-08-12', 3);
    INSERT INTO Alunos VALUES (5, 'Nicola Tesla', '2090-01-08', NULL);
    INSERT INTO Alunos VALUES (6, 'Ada Lovelace', '1978-05-12', 2);
    INSERT INTO Alunos VALUES (7, 'Claude Shannon', '1982-10-15', 3);
    INSERT INTO Alunos VALUES (8, 'Charles Darwin', '2010-02-06', NULL);
    INSERT INTO Alunos VALUES (9, 'Marie Curie', '2007-07-12', 3);
    INSERT INTO Alunos VALUES (10, 'Carl Sagan', '2000-11-20', 1);
    INSERT INTO Alunos VALUES (11, 'Tim Berners-Lee', '1973-12-25', 2);

    -- Consulta usando INNER JOIN para combinar dados das tabelas Alunos e Cidades
    SELECT *
    FROM alunos inner
    join cidades
    on cidade_id = alunos.cidade_id;

![Consulta usando INNER JOIN](https://github.com/RaFFaRaFFaR/Inner.Join.aliases./assets/127689567/6575f99d-6d95-464f-a0de-fb951b5ce9b0)


## Consulta usando INNER JOIN:
ste trecho de código realiza uma consulta nas tabelas Alunos e Cidades usando uma cláusula INNER JOIN. Ele combina registros das tabelas onde o cidade_id na tabela Alunos é igual ao id na tabela Cidades. O resultado incluirá todas as colunas de ambas as tabelas para os registros correspondentes


## Última atualização 09/10/21
