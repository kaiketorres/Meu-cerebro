Em [[Javascript]], `typeof` é um operador unário que retorna uma string indicando o tipo de dado de uma variável ou expressão. Ele pode ser usado de várias maneiras para determinar o tipo de um valor:

1. **Tipos Primitivos:**
    
    - `typeof undefined` retorna `"undefined"`
    - `typeof 123` retorna `"number"`
    - `typeof 'Hello'` retorna `"string"`
    - `typeof true` retorna `"boolean"`
2. **Objetos e Funções:**
    
    - `typeof {}` retorna `"object"`
    - `typeof []` retorna `"object"` (array é tecnicamente um tipo de objeto em JavaScript)
    - `typeof function() {}` retorna `"function"`
3. **Valores Especiais:**
    
    - `typeof null` retorna `"object"` (isso é considerado um erro histórico em JavaScript)
    - `typeof NaN` retorna `"number"`
    - `typeof Infinity` retorna `"number"`

O operador `typeof` é útil para verificar o tipo de dados antes de realizar operações específicas ou para depurar o código. No entanto, é importante lembrar que `typeof null` retornar `"object"` é um comportamento antigo e peculiar do JavaScript que deve ser tratado com cuidado.

Por exemplo:

```
let x;
typeof x; // retorna "undefined"

typeof 123; // retorna "number"

typeof 'Hello'; // retorna "string"

typeof {}; // retorna "object"

typeof []; // retorna "object"

typeof function() {}; // retorna "function"

typeof null; // retorna "object" (cuidado com isso!)
```

Em resumo, `typeof` é uma ferramenta útil para inspecionar tipos de dados em JavaScript, mas é importante estar ciente de suas nuances e limitações, especialmente no caso de `null`.