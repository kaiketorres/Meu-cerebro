
# Método `listen` em[[Node.js]]

O método **`listen`** é utilizado para iniciar um servidor e colocá-lo no estado de **escuta**. Ele é um dos métodos mais importantes ao trabalhar com servidores HTTP em Node.js.

---

## O que ele faz?

1. **Inicia o servidor**:
   - Configura o servidor para começar a escutar requisições.
   - Abre um socket na porta e/ou endereço especificados.

2. **Espera requisições**:
   - Permite que o servidor "ouça" conexões de clientes na porta definida.
   - Quando uma requisição é recebida, o callback do servidor é executado para processar e enviar respostas.

3. **Mantém o servidor em execução**:
   - O servidor permanece ativo, processando conexões até ser encerrado manualmente ou com um comando como `server.close()`.

---

## Estrutura básica

```javascript
server.listen(port, [hostname], [callback]);
```

### Parâmetros:
- **`port`**: Porta onde o servidor vai escutar (obrigatório).
- **`hostname`**: Endereço/IP onde o servidor escutará (opcional, padrão é todas as interfaces).
- **`callback`**: Função executada assim que o servidor começa a escutar (opcional).

---

## Exemplo prático

```javascript
import http from 'http';

const port = 3000;

// Cria o servidor
const server = http.createServer((req, res) => {
  res.write('Oi HTTP');
  res.end();
});

// Inicia o servidor
server.listen(port, () => {
  console.log(`Servidor rodando na porta ${port}`);
});
```

### O que acontece aqui?

1. **`server.listen`**:
   - Inicia o servidor e o coloca para escutar na porta `3000`.
2. Quando acessamos `http://localhost:3000`, o servidor:
   - Responde com "Oi HTTP".
   - Finaliza a resposta ao cliente.
3. O console exibirá a mensagem:
   ```
   Servidor rodando na porta 3000
   ```

---

## Observações importantes

- Se nenhuma `hostname` for especificada, o servidor escutará em todas as interfaces disponíveis.
- O método `listen` é **bloqueante**, ou seja, o servidor espera até que receba requisições.
- O servidor só será encerrado manualmente (`Ctrl + C`) ou com o método `server.close()`.

---


