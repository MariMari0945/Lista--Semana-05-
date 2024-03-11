# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina!
- ao final, publique seu arquivo lista_01.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** O que o código a seguir faz?

![Uma imagem](assets/ex01.PNG)

Escolha a opção que responde corretamente:

a) Imprime os números pares de 1 a 10.

b) Imprime os números ímpares de 1 a 10.

c) Imprime os números pares de 2 a 10. [Correta]

d) Imprime os números ímpares de 2 a 10.

______

**2)** Identificar a linha que falta no código para criar uma classe Veiculo com atributo marca, e uma classe Carro que herda de Veiculo com um método ligar(). 

![Uma imagem](assets/ex02.PNG)

No lugar onde está escrito “// linha” qual das opções abaixo deve estar para funcionar corretamente o código?

A) let carro = new Carro("Toyota"); [Correta]

B) let ligar = new ligar("Toyota");

C) class Moto extends Veiculo {};

D) carro1.ligar();

______

**3)** Qual é o valor de resultado após a execução deste código?

![Uma imagem](assets/ex03.PNG)

Escolha a opção que responde corretamente:

A) 18 [Correta]

B) 16

C) 14

D) 12

______

**4)** Como você criaria um método `acelerar()` em uma classe `Carro`, que recebe um parâmetro `velocidade` e o adiciona a um atributo `velocidadeAtual`?

A) ![Uma imagem](assets/ex04_1.PNG) [Correta]

B) ![Uma imagem](assets/ex04_2.PNG)

C) ![Uma imagem](assets/ex04_3.PNG)

D) ![Uma imagem](assets/ex04_4.PNG)

______

**5)** Qual a forma correta de definir uma classe Carro em JavaScript, com um método ligar() e um atributo marca?

A) ![Uma imagem](assets/ex05_1.PNG) [Correta]

B) ![Uma imagem](assets/ex05_2.PNG)

C) ![Uma imagem](assets/ex05_3.PNG)

D) ![Uma imagem](assets/ex05_4.PNG)

______

**6)** Observe o código abaixo:

![Uma imagem](assets/ex06.PNG)

Qual será a saída do código acima?

A) "Olá, meu nome é João. Olá, meu nome é Maria." [Correta]

B) "Olá, meu nome é ."

C) "João Maria"

D) "undefined undefined"

______

# Questões dissertativas

**7)** Vamos criar um programa em JavaScript para entender classes, métodos e atributos!
Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método chamado descrever() na classe Animal.
  - Este método deve exibir no console uma descrição do animal com seu nome e idade.

  Criando e manipulando Animais:
- Crie dois objetos da classe Animal: um chamado "cachorro" e outro "gato", com idades distintas.
- Para cada animal, chame o método descrever() para ver a descrição no console.

Dica: Utilize `console.log()` para exibir as informações!

  Resposta:
```Javascript
  // Criação de uma classe
class Animal {
    
    //Definição dos atributos
    constructor(nome, idade) { 
        this.nome = nome;
        this.idade = idade;
    }

    // Criação do método "descrever" para explicitar a descrição do animal
    descrever() {
      console.log("Oie! Esse é o(a)" + this.nome + ", e ele(a) tem " + this.idade + "anos de idade!");
    }
  }

  // Definição dos objetos disponível
  const cachorro = new Animal("Pretão", 7)
  const gato = new Animal("Chaninha", 11)

  // Retomada do método para impressão específica de cada animal
  cachorro.descrever();
  gato.descrever();
  ```

_______

**8)** Nos últimos dias tivemos a oportunidade de ter contato com Programação Orientada a Objetos, e tivemos contato com o tema "herança". Herança é um princípio de orientação a objetos, que permite que classes compartilhem atributos e métodos. Ela é usada na intenção de reaproveitar código ou comportamento generalizado ou especializar operações ou atributos. Então vamos praticar esse conteúdo nessa questão.
Vamos criar um programa em JavaScript para entender classes, métodos, atributos e herança!

Classe Animal:
- Crie uma classe chamada Animal.
- Adicione dois atributos: nome e idade.
- Adicione um método descrever() que exiba no console uma descrição do animal com seu nome e idade.

Classe Gato (Herda de Animal):
- Crie uma classe chamada Gato que herda da classe Animal.
- Adicione um atributo extra cor específico para gatos.
- Adicione um método miar() que exiba no console o som que um gato faz.

Criando Animais:
- Crie dois objetos da classe Animal: um chamado cachorro e outro gato, com idades distintas.
- Para o gato, também defina a cor.

Chamando os Métodos:
- Para cada animal, chame o método descrever() para ver a descrição no console.
- Para o gato, chame o método miar() para "ouvir" o som que ele faz (é também para ver o som no console).

Dica: Utilize console.log() para exibir as informações!

 Resposta:
