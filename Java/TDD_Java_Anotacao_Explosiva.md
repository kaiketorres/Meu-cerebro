
# 🧪 TDD em Java (Test-Driven Development) — DO JEITO CABULOSO

## 🤬 O que é essa porra de TDD?

**TDD (Test-Driven Development)** é basicamente você escrever os testes antes de meter a mão no código real.  
É tipo: "primeiro eu testo, depois eu codifico a desgraça."

> 📌 Regra da parada: **Red ➡ Green ➡ Refactor** (ou seja, erra ➡ acerta ➡ melhora)

---

## 🔁 Ciclo do bagulho

1. **Red** – Escreve o teste e ele falha (óbvio, tu nem escreveu o código ainda).
2. **Green** – Faz o mínimo possível pra essa porra passar.
3. **Refactor** – Dá aquele trato bonito no código sem quebrar o teste.

---

## 🛠️ Ferramentas que tu vai usar

- **JUnit** – pra escrever os testes
- **Mockito** – pra criar os mocks (objetos falsos do caralho)
- **Assertions** – tipo `assertEquals()`, `assertTrue()`, essas merdas pra checar o resultado

---

## 🧱 Estrutura de um teste decente

```java
@Test
void deveRetornarMensagem() {
    // Given (prepara a porra toda)
    Mensageiro mensageiro = new Mensageiro();

    // When (chama a função maldita)
    String msg = mensageiro.enviar("Oi");

    // Then (confere se a merda funcionou)
    assertEquals("Mensagem enviada: Oi", msg);
}
```

---

## ✅ Por que essa porra é boa?

- Menos bugs pra te dar dor de cabeça
- Tu consegue refatorar sem se cagar de medo
- Te força a pensar antes de sair digitando igual doido
- A porra do código fica mais confiável

---

## ⚠️ Dicas pra não fazer merda

- Um teste por comportamento (sem enfiar tudo junto)
- Usa `@BeforeEach` pra preparar o cenário (o tal do *fixture*)
- Se o objeto real for lento ou doido, mete um **mock** e segue o baile

---

## 🔚 Resumo

> Testa antes, codifica depois, e para de quebrar o sistema, porra.
