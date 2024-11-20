**JSX (JavaScript XML) - Anotação para Estudos em [[React]]  e [[React  Native]]**

- **O que é JSX**: É uma extensão de sintaxe do JavaScript usada em React. Ele permite escrever o que se parece com HTML diretamente no código JavaScript. Embora pareça HTML, JSX é convertido em JavaScript na hora da execução.
    
- **Por que usar JSX?**: Facilita a criação de interfaces ao combinar a estrutura da interface (HTML) e a lógica (JavaScript) no mesmo arquivo. Isso deixa o código mais claro e fácil de manter.
    
- **Como funciona JSX**: Durante a build, o JSX é transformado em chamadas de função `React.createElement()`. Isso significa que o JSX, embora pareça HTML, cria elementos React de forma mais eficiente.
    
- **Sintaxe Básica**:
    
    - Usar **chaves** (`{}`) para expressões JavaScript dentro do JSX.
    - Todos os elementos devem estar **fechados** (ex.: `<img />`).
    - JSX precisa de **um elemento pai** para encapsular os elementos retornados.
- **Exemplo**:

```
function Welcome() {
  const name = 'Mundo';
  return <h1>Olá, {name}!</h1>;
}
```

- Nesse exemplo, a função retorna um elemento JSX que exibe “Olá, Mundo!” no navegador.
    
- **Regras Importantes**:
    
    - **Class** em HTML vira `className` no JSX.
    - Todos os elementos precisam de um **fechamento** (self-closing tag).
    - **Fragmentos** (`<>...</>`) podem ser usados para evitar divs extras, permitindo retorno de múltiplos elementos.

JSX é um recurso poderoso do React que melhora a legibilidade e facilita o desenvolvimento de UIs dinâmicas.