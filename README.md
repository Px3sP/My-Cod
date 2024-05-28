<!-- CRIANDO UM BANCO DE DADOS PARA UMA PIZZARIA E ESFIRRARIA, BASICO.'''-->

CREATE DATABASE empresa; 
USE empresa; 

CREATE TABLE funcionarios(
nome VARCHAR(50) NOT NULL, 
matricula INTEGER(6) PRIMARY KEY NOT NULL, 
cargo VARCHAR (15)NOT NULL, 
CHECK (cargo IN ("Normal", "Lider","Gestor", "Supervisor", "Diretor", "Presidente"))

);
INSERT INTO funcionarios (nome, matricula, cargo) VALUES ("Victor Gabriel", 123456, "Normal");    
INSERT INTO funcionario(nome, matricula, cargo) VALUES("Cryscia Rodrigues", 321654, "GESTOR"); 

CREATE TABLE clientes(
nome_Cliente VARCHAR(50) NOT NULL, 
telefone VARCHAR(15) NOT NULL,
cod_Cadastro INTEGER(6) NOT NULL PRIMARY KEY, 
dt_Nascimento DATE
); 

INSERT INTO clientes(nome_Cliente, telefone, cod_Cadastro, dt_Nascimento) VALUES("Maria Jose Batista Peixe", "11-945381490", 663576,"1964-05-05");
SELECT *FROM clientes; 

CREATE TABLE pedidos(
num_Pedido INTEGER(123) NOT NULL primary key, 
dt_Compra DATE
);  

INSERT INTO pedidos(num_Pedido, dt_Compra) VALUES (669, "2024-05-28");
SELECT *FROM pedidos; 
