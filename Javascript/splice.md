### Anotação sobre o Método `splice()` em JavaScript

O método `splice()` é usado para adicionar, remover ou substituir elementos de um array em [[Javascript]]. É uma função poderosa que modifica o array original e retorna um novo array contendo os elementos removidos (se houver).

#### Sintaxe:

```
array.splice(início, quantidadeRemover, item1, item2, ...);
```

- **`início`**: Índice a partir do qual a modificação deve começar.
- **`quantidadeRemover`**: Número de elementos a serem removidos a partir do índice de início. Se for `0`, nenhum elemento será removido.
- **`item1, item2, ...`**: (Opcional) Elementos a serem adicionados no array, começando a partir do índice de início.

#### Funcionalidades Principais:

1. **Remover Elementos**:
    
    - Remove um ou mais elementos de um array a partir de uma posição especificada.

```
const frutas = ["maçã", "banana", "laranja", "uva"];
frutas.splice(1, 2); // Remove "banana" e "laranja"
console.log(frutas); // Saída: ["maçã", "uva"]
```

const frutas = ["maçã", "banana", "laranja", "uva"];
frutas.splice(1, 2); // Remove "banana" e "laranja"
console.log(frutas); // Saída: ["maçã", "uva"]

```
const frutas = ["maçã", "uva"];
frutas.splice(1, 0, "banana", "laranja"); // Adiciona "banana" e "laranja" na posição 1
console.log(frutas); // Saída: ["maçã", "banana", "laranja", "uva"]
```


**Substituir Elementos**:

- Substitui elementos existentes por novos.

```
const frutas = ["maçã", "banana", "laranja", "uva"];
frutas.splice(1, 1, "kiwi"); // Substitui "banana" por "kiwi"
console.log(frutas); // Saída: ["maçã", "kiwi", "laranja", "uva"]

```

#### Observações:

- O método `splice()` modifica o array original, então use com cuidado se precisar manter o array inicial intacto.
- Ele é uma ferramenta versátil, ideal para manipulações complexas de arrays, como inserções, remoções e substituições simultâneas.

### Resumo:

`splice()` é um método que permite manipular arrays em JavaScript de forma flexível, adicionando, removendo ou substituindo elementos diretamente no array original.