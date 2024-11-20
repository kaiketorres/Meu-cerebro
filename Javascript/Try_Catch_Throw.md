
# Anotação sobre `try`, `catch` e `throw` em [[JavaScript]]

Hoje eu aprendi sobre como tratar erros em JavaScript usando os blocos `try`, `catch` e a palavra-chave `throw`.

## O que aprendi

- **`throw`**: Usado para lançar um erro manualmente. No código que fizemos, usei o `throw` para lançar um erro caso os valores passados para a função não sejam números. Isso ajuda a garantir que a função só execute se os parâmetros forem válidos.
  
- **`try`**: O bloco `try` é usado para envolver o código que pode gerar um erro. Se o código dentro de `try` falhar, o erro será capturado pelo `catch`.
  
- **`catch`**: O bloco `catch` captura qualquer erro lançado no bloco `try`. É aqui que colocamos o código que lidará com o erro. No meu exemplo, a mensagem amigável será exibida para o usuário se o erro ocorrer.

## Código que criei

```javascript
const soma = (x, y) => {
   if (
      typeof x !== 'number' ||
      typeof y !== 'number') {
      throw new Error('x e y precisam ser numeros')
   }
   return x + y
}

try {
   console.log(soma(1, 2)) // Deve funcionar
   console.log(soma(1, '2')) // Vai gerar um erro
} catch (e) {
   console.log('Alguma coisa mais amigavel para o usuario')
}
```

## Explicação do código

1. A função `soma` recebe dois parâmetros (`x` e `y`).
2. Dentro da função, usamos `typeof` para verificar se os parâmetros são números. Se algum deles não for, lançamos um erro com `throw new Error('x e y precisam ser numeros')`.
3. Se ambos forem números, a soma é realizada e o resultado é retornado.
4. No bloco `try`, tentamos chamar a função `soma` duas vezes. A primeira chamada (`soma(1, 2)`) vai funcionar normalmente, mas a segunda (`soma(1, '2')`) vai lançar um erro, porque o segundo parâmetro não é um número.
5. O bloco `catch` captura esse erro e exibe uma mensagem amigável para o usuário, evitando que o programa quebre.

## Reflexões

Eu achei que o uso de `throw` é uma maneira prática de garantir que os erros sejam tratados de forma controlada, e o `try...catch` permite que eu forneça uma resposta amigável ao usuário em vez de deixar o programa quebrar. É uma maneira mais profissional de lidar com erros!

Agora vou tentar mais exemplos de como lidar com diferentes tipos de erros e aprimorar minhas habilidades com `try`, `catch` e `throw`.
