- Props (propriedades) são a forma de passar dados de um componente pai para um componente filho.
- São imutáveis dentro do componente que as recebe.
- Servem para tornar componentes mais dinâmicos e configuráveis.

**Como Usar Props:**

- São passadas como atributos em elementos[[JSX]].

- Exemplo:
```
function Saudacao(props) {
  return <h1>Olá, {props.nome}!</h1>;
}
function App() {
  return <Saudacao nome="Ana" />;
}

```

**Características Principais:**

- **Fluxo unidirecional:** Props fluem sempre do pai para o filho.
- **Somente leitura:** Não podem ser modificadas dentro do componente que as recebe.
- **Reutilização de componentes:** Permitem que um mesmo componente seja usado com diferentes dados.

**Passando Funções como Props:**

- Permite que componentes filhos executem funções definidas no componente pai.
- Exemplo:

```
function Botao(props) {
  return <button onClick={props.aoClicar}>Clique aqui</button>;
}
function App() {
  function handleClick() {
    alert('Botão clicado!');
  }
  return <Botao aoClicar={handleClick} />;
}

```

**Destructuring de Props:**

- Simplifica a extração de valores diretamente.

- Exemplo:

```
function Saudacao({ nome }) {
  return <h1>Olá, {nome}!</h1>;
}
```

**Vantagens das Props:**

- **Flexibilidade e Personalização:** Componente pode se adaptar conforme as props recebidas.
- **Componentização Reutilizável:** Torna possível reutilizar componentes em diferentes contextos.
- **Facilidade de Passar Dados e Funções:** Permite comunicação fácil entre componentes pai e filho.

**Resumo:**  
Props são fundamentais para a comunicação entre componentes [[React]], ajudando a compartilhar dados e funções de maneira eficiente e a manter a aplicação modular e organizada.