USE cinnectaquery;
-- show tables;

CREATE TABLE EMPREGADOS (
  ID int PRIMARY KEY,
  nome varchar(20) NOT NULL,
  idade int NOT NULL,
  endereco varchar(40) NOT NULL,
  salario float NOT NULL
);
-- describe table empregados;

INSERT INTO EMPREGADOS VALUES (0001, 'Clark', 23, 'endereço 1', 1000);
INSERT INTO EMPREGADOS VALUES (0002, 'Dave', 18, 'endereço 2', 1200);
INSERT INTO EMPREGADOS VALUES (0003, 'Ava', 33, 'endereço 3', 5000);

INSERT INTO EMPREGADOS VALUES (0004, 'Eva', 13, 'endereço 4', 1300);
INSERT INTO EMPREGADOS VALUES (0005, 'John', 43, 'endereço 5', 5500);
INSERT INTO EMPREGADOS VALUES (0006, 'Hiro', 53, 'endereço 6', 4800);

SELECT * FROM EMPREGADOS WHERE idade = '23';
SELECT A.salario, B.salario FROM EMPREGADOS A CROSS JOIN EMPREGADOS B WHERE A.id != B.id AND A.salario < B.salario ORDER BY A.salario;
