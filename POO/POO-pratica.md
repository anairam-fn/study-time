## Programação Orientada a Objeto (POO)

1. Palavra-chave THIS

Representa o contexto em que determinada função ou método será executado.

É uma referência ao próprio objeto que chamou. Sempre que se quer modificar algum atributo dentro de uma classe, utiliza-se this na frente desse atributo.

```java

public class Caneta {
    String modelo;
    String cor;
    float ponta;
    int carga;
    boolean tampada;

    void status() {
        System.out.println("Modelo: " + this.modelo);
        System.out.println("Uma caneta " + this.cor);
        System.out.println("Ponta: " + this.ponta);
        System.out.println("Carga: " + this.carga);
        System.out.println("Esta tampada? " + this.tampada);
    }
}
```
