O `use strict` em [[Javascript]] é uma instrução que ativa o modo estrito do JavaScript. Esse modo foi introduzido no ECMAScript 5 (ES5) e é uma forma de escrever código JavaScript mais robusto, ajudando a evitar erros comuns. Quando o modo estrito está ativado, certas práticas que são permitidas no modo não estrito (modo "sloppy") são tratadas como erros.

### Como ativar o modo estrito

Para ativar o modo estrito, basta adicionar a string `"use strict";` no início do seu script ou no início de uma função.

#### No nível de script

```
"use strict";

function exemplo() {
    // Código aqui estará em modo estrito
}
```

No nível de função

```
function exemplo() {
    "use strict";
    // Código aqui estará em modo estrito
}
```

### Benefícios do modo estrito

1. **Erros silenciosos se tornam explícitos:** Muitos erros que seriam ignorados ou falariam silenciosamente no modo não estrito gerarão exceções no modo estrito, facilitando a identificação e correção de problemas.
    
2. **Prevenção de variáveis globais acidentais:** No modo não estrito, atribuir um valor a uma variável que não foi declarada cria uma variável global. No modo estrito, isso gera um erro.

```
"use strict";
x = 10; // Gera um erro, pois x não foi declarado

```

3. Eliminação de algumas más práticas:** O modo estrito elimina alguns comportamentos do JavaScript que são confusos ou considerados más práticas.

- Não permite a duplicação de parâmetros em funções:
```
"use strict";
function soma(a, a, c) { // Gera um erro
    return a + a + c;
}
```

Não permite a exclusão de propriedades não removíveis:

```
"use strict";
delete Object.prototype; // Gera um erro
```

4. **Restrição de uso do `eval`:** No modo estrito, o `eval` não introduz novas variáveis no escopo circundante.  

```
"use strict";
eval("var x = 2");
console.log(x); // Gera um erro, pois x não está definido
```

5. **Mais segurança no `this`:** No modo estrito, o valor de `this` em funções que não são chamadas como métodos é `undefined`, em vez de ser o objeto global. Isso pode ajudar a evitar erros quando funções são chamadas de forma incorreta.

```
"use strict";
function saudacao() {
    console.log(this);
}
saudacao(); // undefined
```

### Quando usar o modo estrito

É uma boa prática usar o modo estrito em novos projetos ou ao refatorar código existente. Ele ajuda a escrever um código mais seguro, detecta erros mais cedo e torna o JavaScript mais previsível.

Se tiver mais dúvidas sobre o uso de `use strict` ou qualquer outra coisa, sinta-se à vontade para perguntar!