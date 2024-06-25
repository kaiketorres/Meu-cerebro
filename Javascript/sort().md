O método `sort()` em [[Javascript]] , como arrays em JavaScript, é usado para ordenar os elementos. Por padrão, ele ordena em ordem alfabética ou por valores Unicode. Para ordenação numérica ou personalizada, é necessário fornecer uma função de comparação como argumento. É importante lembrar que `sort()` altera o array original e não retorna uma cópia ordenada.

exemplo simples de como usar o método `sort()` em um array em JavaScript para ordenar números numericamente:

```
let numeros = [3, 1, 5, 2, 4];

// Ordenação numérica crescente
numeros.sort((a, b) => a - b);

console.log(numeros); // Saída: [1, 2, 3, 4, 5]
```

Neste exemplo:

- `numeros` é um array de números desordenados.
- `numeros.sort((a, b) => a - b);` ordena os números de forma crescente utilizando uma função de comparação que subtrai `a` de `b`.
- `console.log(numeros);` imprime o array `numeros` ordenado.

Este é um exemplo básico de como usar `sort()` para ordenação numérica em JavaScript.

