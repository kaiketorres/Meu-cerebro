Em [[SQL]], `VARCHAR` (abreviação de "variable character") é um tipo de dado utilizado para armazenar cadeias de caracteres de comprimento variável. Diferente do tipo `CHAR`, que tem um comprimento fixo, o `VARCHAR` permite armazenar strings de tamanhos diferentes até um limite especificado.

Aqui está um exemplo de como usar `VARCHAR` em uma declaração SQL:
```
CREATE TABLE usuarios (
    id INT PRIMARY KEY,
    nome VARCHAR(50)
);
```

Nesse exemplo, a coluna `nome` pode armazenar até 50 caracteres. Se você armazenar um valor com menos de 50 caracteres, o espaço não utilizado não será desperdiçado, ao contrário do `CHAR`, que sempre usa o espaço total alocado, preenchendo com espaços em branco se necessário.