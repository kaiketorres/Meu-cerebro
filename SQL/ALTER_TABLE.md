
# ALTER TABLE

O comando **ALTER TABLE** é utilizado em[[ SQL]] para modificar a estrutura de uma tabela existente. Ele permite realizar diversas alterações sem a necessidade de recriar a tabela.

## **Principais Usos**

### 1. Adicionar Coluna
Você pode adicionar uma nova coluna à tabela:
```sql
ALTER TABLE nome_tabela
ADD nova_coluna tipo_dado;
```
Exemplo:
```sql
ALTER TABLE produtos
ADD categoria VARCHAR(50);
```

### 2. Remover Coluna
Para remover uma coluna existente:
```sql
ALTER TABLE nome_tabela
DROP COLUMN nome_coluna;
```
Exemplo:
```sql
ALTER TABLE produtos
DROP COLUMN categoria;
```

### 3. Modificar Coluna
Para alterar o tipo de dado ou outras propriedades de uma coluna:
```sql
ALTER TABLE nome_tabela
MODIFY nome_coluna novo_tipo_dado;
```
Exemplo:
```sql
ALTER TABLE produtos
MODIFY preco DECIMAL(10,2);
```

### 4. Renomear Coluna
Para renomear uma coluna (suportado em alguns bancos de dados):
```sql
ALTER TABLE nome_tabela
RENAME COLUMN nome_antigo TO nome_novo;
```
Exemplo:
```sql
ALTER TABLE produtos
RENAME COLUMN preco TO valor;
```

### 5. Renomear Tabela
Para renomear a tabela inteira:
```sql
ALTER TABLE nome_tabela
RENAME TO novo_nome_tabela;
```
Exemplo:
```sql
ALTER TABLE produtos
RENAME TO itens;
```

## **Considerações**
- Use com cuidado, especialmente ao remover colunas, pois isso pode resultar em perda de dados.
- Certifique-se de fazer backup antes de realizar alterações críticas.

## **Anotações Adicionais**
- Algumas variações podem depender do banco de dados que você está utilizando (MySQL, PostgreSQL, SQL Server, etc.).
- Nem todos os comandos são suportados em todos os SGBDs.

---
> _Essa anotação foi feita como parte do estudo sobre comandos SQL._
