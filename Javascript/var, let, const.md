Em [[Javascript]], as palavras-chave `let`, `const` e `var` são usadas para declarar variáveis, mas existem diferenças importantes entre elas em termos de escopo, possibilidade de reatribuição e hoisting. Vamos explorar cada uma:

### `var`

- **Escopo**: Variáveis declaradas com `var` têm escopo de função. Ou seja, se forem declaradas dentro de uma função, só são acessíveis dentro dessa função. Se declaradas fora de uma função, têm escopo global.
- **Hoisting**: Variáveis `var` são "içadas" para o topo de seu escopo, o que significa que podem ser usadas antes de serem declaradas (mas com valor `undefined`).
- **Reatribuição**: Pode ser reatribuída e redeclarada dentro do mesmo escopo.

```
console.log(a); // undefined (devido ao hoisting)
var a = 10;
console.log(a); // 10

if (true) {
    var b = 20;
}
console.log(b); // 20 (escopo de função, mas não de bloco)
```

### `let`

- **Escopo**: Variáveis declaradas com `let` têm escopo de bloco, o que significa que só são acessíveis dentro do bloco `{}` onde foram declaradas.
- **Hoisting**: Também são içadas, mas não podem ser acessadas antes da declaração no código.
- **Reatribuição**: Pode ser reatribuída, mas não redeclarada no mesmo escopo.

```
// console.log(c); // ReferenceError: Cannot access 'c' before initialization
let c = 10;
console.log(c); // 10

if (true) {
    let d = 20;
    console.log(d); // 20 (escopo de bloco)
}
// console.log(d); // ReferenceError: d is not defined
```

### `const`

- **Escopo**: Também tem escopo de bloco.
- **Hoisting**: Comportamento similar ao `let`, içada mas não acessível antes da declaração.
- **Reatribuição**: Não pode ser reatribuída. O valor atribuído é constante, mas isso não significa que o valor é imutável se for um objeto ou array (as propriedades podem ser alteradas).

```
// console.log(e); // ReferenceError: Cannot access 'e' before initialization
const e = 10;
console.log(e); // 10

// e = 20; // TypeError: Assignment to constant variable.

if (true) {
    const f = 20;
    console.log(f); // 20 (escopo de bloco)
}
// console.log(f); // ReferenceError: f is not defined

const obj = { key: 'value' };
obj.key = 'newValue'; // Isto é permitido
console.log(obj.key); // 'newValue'

// obj = {}; // TypeError: Assignment to constant variable.
```

### Resumo das Diferenças

- **Escopo**: `var` tem escopo de função, `let` e `const` têm escopo de bloco.
- **Hoisting**: Todas são içadas, mas `let` e `const` não podem ser acessadas antes da declaração.
- **Reatribuição**: `var` e `let` podem ser reatribuídas, `const` não pode ser reatribuída.

Essas diferenças são cruciais para entender o comportamento das variáveis em JavaScript e escolher a palavra-chave apropriada para suas necessidades.

