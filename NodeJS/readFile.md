
# [[Node.js]] - Comando `readFile`

## O que é?
O `readFile` é um método do módulo `fs` (File System) no Node.js usado para ler o conteúdo de arquivos de forma assíncrona.

## Sintaxe
```javascript
const fs = require('fs');

fs.readFile('caminho/para/arquivo.txt', 'utf8', (err, data) => {
    if (err) {
        console.error('Erro ao ler o arquivo:', err);
        return;
    }
    console.log('Conteúdo do arquivo:', data);
});
```
## Parâmetros
1. **Caminho do arquivo**: String que especifica o caminho para o arquivo que será lido.
2. **Codificação (opcional)**: Exemplo: `'utf8'`. Define como o arquivo será decodificado.
3. **Callback**: Função que recebe dois parâmetros:
    - **err**: Contém o erro, caso aconteça.
    - **data**: Contém o conteúdo do arquivo lido.

## Exemplos
### Ler um arquivo de texto simples
```javascript
const fs = require('fs');

fs.readFile('exemplo.txt', 'utf8', (err, data) => {
    if (err) {
        console.error('Erro:', err);
    } else {
        console.log('Conteúdo:', data);
    }
});
```

### Sem definir a codificação
Se a codificação não for especificada, o `data` será retornado como um buffer:
```javascript
fs.readFile('exemplo.txt', (err, data) => {
    if (err) throw err;
    console.log(data); // Exibe um buffer
});
```

## Tratamento de erros
É importante sempre tratar erros para evitar falhas inesperadas no programa:
```javascript
fs.readFile('arquivo-inexistente.txt', 'utf8', (err, data) => {
    if (err) {
        console.error('Arquivo não encontrado:', err.message);
        return;
    }
    console.log(data);
});
```

## Dicas
- Para operações síncronas, use `fs.readFileSync` (bloqueia o loop de eventos, então use com cautela).
- Combine com Promises (`fs.promises.readFile`) para evitar callbacks e usar `async/await`.

## Referências
- [Documentação oficial do Node.js](https://nodejs.org/api/fs.html#fsreadfilepath-options-callback)
