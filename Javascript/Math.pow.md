A função `Math.pow` em [[Javascript]] é usada para elevar um número a uma determinada potência. Ela recebe dois argumentos: o primeiro é a base e o segundo é o expoente.

A sintaxe é a seguinte:

```
Math.pow(base, expoente)
```

Aqui está um exemplo simples de como usar `Math.pow`:

```
let base = 2;
let expoente = 3;

let resultado = Math.pow(base, expoente);
console.log(resultado); // Saída: 8

```

Neste exemplo:

- `Math.pow(2, 3)` calcula 2 elevado à potência de 3, que é 8.

Para integrar `Math.pow` no cálculo do IMC, o código ficaria assim:

```
function calcularIMC(peso, altura) {
    // Altura em metros deve ser elevada ao quadrado usando Math.pow
    let alturaAoQuadrado = Math.pow(altura, 2);
    
    // Cálculo do IMC
    let imc = peso / alturaAoQuadrado;
    
    // Retornando o valor do IMC
    return imc;
}

// Exemplo de uso
let peso = 70; // Peso em quilogramas
let altura = 1.75; // Altura em metros

let imc = calcularIMC(peso, altura);
console.log("O IMC é: " + imc.toFixed(2)); // Arredondando para duas casas decimais
```

Neste código:

- `Math.pow(altura, 2)` é usado para elevar a altura ao quadrado. Isso substitui a operação `altura * altura` usada anteriormente.
