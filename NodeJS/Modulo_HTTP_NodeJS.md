
# Módulo `http` em [[Node.js]]

O módulo **`http`** em Node.js é um dos principais módulos embutidos na linguagem, usado para criar e gerenciar servidores HTTP. Ele permite manipular tanto requisições quanto respostas HTTP.

---

## O que é o módulo `http`?

- É um módulo nativo do Node.js.
- Permite criar servidores que processam requisições e enviam respostas utilizando o protocolo HTTP.
- Fornece métodos e classes para trabalhar com servidores HTTP e clientes.

---

## Principais métodos e classes

### 1. **`http.createServer(callback)`**
- Cria um servidor HTTP.
- Aceita um callback com dois parâmetros:
  - **`req`**: Representa a requisição feita pelo cliente.
  - **`res`**: Representa a resposta enviada pelo servidor.

Exemplo:
```javascript
import http from 'http';

const server = http.createServer((req, res) => {
  res.write('Oi HTTP'); // Envia uma mensagem de resposta
  res.end();            // Finaliza a resposta
});
```

### 2. **`server.listen(port, [hostname], [callback])`**
- Coloca o servidor em estado de escuta para receber requisições.

Exemplo:
```javascript
server.listen(3000, () => {
  console.log('Servidor rodando na porta 3000');
});
```

### 3. **Eventos do servidor**
O servidor pode responder a eventos, como:
- **`request`**: Quando uma requisição é recebida.
- **`close`**: Quando o servidor é encerrado.

Exemplo:
```javascript
server.on('request', (req, res) => {
  console.log('Nova requisição recebida');
});
```

### 4. **Requisições HTTP (objeto `req`)**
- Contém informações sobre a requisição do cliente, como:
  - **`req.method`**: Método HTTP usado (ex.: `GET`, `POST`).
  - **`req.url`**: URL requisitada pelo cliente.
  - **`req.headers`**: Cabeçalhos HTTP da requisição.

Exemplo:
```javascript
server.on('request', (req, res) => {
  console.log(`Método: ${req.method}, URL: ${req.url}`);
});
```

### 5. **Respostas HTTP (objeto `res`)**
- Permite enviar respostas ao cliente.
- Métodos comuns:
  - **`res.writeHead(statusCode, headers)`**: Define o código de status e os cabeçalhos da resposta.
  - **`res.write(data)`**: Escreve o corpo da resposta.
  - **`res.end()`**: Finaliza a resposta.

Exemplo:
```javascript
server.on('request', (req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/plain' });
  res.write('Resposta do servidor');
  res.end();
});
```

---

## Exemplo prático completo

```javascript
import http from 'http';

const server = http.createServer((req, res) => {
  if (req.url === '/') {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Bem-vindo à página inicial!');
  } else if (req.url === '/sobre') {
    res.writeHead(200, { 'Content-Type': 'text/plain' });
    res.end('Sobre nós');
  } else {
    res.writeHead(404, { 'Content-Type': 'text/plain' });
    res.end('Página não encontrada');
  }
});

server.listen(3000, () => {
  console.log('Servidor rodando na porta 3000');
});
```

---

## Observações importantes

- O módulo `http` é ideal para criar servidores simples e eficientes.
- Para servidores mais robustos ou com roteamento complexo, considere usar bibliotecas como **Express.js**.

---

