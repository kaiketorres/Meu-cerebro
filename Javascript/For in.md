
- O `for...in` é usado para **iterar sobre as propriedades enumeráveis** de um objeto ou sobre as chaves de um array.
- Ele **retorna o nome da propriedade ou o índice**, não o valor diretamente.

```
const pessoa = {nome: 'João', idade: 25};
for (let chave in pessoa) {
  console.log(chave); // imprime 'nome' e 'idade'
}
```

Exemplo com array:

```
const numeros = [10, 20, 30];
for (let indice in numeros) {
  console.log(indice); // imprime 0, 1, 2 (os índices)
}
```

- **Usado mais com objetos** do que arrays, pois o foco é nas **propriedades** e **não necessariamente nos valores**.
- No caso de arrays, usar `for...in` **não é muito recomendado**, já que ele percorre as chaves (índices) e não os valores. Para arrays, o `for...of` seria mais adequado.
- Importante: o `for...in` percorre **todas as propriedades enumeráveis**, o que inclui as propriedades herdadas de protótipos, então é importante tomar cuidado para evitar pegar propriedades indesejadas.