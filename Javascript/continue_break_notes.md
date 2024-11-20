
# Notas sobre continue e break no [[JavaScript]]

### Código de exemplo:
```js
const numeros = [1, 2, 3, 4, 5, 6, 7, 8, 9];

for (let numero of numeros) {
  if (numero === 2) {
    console.log('Pulei o número 2');
    continue; // Ignora o restante do bloco e passa para a próxima iteração do loop
  }

  if (numero === 7) {
    console.log('7 encontrado, saindo...');
    break; // Sai do loop completamente
  }

  console.log(numero); // Executado se nenhum dos `if` for acionado
}
```

### Explicação:
- **`continue`**: Quando usado, ele faz o loop pular a execução do código abaixo dele na iteração atual e ir direto para a próxima iteração.  
  - **Exemplo:** No código acima, quando `numero` é igual a `2`, a mensagem 'Pulei o número 2' é exibida e o `continue` faz o loop avançar para o próximo número, sem executar `console.log(numero)`.

- **`break`**: Este comando finaliza o loop assim que é encontrado. O código abaixo dele não será executado, e o controle do programa sai do loop.  
  - **Exemplo:** Quando `numero` é igual a `7`, a mensagem '7 encontrado, saindo...' é exibida e o `break` faz o loop parar imediatamente.

### Saída esperada:
```
1
Pulei o número 2
3
4
5
6
7 encontrado, saindo...
```