```Javascript
// Criação de uma classe
class Animal {
    // Definição dos atributos
    constructor(nome, idade) {
        this.nome = nome
        this.idade = idade
    }
    // Criação do método "descrever" para explicitar a descrição do animal
    descrever() {
        console.log("Oie! Esse é o(a) " + this.nome + ", e ele(a) tem" + this.idade + " anos de idade!");
    }
  }
  
  // Criação da classe "Gato" que herda atributos da classe "Animal"
  class Gato extends Animal {
    // Definição dos atributos herdados e novos 
    constructor(nome, idade, cor) { 
        super (nome, idade)
        this.cor = cor
    }
  
    // Criação do método "descrever" para explicitar a descrição do animal
    descrever() {
      console.log("Oie! Este é o(a) " + this.nome + ", e ele(a) tem" + this.idade + " anos de idade e cor " + this.cor + "!");
    }
  
    // Criação de um método para o miado do gato
    miar() {
      console.log("Miawwwww");
    }
  }
  
  // Definição dos objetos (cachorro e gato)
  const cachorro = new Animal("Pretão", 7);
  const gato = new Gato("Chaninha", 11, "Rajadinha");
  
  // Retomada do método para impressão específica de cada animal
  cachorro.descrever();
  gato.descrever();
  gato.miar();
```

______

**9)** Vamos criar um programa em JavaScript para somar notas!

Classe SomadorDeNotas:
- Crie uma classe chamada SomadorDeNotas.
- Adicione um atributo total inicializado com 0 para armazenar a soma das notas.

Método adicionarNota:
- Adicione um método chamado adicionarNota(nota) na classe SomadorDeNotas.
- Este método deve receber um parâmetro nota e somá-lo ao atributo total.

Criando o Somador e Adicionando Notas:
- Crie um objeto da classe SomadorDeNotas, chamado somador.
- Utilize o método adicionarNota(nota) para adicionar algumas notas ao somador.

Chamando o Método para Ver o Total:
- Após adicionar todas as notas, chame um método verTotal() para exibir o total das notas adicionadas.

Dica: Utilize console.log() para exibir as informações!

Resposta:
```Javascript
//Cria a clase "SomadordeNotas"
class SomadordeNotas {

  // Definição dos atributos
  constructor() {
      this.total = 0 // O atributo se inicia no 0 
  }

  // Criação do método que recebe um valor da nota, que é adicionado do total após a adição
  adicionarNota(nota) {
      this.total += nota
  }

  // Criação do método que resulta no valor total
  verTotal() {
      console.log("Total de notas: " + this.total)
  }
}

// Definição do objeto SomadordeNotas
const somador = new SomadordeNotas()

// Atribuição do valor de novas notas
somador.adicionarNota(8.2)
somador.adicionarNota(9)
somador.adicionarNota(9.8)

// Resulta no valor total depois da adição de todas as notas
somador.verTotal()
```
______

**10)** Imagine que você está criando um programa em JavaScript para uma escola. Neste programa, existem diferentes tipos de funcionários, cada um com suas próprias características. Considere as seguintes classes:

Funcionário:
- atributo: Nome
- atributo: Idade
- atributo: Salário base
- método: calcularSalario() - Este método calcula o salário total do funcionário. Para cada tipo de funcionário, o cálculo será diferente.

Professor (herança de Funcionário):
- atributo: Disciplina
- atributo: Horas de aula por semana
- método: calcularSalario() - Para calcular o salário do professor, multiplicamos suas horas de aula pelo valor da hora/aula.

Agora, sua tarefa é escrever um código em JavaScript que crie as classes Funcionário e Professor, com suas características e métodos descritos acima. Depois de criar as classes, crie:
- Dois objetos do tipo Professor com informações fictícias.
- Para cada objeto, chame o método calcularSalario() e mostre o salário calculado no console.

Certifique-se de explicar cada parte do código utilizando comentários, explicando para que serve cada atributo e método, bem como a lógica por trás do cálculo de salário para o tipo de funcionário Professor.

// Criação da classe. Toda classe tem incluída por padrão um constructor, que pode ser vazio. Nesse caso, também irei configurá-lo manualmente:

 Resposta:
 ```Javascript
 // Criação da classe "Funcionario"
class Funcionario {
  // Definição dos atributos
  constructor(nome, idade, salarioBase) { 
    
    // Criação dos atributos
    this.nome = nome
    this.idade = idade
    this.salarioBase = salarioBase
    this.salario = this.calcularSalario() // Este atributo - em específico - retorna o cáulculo do próximo método 
  }

  // Método que retorna o valor base do salário incial
  calcularSalario() {
    return this.salarioBase

  }
}

// Criação da classe "Professor" que herda atributos da classe "Funcionario"
class Professor extends Funcionario {
  constructor(nome, idade, salarioBase, disciplina, horasdeAula) {
    super(nome, idade, salarioBase)
    this.disciplina = disciplina
    this.horasdeAula = horasdeAula
    this.valorAula = 6.0
    this.salario = this.calcularSalario()
  }

  //Método que retorna o valor do salário base e adicona o cálculo feito entre o valor da aula e a carga horária mensal do professor
  calcularSalario() {
     return super.calcularSalario() + (this.valorAula * this.horasdeAula)
  }
  
}

// Criação de dois objetos da classe Professor (professor e professora)
const professora = new Professor("Juliana", 32, 1500, "Artes", 120)
const professor = new Professor("Danilo", 45, 1500, "Educação Física", 176)

// Retomada do método para exibição do salário total do profissional
console.log(professora.calcularSalario())
console.log(professor.calcularSalario())
```
