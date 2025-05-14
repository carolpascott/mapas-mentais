---
markmap:
  initialExpandLevel: 2
---

# 🧠 SQL

## 🔷 DDL – Data Definition Language
- Define estruturas do banco

### CREATE
- 📎 Cria tabelas, bancos, views

 ```SQL
CREATE TABLE clientes (
  id INT PRIMARY KEY,
  nome VARCHAR(100)); 
```


| Constraint          | Exemplo de uso                                                                 |
|---------------------|---------------------------------------------------------------------------------|
| `PRIMARY KEY`       | `id INT PRIMARY KEY`                                                            |
| `FOREIGN KEY`       | `FOREIGN KEY (cliente_id) REFERENCES clientes(id)`                             |
| `UNIQUE`            | `email VARCHAR(100) UNIQUE`                                                    |
| `NOT NULL`          | `nome VARCHAR(100) NOT NULL`                                                   |
| `CHECK`             | `CHECK (idade >= 18)`                                                           |
| `DEFAULT`           | `data_cadastro DATE DEFAULT CURRENT_DATE`                                      |


### ALTER
- 📎 Modifica estrutura

```SQL
ALTER TABLE clientes
ADD email VARCHAR(100);
```

|   Comandos                  | Exemplo                                        |
|-----------------------------|------------------------------------------------|
| `ADD`                       | `ALTER TABLE t ADD coluna VARCHAR(50);`        |
| `DROP COLUMN`               | `ALTER TABLE t DROP COLUMN coluna;`            |
| `MODIFY` / `CHANGE`         | `ALTER TABLE t MODIFY nome VARCHAR(100);`      |
| `RENAME COLUMN`             | `ALTER TABLE t RENAME COLUMN nome TO nome2;`   |
| `RENAME TO`                 | `ALTER TABLE t RENAME TO nova_tabela;`         |
| `ADD CONSTRAINT`            | `ALTER TABLE t ADD CONSTRAINT pk PRIMARY KEY(id);` |
| `DROP CONSTRAINT`           | `ALTER TABLE t DROP CONSTRAINT fk_cliente;`    |

### DROP
- 📎 Remove estrutura

``` SQL
DROP TABLE clientes;
```

### TRUNCATE
-📎 Apaga todos os dados, sem WHERE

``` SQL
TRUNCATE TABLE clientes;
```
---

## 🟢 DML – Data Manipulation Language
- Manipula os dados da tabela

### INSERT
- 📎 Adiciona dados

``` SQL
INSERT INTO clientes (id, nome)
VALUES (1, 'Carol');
``` 

### UPDATE
- 📎 Atualiza dados existentes

``` SQL
UPDATE clientes
SET nome = 'Carolina'
WHERE id = 1;
``` 
### DELETE
- 📎 Remove registros

``` SQL
DELETE FROM clientes
WHERE id = 1;
``` 
### SELECT
- 📎 Consulta dados

``` SQL
SELECT nome
FROM clientes
WHERE id = 1;
``` 
---

## 🔐 DCL – Data Control Language

### GRANT
- 📎 Concede permissão

``` SQL
GRANT SELECT ON clientes
TO usuario1;
```

### REVOKE
- 📎 Remove permissão

``` SQL
REVOKE SELECT ON clientes
FROM usuario1;
```

---

## 🔄 TCL – Transaction Control Language

### COMMIT
- 📎 Salva alterações

### ROLLBACK
- 📎 Desfaz alterações

### SAVEPOINT
- 📎 Marca ponto de retorno

---

## 🔗 JOINs – Junção de Tabelas

### INNER JOIN
``` SQL
-- 📎 Retorna apenas registros com correspondência

SELECT f.nome, d.nome
FROM funcionarios f
INNER JOIN departamentos d ON f.dep_id = d.id;
```

### LEFT JOIN
``` SQL
-- 📎 Todos da tabela da esquerda, mesmo sem correspondência

SELECT f.nome, d.nome
FROM funcionarios f
LEFT JOIN departamentos d ON f.dep_id = d.id;
```

### RIGHT JOIN
- 📎 Todos da direita, mesmo sem correspondência

### FULL OUTER JOIN
- 📎 Todos os dados de ambas as tabelas

---

## 📊 Funções Agregadas

### COUNT()
``` SQL
-- 📎 Conta registros

SELECT COUNT(*)
FROM funcionarios;
```

### AVG()
``` SQL
-- 📎 Média

SELECT AVG(salario)
FROM funcionarios;
```

### SUM()
- 📎 Soma total

### MIN() / MAX()
- 📎 Menor / maior valor

---

## ⚠️ 🔥 Bizus de Prova

### WHERE não pode ser usado com funções agregadas

| - | Para filtrar funções, use HAVING|
|-|-|

```SQL
SELECT departamento, COUNT(*) 
FROM funcionarios 
GROUP BY departamento 
HAVING COUNT(*) > 10;
```

### GROUP BY sempre antes do HAVING

### TRUNCATE é mais rápido que DELETE, mas não permite WHERE

### DELETE pode ser desfeito com ROLLBACK, TRUNCATE não

### FULL OUTER JOIN pode ser simulado com UNION de LEFT + RIGHT

### NULL não é igual a nada (nem a outro NULL)

### COUNT(*) conta tudo, COUNT(campo) ignora NULL

---

## 🧠 Palavras-chave

- DDL = estrutura | DML = dados | DCL = controle | TCL = transações  
- JOIN = junção de tabelas  
- GROUP BY + HAVING → para filtrar agregações  
- NULL ≠ 0 ≠ ''
