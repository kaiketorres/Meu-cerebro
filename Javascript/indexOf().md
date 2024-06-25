O método `indexOf()` em [[Javascript]]é usado para encontrar a primeira ocorrência de um elemento em um array ou uma substring em uma string e retorna o índice dessa ocorrência. Aqui está um resumo sucinto:

**Em Arrays**:

- `indexOf()` busca a primeira ocorrência de um elemento no array e retorna seu índice.

```
let array = [10, 20, 30, 40, 50];
let indice = array.indexOf(30);

console.log(indice); // Saída: 2
```

Se o elemento não for encontrado, retorna `-1`.

```
let indiceNaoEncontrado = array.indexOf(100);

console.log(indiceNaoEncontrado); // Saída: -1
```

**Em Strings**:

- `indexOf()` procura a primeira ocorrência de uma substring na string e retorna seu índice.

```
let frase = "Olá, mundo!";
let indice = frase.indexOf("mundo");

console.log(indice); // Saída: 5
```

Aceita um segundo parâmetro opcional para indicar a partir de qual índice iniciar a busca.

```
let indice2 = frase.indexOf("m", 7); // Busca a partir do índice 7
console.log(indice2); // Saída: -1 (porque não há "m" após o índice 7)
```

Em resumo, `indexOf()` é útil para encontrar a posição de elementos específicos em arrays e substrings em strings. Ele retorna `-1` se o elemento não for encontrado.