## O que é um Construtor?
Um **construtor** é um método especial em Java usado para inicializar objetos. Ele é chamado automaticamente quando um objeto de uma classe é criado.

## Características dos Construtores:
- Possuem o mesmo nome da classe.
- Não possuem um tipo de retorno (nem mesmo `void`).
- São chamados automaticamente quando um objeto é instanciado.

## Tipos de Construtores

### 1. Construtor Padrão (Default)
Se nenhuma classe definir um construtor, o Java fornece um construtor padrão sem argumentos.

```java
class Pessoa {
    // Construtor padrão (implicado)
    void mostrarMensagem() {
        System.out.println("Olá, sou uma pessoa!");
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p = new Pessoa(); // Chamada do construtor padrão
        p.mostrarMensagem();
    }
}
```

### 2. Construtor Personalizado (Com Parâmetros)
Podemos definir um construtor para inicializar atributos da classe.

```java
class Pessoa {
    String nome;

    // Construtor personalizado
    Pessoa(String nome) {
        this.nome = nome;
    }

    void mostrarNome() {
        System.out.println("Nome: " + nome);
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p = new Pessoa("Kaique");
        p.mostrarNome();
    }
}
```

### 3. Construtor Sobrecarga (Overloading)
Podemos definir múltiplos construtores com diferentes parâmetros.

```java
class Pessoa {
    String nome;
    int idade;

    // Construtor 1
    Pessoa(String nome) {
        this.nome = nome;
    }

    // Construtor 2
    Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    void mostrarDados() {
        System.out.println("Nome: " + nome + ", Idade: " + idade);
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p1 = new Pessoa("Kaique");
        Pessoa p2 = new Pessoa("Lucas", 25);

        p1.mostrarDados();
        p2.mostrarDados();
    }
}
```

## Uso do `this()` para Chamar Construtores
Podemos chamar um construtor dentro de outro usando `this()`, para evitar repetição de código.

```java
class Pessoa {
    String nome;
    int idade;

    Pessoa(String nome) {
        this(nome, 18); // Chamando outro construtor
    }

    Pessoa(String nome, int idade) {
        this.nome = nome;
        this.idade = idade;
    }

    void mostrarDados() {
        System.out.println("Nome: " + nome + ", Idade: " + idade);
    }
}

public class Main {
    public static void main(String[] args) {
        Pessoa p1 = new Pessoa("Kaique");
        p1.mostrarDados();
    }
}
```

## Construtor Privado (Singleton Pattern)
Construtores privados impedem que a classe seja instanciada externamente. Esse conceito é usado no **Singleton Pattern**.

```java
class Singleton {
    private static Singleton instancia;

    private Singleton() {} // Construtor privado

    public static Singleton getInstance() {
        if (instancia == null) {
            instancia = new Singleton();
        }
        return instancia;
    }
}

public class Main {
    public static void main(String[] args) {
        Singleton obj = Singleton.getInstance();
        System.out.println("Objeto Singleton criado: " + obj);
    }
}
```

---

