<!--
Meta Description: # "super" em Swift: Entendendo a Palavra-Chave para Acesso a Superclasses ## Sinopse A palavra-chave `super` em Swift é utilizada para referenciar mét...
Meta Keywords: super, classe, que, métodos, uma
-->

# "super" em Swift: Entendendo a Palavra-Chave para Acesso a Superclasses

## Sinopse
A palavra-chave `super` em Swift é utilizada para referenciar métodos, propriedades e inicializadores de uma superclass. Essa funcionalidade é essencial para habilitar a herança e a reutilização de código, permitindo que classes derivadas acessem e modifiquem comportamentos de suas superclasses.

## Documentação
A palavra-chave `super` é um elemento fundamental na programação orientada a objetos em Swift. Ao criar uma classe que herda de outra, você pode usar `super` para chamar métodos e acessar propriedades da classe pai. O uso de `super` é crucial quando você deseja estender ou modificar o comportamento de uma classe base sem reescrever todo o código.

### Propósito
- Acessar métodos e propriedades de uma superclass.
- Facilitar a sobreposição de métodos e a execução de código da classe pai dentro de implementar métodos na classe filha.

### Uso
Para utilizar `super`, você deve estar dentro de uma classe que herda de outra. O uso básico é feito da seguinte forma:

```swift
class SuperClasse {
    func metodoExemplo() {
        print("Método da SuperClasse")
    }
}

class SubClasse: SuperClasse {
    override func metodoExemplo() {
        super.metodoExemplo() // Chama o método da SuperClasse
        print("Método da SubClasse")
    }
}
```

Neste exemplo, ao chamar `metodoExemplo` em uma instância de `SubClasse`, você verá tanto a mensagem da `SuperClasse` quanto da `SubClasse`.

## Exemplos
### Exemplo 1: Chamando Métodos da Superclasse
```swift
class Animal {
    func fazerSom() {
        print("Animal faz som")
    }
}

class Cachorro: Animal {
    override func fazerSom() {
        super.fazerSom() // Chama o método da classe Animal
        print("Cachorro late")
    }
}

let meuCachorro = Cachorro()
meuCachorro.fazerSom()
// Saída:
// Animal faz som
// Cachorro late
```

### Exemplo 2: Acessando Propriedades
```swift
class Veiculo {
    var tipo: String {
        return "Veículo genérico"
    }
}

class Carro: Veiculo {
    override var tipo: String {
        return super.tipo + " - Carro"
    }
}

let meuCarro = Carro()
print(meuCarro.tipo) // Saída: Veículo genérico - Carro
```

## Explicação
Um dos erros comuns ao usar `super` é tentar acessá-lo fora do contexto de uma classe que herda de outra. Além disso, é importante lembrar que `super` deve ser usado apenas com métodos e propriedades que foram marcados como `override` na classe filha. Ao não fazer isso, o compilador gerará um erro.

Outro ponto a considerar é que, ao utilizar `super` para chamar um inicializador, você deve garantir que o inicializador da superclass seja chamado antes de usar qualquer propriedade da classe filha, para evitar acessar propriedades não inicializadas.

## Resumo em Uma Linha
A palavra-chave `super` em Swift permite que subclasses acessem métodos e propriedades de suas superclasses, facilitando a herança e a reutilização de código.