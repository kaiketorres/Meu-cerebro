O operador ternário é uma forma concisa de escrever uma expressão condicional em [[Javascript]]. Ele permite executar uma expressão baseada em uma condição de maneira mais compacta do que usando a estrutura `if-else`.

### Estrutura Básica

A estrutura básica do operador ternário é:

```
condição ? expressãoSeVerdadeiro : expressãoSeFalso;
```

- **condição**: Uma expressão que é avaliada como `true` ou `false`.
- **expressão Se Verdadeiro**: O código que será executado se a condição for `true`.
- **expressão Se Falso**: O código que será executado se a condição for `false`.

### Funcionamento

- O operador ternário avalia a condição.
- Se a condição for `true`, ele executa e retorna `expressãoSeVerdadeiro`.
- Se a condição for `false`, ele executa e retorna `expressãoSeFalso`.

### Exemplos

#### Exemplo 1: Uso Simples

```
const idade = 18;
const podeVotar = idade >= 18 ? 'Pode votar' : 'Não pode votar';
console.log(podeVotar); // Output: 'Pode votar'
```

Exemplo 2: Uso em JSX (React/[[React  Native]])

```
import React from 'react';
import { Text } from 'react-native';

const MeuComponente = ({ ver }) => {
  return (
    {ver ? <Text>Curso de React Native</Text> : <Text>...</Text>}
  );
};
```

### Vantagens

- **Conciso**: Escreve uma condição em uma única linha, economizando espaço e tornando o código mais limpo.
- **Legível**: Para expressões simples, pode ser mais fácil de ler do que uma estrutura `if-else` completa.

### Desvantagens

- **Complexidade**: Para condições complexas, o operador ternário pode se tornar difícil de ler e entender.
- **Legibilidade**: Pode reduzir a legibilidade se usado em excesso ou em expressões complexas.

### Comparação com `if-else`

```
// Usando if-else
let resultado;
if (condição) {
  resultado = expressãoSeVerdadeiro;
} else {
  resultado = expressãoSeFalso;
}

// Usando operador ternário
let resultado = condição ? expressãoSeVerdadeiro : expressãoSeFalso;
```



Em resumo, o operador ternário é uma ferramenta útil para simplificar condições simples e tornar o código mais conciso. No entanto, para condições complexas, `if-else` ainda pode ser a escolha mais legível.