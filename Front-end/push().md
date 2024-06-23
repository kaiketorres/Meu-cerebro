Em JavaScript, o método `.push()` é fundamental para adicionar um ou mais elementos ao final de um [[Variáveis Compostas]] ou arrays. Ele modifica o array original e retorna o novo comprimento do array após a adição dos elementos. Aqui está um exemplo simples de como usar o `.push()`:

```
let frutas = ['maçã', 'banana'];
console.log(frutas); // Output: ['maçã', 'banana']

// Adicionando um elemento usando .push()

frutas.push('laranja');
console.log(frutas); // Output: ['maçã', 'banana', 'laranja']

// Adicionando múltiplos elementos usando .push()

frutas.push('melancia', 'morango');
console.log(frutas); // Output: ['maçã', 'banana', 'laranja', 'melancia', 'morango']
```

Note que o método `.push()` altera o array original, adicionando os elementos fornecidos ao final dele. Isso é útil quando você precisa expandir dinamicamente um array durante a execução de um programa em JavaScript.

