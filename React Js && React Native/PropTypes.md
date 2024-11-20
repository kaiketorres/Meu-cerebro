`- **PropTypes** são uma ferramenta de validação de tipos de props em[[React]].
- Permitem verificar se as props passadas para um componente têm o tipo correto, ajudando a identificar bugs ou inconsistências.
- Não são necessárias, mas são úteis para garantir que um componente seja utilizado corretamente.

**Como usar PropTypes:**

- É necessário importar `PropTypes` do pacote `prop-types`.

- As validações são definidas como propriedades do componente.

	
```
import PropTypes from 'prop-types';

function Saudacao({ nome, idade }) {
  return (
    <div>
      <h1>Olá, {nome}!</h1>
      <p>Idade: {idade}</p>
    </div>
  );
}

Saudacao.propTypes = {
  nome: PropTypes.string.isRequired, // 'nome' deve ser uma string obrigatória
  idade: PropTypes.number            // 'idade' deve ser um número
};	
```

**Principais Validações:**

- `PropTypes.string`: Valor deve ser uma string.
- `PropTypes.number`: Valor deve ser um número.
- `PropTypes.bool`: Valor deve ser um booleano.
- `PropTypes.array`: Valor deve ser um array.
- `PropTypes.object`: Valor deve ser um objeto.
- `PropTypes.func`: Valor deve ser uma função.
- `PropTypes.node`: Qualquer coisa que pode ser renderizada (números, strings, elementos ou arrays de elementos).
- `PropTypes.element`: Um elemento React.
- `PropTypes.oneOf([valor1, valor2])`: Valor deve ser um entre os valores especificados.
- `PropTypes.arrayOf(tipo)`: Array de elementos de um determinado tipo.
- `PropTypes.shape({ chave: tipo })`: Objeto com formato específico.

**Propriedades Opcionais e Obrigatórias:**

- Para marcar uma prop como obrigatória, adiciona-se `.isRequired`.
    - Exemplo: `PropTypes.string.isRequired`

**Quando Usar PropTypes:**

- Durante o desenvolvimento, para garantir que o componente seja usado corretamente com os dados esperados.
- Em grandes equipes ou projetos colaborativos, PropTypes ajudam a documentar os componentes e as props que eles requerem.

**Limitações:**

- PropTypes são verificadas apenas em tempo de execução, não em tempo de compilação.
- Não são tão robustas quanto ferramentas de tipagem estática como TypeScript.

**Vantagens do Uso:**

- **Documentação automática:** Facilita a compreensão das props que um componente espera.
- **Detecção de Erros:** Ajuda a identificar rapidamente quando as props erradas ou ausentes são passadas para um componente.
- **Manutenção:** Auxilia na manutenção, pois torna o comportamento esperado de um componente mais claro.