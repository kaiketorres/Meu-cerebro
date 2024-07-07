Em SQL, `ENUM` é um tipo de dado especial disponível em alguns sistemas de gerenciamento de banco de dados (DBMS), como MySQL, que permite definir um conjunto de valores pré-determinados para uma coluna. Esse tipo de dado é útil quando você deseja que uma coluna possa armazenar apenas um conjunto restrito de valores específicos.

Aqui está um exemplo de como usar `ENUM` em uma declaração SQL:

```
CREATE TABLE usuarios (
    id INT PRIMARY KEY,
    nome VARCHAR(50) NOT NULL,
    status ENUM('ativo', 'inativo', 'pendente') NOT NULL
);
```

Neste exemplo, a coluna `status` pode armazenar apenas um dos três valores: `'ativo'`, `'inativo'` ou `'pendente'`. Tentar inserir um valor diferente resultará em um erro.

O tipo `ENUM` é útil para garantir a integridade dos dados, limitando os valores possíveis que uma coluna pode ter e facilitando a manutenção e a leitura dos dados no banco de dados.