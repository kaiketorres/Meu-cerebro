### Funções em JavaScript

Uma função  em [[Javascript]] é um bloco de código que pode ser chamado e executado sempre que necessário. Elas são úteis para agrupar um conjunto de instruções que realizam uma tarefa específica, permitindo reutilização de código e organização lógica.

#### Declaração de uma Função

Existem várias maneiras de declarar funções em JavaScript:

1. **Função Declarada**:

```
function nomeDaFuncao(param1, param2) {
    // código a ser executado
}
```

2. **Função Expressa**:

```
const nomeDaFuncao = function(param1, param2) {
    // código a ser executado
};
```

3. **Função de Flecha (Arrow Function)**:

```
const nomeDaFuncao = (param1, param2) => {
    // código a ser executado
};
```

### Exemplo de Função

Aqui está um exemplo de uma função simples que calcula a soma de dois números e retorna o resultado:

```
function soma(a, b) {
    return a + b;
}

// Chamando a função
let resultado = soma(5, 3);
console.log(resultado);  // Saída: 8
```

Neste exemplo:

- `function soma(a, b)` declara uma função chamada `soma` que aceita dois parâmetros, `a` e `b`.
- `return a + b;` realiza a soma dos parâmetros e retorna o resultado.
- `soma(5, 3)` chama a função com os argumentos `5` e `3`, e o resultado é armazenado na variável `resultado`.
- `console.log(resultado);` imprime o resultado no console, que será `8`.