**O que é o `trim()`?**

- O método `trim()` é uma função embutida em [[Javascript]] que remove os espaços em branco do início e do fim de uma string. Isso inclui espaços, tabs e quebras de linha.

**Quando usar?**

- Sempre que precisar limpar uma string antes de usá-la, como ao comparar, armazenar ou exibir dados.
- É útil para garantir que entradas de usuários, como nomes ou emails, não tenham espaços extras que possam causar erros.

**Exemplo Prático:**

```
let nome = "   João Silva   ";
let nomeSemEspacos = nome.trim();

console.log(nome);           // Resultado: "   João Silva   "
console.log(nomeSemEspacos); // Resultado: "João Silva"
```

**Por que isso é importante?**

- Ajuda a evitar problemas com formatações inesperadas.
- Melhora a consistência dos dados, especialmente ao lidar com entradas de usuários.

**Observação:**

- O `trim()` não altera a string original; ele retorna uma nova string com os espaços removidos.
