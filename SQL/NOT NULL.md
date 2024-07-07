Em [[SQL]], a cláusula `NOT NULL` é usada para especificar que uma coluna não pode conter valores `NULL`. Isso significa que, ao inserir ou atualizar registros em uma tabela, é obrigatório fornecer um valor para as colunas que têm a restrição `NOT NULL`. Se tentar inserir um valor `NULL` em uma dessas colunas, o banco de dados retornará um erro.

Aqui está um exemplo de uso de `NOT NULL` em uma declaração SQL:
```
CREATE TABLE usuarios (
    id INT PRIMARY KEY,
    nome VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

Neste exemplo, as colunas `nome` e `email` são definidas como `NOT NULL`, o que significa que não podem ter valores `NULL`. Portanto, ao adicionar um novo registro à tabela `usuarios`, você deve fornecer valores para essas colunas.