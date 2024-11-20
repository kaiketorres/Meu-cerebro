- `defaultProps` são usados para definir valores padrão para as props de um componente React.
- Se uma prop não for passada ao componente, ele usará o valor definido em `defaultProps`.
- Esse recurso é especialmente útil para garantir que o componente tenha um comportamento consistente, mesmo se algumas props não forem fornecidas.

**Como Usar `defaultProps`:**

- `defaultProps` são definidos como uma propriedade do próprio componente.
- Funciona para componentes de classe e componentes funcionais.

**Exemplo com Componente Funcional:**

```
function Saudacao({ nome }) {
  return <h1>Olá, {nome}!</h1>;
}

Saudacao.defaultProps = {
  nome: 'Usuário'  // Valor padrão para a prop 'nome'
};
```

- Se `Saudacao` for chamado sem um valor para `nome`, ele exibirá "Olá, Usuário!".

**Exemplo com Componente de Classe:**

```
class Botao extends React.Component {
  render() {
    return <button>{this.props.texto}</button>;
  }
}

Botao.defaultProps = {
  texto: 'Clique aqui'  // Valor padrão para a prop 'texto'
};
```

**Vantagens de Usar `defaultProps`:**

- **Evita Condicionais Desnecessárias:** Reduz a necessidade de verificar se uma prop foi passada usando operadores condicionais dentro do componente.
- **Mantém o Comportamento Consistente:** Garante que as props tenham valores previsíveis, mesmo que não sejam fornecidas.
- **Facilita Reutilização de Componentes:** Permite que você defina valores padrão sem alterar o comportamento para os casos em que as props sejam fornecidas.
**Considerações:**

- Com o uso de **destructuring**, os valores padrão podem ser definidos diretamente como parâmetros de função, tornando `defaultProps` menos necessário em muitos casos.
- Para componentes criados com **[[React ]]Hooks** ou **componentes funcionais modernos**, definir valores padrão no destructuring das props é mais comum:

```
function Saudacao({ nome = 'Usuário' }) {
  return <h1>Olá, {nome}!</h1>;
}
```

- `defaultProps` ainda é útil para componentes de classe e para alguns cenários específicos em componentes funcionais.

**Resumo:** `defaultProps` permite definir valores padrão para props, ajudando a evitar comportamentos indesejados quando props são omitidas. É útil para garantir que os componentes sempre tenham dados para trabalhar e que se comportem de maneira previsível.