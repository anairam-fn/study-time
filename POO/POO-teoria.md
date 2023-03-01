## Programação Orientada a Objeto (POO)

**Paradigmas da programação** se baseiam, normalmente, em alguma teoria matemática e/ou computacionall desenvolvida para resolver determinados problemas de programação de determinada forma.

- Evolução da programação

**Programação Baixo Nível:** instruções eram dadas ao computadore da maneira que ele entendia (binário, decimal...). Grande complexidade. 

**Programação Linear:** linguagens de alto nível com comandos compreensíveis pelos programadores, mas sem muita estruturação e com limitações. 

**Programação Estruturada:** permitia que pequenos pedaços de programação linear, organizados de certa maneira, pudessem ser executados fora da ordem natural das coisas. Originaram-se os sistemas. O crescimento desses sistemas ocasionou algumas falhas nos conceitos da programação estruturada. 

**Programação Modular:** permitia a criação de pequenos módulos estruturados, valorizando dados e funcionalidades, colocando eles em pequenas cápsulas protegidas que poderiam compor sistemas maiores.

**Programação Orientada a Objetos**: estrutura de objetos com características e comportamentos (métodos), que interagem uns com os outros.

1. Objetivo

Aproximar o mundo digital do mundo real.

**Postulado de Alan Kay:** “O computador ideal deve funcionar como um organismo vivo, isso é, cada célula se relaciona com outras a fim de alcançar um objetivo, mas cada uma funciona de forma autônoma. As células poderiam também reagrupar-se para resolver um outro problema ou desempenhar outras funções” 


2. Vantagens da POO

- **C**onfiável: todo software orientado a objeto é confiável. O isolamento entre as partes gera software seguro. Ao alterar uma parte, nenhuma outra é afetada.

- **O**portuno: Ao dividir tudo em partes, várias delas podem ser desenvolvidas em paralelo.

- **M**anutenível: Atualizar um software é mais fácil. Uma pequena modificação vai beneficiar todas as partes que usarem o objeto.

- **E**xtensível: O software não é estático. Ele deve crescer para permanecer útil.

- **R**eutilizável: Podemos usar objetos de um sistema que criamos em outro sistema futuro.

- **N**atural: Uma coisa natural é mais fácil de entender. Preocupa-se mais na funcionalidade do que nos detalhes de implementação.


3. O que é um Objeto?

"Coisa material ou abstrata que pode ser percebida pelos sentidos e descrita por meio das suas **características**, **comportamentos** e **estado atual**."

É uma instância de uma classe.

4. O que é uma Classe?

Como se chama um modelo de onde são tirados os objetos que compartilham atributos (o que o objeto tem), métodos (o que o objeto faz) e estados (como o objeto está).

Define os atributos e métodos comuns que serão compartilhados por um objeto.

5. Instanciamento

Geração de um novo objeto a partir de uma classe.

6. Abstração

Conceito muito importante da POO, em que se representa somente os aspectos essenciais de um objeto.

7. Visibilidade

Indica o nível de acesso aos componesntes internos (atributos e métodos) de uma classe.

(+) visibilidade **pública**: a classe atual e todas as outras classes podem ter acesso ao atributo ou método público.

(-) visibilidade **privada**: somente a classe atual tem acesso a um atributo ou método privado.

(#) visibilidade **protegida**: um atributo ou método protegido dá acesso a classe atual a todas as suas subclasses.

8. Métodos especiais

- **Métodos Acessores (Getters):** métodos que conseguem acessar algum atributo mantendo a segurança de acesso a ele.

- **Métodos Modificadores (Setters):** métodos que modificam coisas que estão dentro do objeto, garantindo a segurança do atributo.

- **Método Construtor (Construct):** recebe as propriedades que um objeto precisa ter ao ser instanciado a partir de uma classe.

9. Encapsulamento

Encapsular é ocultar partes independentes da implementação, permitindo construir partes invisíveis ao mundo exterior.

A interação com a cápsula é chamada de "mensagem".

- **Interface:** lista de serviços fornecidos por um componente. É o contato com o mundo exterior, que define o que pode ser feito com um objeto de uma classe. Canal de comunicação externa. É representada de forma parecida a de uma classe, mas não tem atributos. **Interface só possui métodos abstratos** - são métodos que não são desenvolvidos na interface .

Um software encapsulado protege o código do usuário e o usuário do código.

O encapsulamento é uma boa prática para produzir Classes mais eficiente.

- **Vantagens em encapsular:**
  - Tornar mudanças invisíveis;
  - Facilitar reutilização do código;
  - Reduzir efeito colaterais;

Ao encapsular, os atributos de uma Classe devem ser, no mínimo, protegidos, **NUNCA** públicos.

10. Herança

A herança permite basear uma nova classe na definicação de uma outra classe previamente existente e será aplicada tanto para características (propriedades) quanto para os comportamentos (métodos).

Exemplo: seres humanos, gatos e pássaros (subclasses) são animais e poderiam herdar características e comportamentos de uma superclasse Animal.

**Conceitos na Árvore Hierárquica:**
- Raiz: classe que não tem superclasses.
- Folha: subclasse que não tem subclasses.

- Descendentes e Acestrais.

- Especialização: percorrer a árvore de cima pra baixo.
- Generalização: percorrer a árvore de baixo pra cima.

**Tipos de Herança**

- **Herança de Implementação:** uma classe filha herda todos os atributos e métodos de uma classe mãe e, em seguida, adiciona ou substitui os métodos necessários para implementar o comportamento exclusivo da classe filha.
- **Herança para Diferença:** quando uma classe filha herda apenas uma parte dos atributos e métodos de uma classe mãe, e adiciona ou modifica a implementação dos atributos e métodos que não são herdados. Dessa forma, a classe filha tem alguns aspectos em comum com a classe mãe, mas é diferente o suficiente para justificar a criação de uma nova classe.

**Abstrato e Final**

- **Classe Abstrata:** não pode ser instanciada. Só pode servir como progenitora.
- **Método Abstrato:** declarado, mas não implementado na progenitora. Só pode ser colocado dentro de uma interface ou de uma classe abstrato.
- **Classe Final:** não pode ser herdada por outra classe. Obrigatoriamente folha, não pode ter "filhos".
- **Método Final:** não pode ser sobrescrito pelas suas sub-classes. Obrigatoriamente herdado.

11. Polimorfismo

Permite que um mesmo nome represente vários comportamentos diferentes.

- Assinatura do método: identificada pela ***quantidade*** e pelos ***tipos*** de parâmetros.

```java
public float calcMedia(float n1, float n2) {
  return x
}

public int calcMedia(float v1, float v2) {
  return x
}
```

Os métodos acima possuem a mesma assinatura, mesmo retornando valores diferentes e tendo o nome dos parâmetros diferentes.

- Tipos de polimorfismo

a) Sobreposição: acontece quando **substituímos** um método de uma superclasse na sua subclasse usando a **mesma assinatura**.

b) Sobrecarga: quando uma classe tem dois ou mais métodos com o mesmo nome, mas com parâmetros diferentes (**assinaturas diferentes**), permitindo que a classe possa executar uma mesma ação com diferentes tipos de dados.

POO com Java - https://www.cursoemvideo.com/curso/java-poo/
