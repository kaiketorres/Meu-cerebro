
# Comando CHAR no SQL

## O que é [[Char]]?
`CHAR` é um tipo de dado em SQL usado para armazenar **cadeias de caracteres de tamanho fixo**. Isso significa que, independentemente do número de caracteres inseridos, o espaço reservado será sempre o mesmo.

### Características principais:
- **Tamanho fixo**: Quando definido, sempre ocupará o mesmo espaço na tabela.
  Ex.: `CHAR(10)` armazenará até 10 caracteres. Se o valor inserido for menor, ele será preenchido com espaços em branco até atingir o tamanho.
- Usado quando você sabe que o comprimento dos dados será sempre o mesmo (ex.: códigos de produtos, abreviações de estado).

### Exemplos:
1. **Criando uma tabela com CHAR**  
```sql
CREATE TABLE Produtos (
    codigo CHAR(5),
    nome VARCHAR(50)
);
```
Neste exemplo, a coluna `codigo` terá sempre 5 caracteres.

2. **Inserindo dados**  
```sql
INSERT INTO Produtos (codigo, nome)
VALUES ('123', 'Chocolate');
```
O valor `123` será armazenado como `123  ` (com dois espaços adicionais).

3. **Diferença entre CHAR e VARCHAR**  
- `CHAR`: Tamanho fixo (mais rápido para acessar dados com tamanho constante).  
- `VARCHAR`: Tamanho variável (mais eficiente em armazenamento para dados de comprimento variável).

### Quando usar?
- Use `CHAR` para dados que sempre terão o mesmo comprimento, como:
  - Códigos de barras
  - Siglas de estados
  - CEPs

---
**Nota:** Para evitar problemas, lembre-se de usar o comando `TRIM()` ao consultar valores para remover os espaços em branco extras.
