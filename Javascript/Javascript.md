As Variáveis compostas têm a capacidade de armazenar mais de um valor, ao contrário das variáveis simples. 

Arrays são coleções ordenadas de valores, acessados por um índice numérico.

```
// Exemplo de uma array em JavaScript

let frutas = ['Maçã', 'Banana', 'Morango'];

// Acessando elementos da array

console.log(frutas[0]); // Saída: Maçã
console.log(frutas[1]); // Saída: Banana
console.log(frutas[2]); // Saída: Morango

// Adicionando um elemento ao final da array

frutas.push('Laranja');
console.log(frutas); // Saída: ['Maçã', 'Banana', 'Morango', 'Laranja']
```

Objetos são coleções não ordenadas de pares chave-valor.

```
// Exemplo de um objeto em JavaScript

let pessoa = {
    nome: 'João',
    idade: 30,
    cidade: 'São Paulo'
};

// Acessando propriedades do objeto

console.log(pessoa.nome); // Saída: João
console.log(pessoa.idade); // Saída: 30
console.log(pessoa.cidade); // Saída: São Paulo

// Alterando uma propriedade do objeto

pessoa.idade = 31;
console.log(pessoa); // Saída: { nome: 'João', idade: 31, cidade: 'São Paulo' }

```

Esses exemplos ilustram como você pode usar variáveis compostas em JavaScript para armazenar e manipular conjuntos de dados mais complexos, como listas de itens ou informações estruturadas sobre entidades.