  # Arrays Multidimensionais em Java

## O que são?

Arrays multidimensionais são arrays que contêm outros arrays como elementos. Eles podem ser usados para representar estruturas como tabelas, matrizes ou dados de várias dimensões.

### Sintaxe

Para declarar e inicializar um array multidimensional em Java:

```java
int[][] matriz = new int[3][4]; // 3 linhas e 4 colunas
```

Você também pode inicializar diretamente os valores:

```java
int[][] matriz = {
    {1, 2, 3},
    {4, 5, 6},
    {7, 8, 9}
};
```

## Acessando elementos

Os elementos de um array multidimensional podem ser acessados usando dois índices:

```java
System.out.println(matriz[1][2]); // Acessa o elemento na linha 1, coluna 2
```

## Percorrendo arrays multidimensionais

O loop `for` é comumente usado para percorrer arrays multidimensionais:

```java
for (int i = 0; i < matriz.length; i++) {
    for (int j = 0; j < matriz[i].length; j++) {
        System.out.print(matriz[i][j] + " ");
    }
    System.out.println();
}
```

### Loop For-Each

Você também pode usar o loop `for-each`:

```java
for (int[] linha : matriz) {
    for (int elemento : linha) {
        System.out.print(elemento + " ");
    }
    System.out.println();
}
```

## Arrays Irregulares

Em Java, você pode criar arrays com tamanhos irregulares:

```java
int[][] irregular = new int[3][];
irregular[0] = new int[2];
irregular[1] = new int[4];
irregular[2] = new int[3];
```

Isso permite que cada "linha" do array tenha um número diferente de elementos.

### Acessando elementos em arrays irregulares

A lógica de acesso é a mesma, mas é necessário ter cuidado para evitar `NullPointerException` se a linha não foi inicializada:

```java
System.out.println(irregular[1][2]); // Acessa a linha 1, coluna 2
```

## Resumo

- **Arrays multidimensionais** são arrays que contêm outros arrays.
- Eles podem ser usados para representar estruturas de dados mais complexas.
- Você pode inicializar diretamente os valores ou usar tamanhos variáveis para cada linha.

### Dica

Sempre verifique o tamanho do array com `.length` antes de acessar seus elementos para evitar erros como `ArrayIndexOutOfBoundsException`.

---

