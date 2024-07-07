Em SQL, `DECIMAL` (ou `NUMERIC`) é um tipo de dado utilizado para armazenar números com ponto decimal de precisão exata. Este tipo é particularmente útil para armazenar valores monetários ou outros números onde a precisão decimal é crucial.

A sintaxe básica para definir uma coluna `DECIMAL` é:
```
DECIMAL(p, s)
```

Onde:

- `p` é a precisão (precision), ou seja, o número total de dígitos que o número pode ter.
- `s` é a escala (scale), ou seja, o número de dígitos à direita do ponto decimal.

Por exemplo:

```
CREATE TABLE produtos (
    id INT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    preco DECIMAL(10, 2) NOT NULL
);
```

Neste exemplo, a coluna `preco` pode armazenar números com até 10 dígitos no total, dos quais 2 são reservados para a parte decimal. Assim, valores como `12345678.90` ou `0.99` são válidos.

Usar `DECIMAL` é importante em contextos onde a precisão financeira é necessária, como em sistemas bancários ou de contabilidade, onde até pequenos erros de arredondamento podem ser significativos.
