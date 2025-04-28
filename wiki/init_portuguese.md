<!--
Meta Description: # Entendendo o "init" em Swift: Inicializadores em Swift ## Sinopse O "init" em Swift é um construtor que permite a criação e a inicialização de instâ...
Meta Keywords: swift, init, que, inicializador, self
-->

# Entendendo o "init" em Swift: Inicializadores em Swift

## Sinopse
O "init" em Swift é um construtor que permite a criação e a inicialização de instâncias de classes, estruturas e enums. É uma parte fundamental da programação orientada a objetos em Swift.

## Documentação
O inicializador "init" é um método especial que é chamado quando uma nova instância de uma classe ou estrutura é criada. Ele é responsável por configurar as propriedades da instância e executar qualquer configuração necessária antes que a instância esteja pronta para uso.

### Propósito
O objetivo principal do "init" é garantir que as instâncias de classes e estruturas sejam criadas em um estado válido e consistente.

### Uso
Para definir um inicializador em Swift, você usa a palavra-chave `init`. Um inicializador pode ter parâmetros para permitir que os valores sejam passados durante a criação da instância.

#### Sintaxe básica:
```swift
class NomeDaClasse {
    var propriedade: Tipo

    init(parametro: Tipo) {
        self.propriedade = parametro
    }
}
```

## Exemplos
### Exemplo 1: Inicializador padrão
```swift
class Carro {
    var modelo: String
    var ano: Int

    init(modelo: String, ano: Int) {
        self.modelo = modelo
        self.ano = ano
    }
}

let meuCarro = Carro(modelo: "Fusca", ano: 1970)
print(meuCarro.modelo) // Saída: Fusca
```

### Exemplo 2: Inicializador sem parâmetros
```swift
struct Pessoa {
    var nome: String
    var idade: Int

    init() {
        self.nome = "Desconhecido"
        self.idade = 0
    }
}

let pessoaDefault = Pessoa()
print(pessoaDefault.nome) // Saída: Desconhecido
```

### Exemplo 3: Inicializador com valores padrão
```swift
class Animal {
    var especie: String
    var idade: Int

    init(especie: String, idade: Int = 1) {
        self.especie = especie
        self.idade = idade
    }
}

let gato = Animal(especie: "Gato")
print(gato.idade) // Saída: 1
```

## Explicação
Um erro comum ao usar inicializadores em Swift é esquecer de chamar `self` para inicializar propriedades. Além disso, ao criar inicializadores em classes que herdam de outras classes, é importante garantir que os inicializadores da superclasse sejam chamados corretamente.

Outro ponto importante é que, se uma classe possui propriedades opcionais, você pode optar por não inicializá-las no inicializador. Porém, isso deve ser feito com cautela para evitar estados inválidos.

### Gotchas
- Inicializadores não têm um valor de retorno.
- Você não pode chamar métodos de instância antes que todas as propriedades tenham sido inicializadas.
- Classes com propriedades não opcionais devem ter todos os valores atribuídos no inicializador.

## Resumo em Uma Linha
O "init" em Swift é um inicializador que permite configurar e criar instâncias de classes e estruturas de forma segura e consistente.