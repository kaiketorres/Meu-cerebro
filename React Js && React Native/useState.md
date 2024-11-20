- `useState` é um **hook** que permite adicionar estado a componentes funcionais em [[React]].
- Antes da introdução dos hooks, apenas componentes de classe podiam gerenciar estado. `useState` tornou possível gerenciar o estado em componentes funcionais de maneira mais simples.

**Como Usar `useState`:**

- O `useState` é importado do React e retorna um array com dois elementos: o estado atual e uma função para atualizar esse estado.
- A sintaxe básica é:

```
const [estado, setEstado] = useState(valorInicial);

```

- `estado` é o valor atual do estado.
- `setEstado` é a função usada para atualizar o valor do estado.
- `valorInicial` é o valor inicial do estado.

**Exemplo Básico de Uso:**

```
import React, { useState } from 'react';

function Contador() {
  // Declara uma variável de estado chamada "contagem" com valor inicial 0
  const [contagem, setContagem] = useState(0);

  return (
    <div>
      <p>Você clicou {contagem} vezes</p>
      <button onClick={() => setContagem(contagem + 1)}>
        Clique aqui
      </button>
    </div>
  );
}
```

- O estado `contagem` é inicializado com `0`.
- Quando o botão é clicado, `setContagem(contagem + 1)` é chamado para atualizar o estado.

**Principais Características:**

1. **Estado Inicial:** O valor inicial passado para `useState` é usado apenas na primeira renderização.
2. **Função de Atualização:** A função `setEstado` pode ser usada para alterar o valor do estado. Chamadas para `setEstado` re-renderizam o componente com o novo valor.
3. **Comportamento Assíncrono:** As atualizações de estado podem ser agrupadas e não são imediatas. Isso significa que mudanças no estado podem não ser refletidas imediatamente no código seguinte.
4. **Valores Complexos:** `useState` pode armazenar qualquer tipo de valor: strings, números, objetos, arrays, funções, etc.

**Atualização com Função:**

- Se o próximo estado depende do estado anterior, é uma boa prática usar uma função de atualização:

```
setEstado(prevEstado => prevEstado + 1);

```

**Gerenciando Estado Complexo:**

- Quando o estado é um objeto ou array, é importante lembrar que `useState` não mescla automaticamente os valores. Você precisa fazer isso manualmente usando, por exemplo, o **spread operator**:

```
const [usuario, setUsuario] = useState({ nome: '', idade: 0 });

// Atualizando apenas o campo "nome"
setUsuario(prevUsuario => ({ ...prevUsuario, nome: 'Maria' }));

```


**Resumo:**

- **`useState`** permite adicionar estado a componentes funcionais, tornando-os mais dinâmicos e interativos.
- **Facilidade e Legibilidade:** Substitui a complexidade de gerenciar estado em componentes de classe com uma abordagem mais simples.
- **Reatividade:** Atualizar o estado com `setEstado` causa a re-renderização do componente para refletir as mudanças.

`useState` é um dos hooks mais usados em React e fornece uma maneira eficiente de gerenciar o estado em componentes funcionais.