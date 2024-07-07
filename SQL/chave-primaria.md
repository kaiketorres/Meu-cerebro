Em [[SQL]], uma chave primária (PRIMARY KEY) é um campo ou conjunto de campos em uma tabela que identifica de maneira exclusiva cada registro dessa tabela. A chave primária possui as seguintes características principais:

1. **Unicidade**: Cada valor na chave primária deve ser único, garantindo que cada registro possa ser identificado de forma exclusiva.
2. **Não-nulidade**: A chave primária não pode conter valores `NULL`. Todos os registros devem ter um valor na coluna ou colunas que compõem a chave primária.

Aqui está um exemplo de como definir uma chave primária em uma tabela SQL:

### Exemplo 1: Chave primária simples

```
CREATE TABLE usuarios (
    id INT PRIMARY KEY,
    nome VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL
);
```

Neste exemplo, a coluna `id` é definida como a chave primária da tabela `usuarios`. Cada valor de `id` deve ser único e não pode ser `NULL`.

### Exemplo 2: Chave primária composta

```
CREATE TABLE pedidos (
    pedido_id INT,
    produto_id INT,
    quantidade INT,
    PRIMARY KEY (pedido_id, produto_id)
);
```

Neste exemplo, a chave primária é composta por duas colunas: `pedido_id` e `produto_id`. A combinação dos valores dessas duas colunas deve ser única para cada registro na tabela `pedidos`, e nenhuma das colunas pode conter valores `NULL`.

### Benefícios de usar chaves primárias

- **Integridade dos Dados**: As chaves primárias garantem que cada registro na tabela possa ser identificado de maneira única, ajudando a manter a integridade dos dados.
- **Desempenho**: As chaves primárias criam índices automaticamente, o que pode melhorar o desempenho das consultas que utilizam essas colunas para busca.
- **Relacionamentos**: Em bancos de dados relacionais, as chaves primárias são frequentemente usadas para criar relacionamentos entre tabelas. Por exemplo, uma chave primária em uma tabela pode ser referenciada como chave estrangeira (FOREIGN KEY) em outra tabela.

### Alterando a chave primária

Se precisar alterar ou adicionar uma chave primária em uma tabela existente, você pode usar os comandos `ALTER TABLE`. Aqui está um exemplo:

#### Adicionar uma chave primária:

```
ALTER TABLE usuarios
ADD PRIMARY KEY (id);
```

Remover uma chave primária

```
ALTER TABLE usuarios
DROP PRIMARY KEY;
```

Usar chaves primárias de forma adequada é fundamental para projetar um banco de dados relacional eficiente e bem estruturado.