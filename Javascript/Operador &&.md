O operador lógico `&&` (AND) é utilizado para verificar se duas condições são verdadeiras ao mesmo tempo. Se ambos os operandos forem verdadeiros, ele retorna `true`. Caso qualquer um dos operandos seja falso, ele retorna `false`. [[Javascript]]

Sintaxe:

```
condição1 && condição2
```

Exemplo de uso:

```
let a = 5;
let b = 10;

if (a > 0 && b > 5) {
  console.log("Ambas as condições são verdadeiras.");
} else {
  console.log("Uma das condições é falsa.");
}
```

No exemplo acima, o código dentro do `if` só será executado se ambas as condições (`a > 0` e `b > 5`) forem verdadeiras.

- **Comportamento de curto-circuito**:  
    Se a primeira condição for falsa, o JavaScript nem verifica a segunda condição, já que o resultado será `false` de qualquer maneira.

### Exemplo com curto-circuito:

```
let x = 0;
let y = 10;

if (x !== 0 && y > 5) {
  console.log("Essa mensagem não será exibida.");
}
```

Como `x !== 0` é falso, a segunda condição nem é verificada.

### Conclusão:

O operador `&&` é ideal para casos onde você deseja garantir que várias condições sejam verdadeiras ao mesmo tempo antes de executar um bloco de código.


Código:

```
console.log('Luiz Otavio' && 0 && 'Maria');
```

### Explicação:

No JavaScript, o operador lógico `&&` (AND) retorna o **primeiro valor "falsy"** que encontrar ao avaliar uma sequência de expressões, ou o último valor se todas as expressões forem "truthy".

#### Avaliação passo a passo:

1. **`'Luiz Otavio'`**: Strings não vazias são consideradas **truthy** em JavaScript. Portanto, `'Luiz Otavio'` é truthy.
    
2. **`0`**: O número `0` é considerado um valor **falsy** em JavaScript. Como o operador `&&` encontra esse valor falsy, ele para a avaliação e retorna `0`.
    
3. **`'Maria'`**: Não é avaliado, porque o operador `&&` já encontrou um valor falsy (`0`) e interrompeu a execução.
    

### Resumo:

- O operador `&&` retorna o **primeiro valor falsy** encontrado. No caso deste código, `0` é falsy, então ele é o valor retornado e, por isso, o código imprime `0` no console.

A expressão é interrompida assim que encontra o valor `0`, ignorando qualquer avaliação posterior.