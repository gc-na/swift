<!--
Meta Description: # Extensões em Swift: Como Ampliar Funcionalidades de Tipos ## Sinopse As extensões em Swift permitem que você adicione novas funcionalidades a tipos ...
Meta Keywords: extensões, que, swift, tipos, você
-->

# Extensões em Swift: Como Ampliar Funcionalidades de Tipos

## Sinopse
As extensões em Swift permitem que você adicione novas funcionalidades a tipos existentes, como classes, estruturas, enumerações e até mesmo tipos de dados nativos. Essa característica é fundamental para a modularização e organização do código, promovendo a reutilização e a legibilidade.

## Documentação
As extensões são uma ferramenta poderosa no Swift que possibilitam a ampliação de tipos sem a necessidade de criar subclasses ou modificar o código original. Com extensões, você pode adicionar:

- Métodos: Funções que podem ser chamadas em instâncias do tipo.
- Propriedades: Propriedades computadas que não armazenam valores.
- Inicializadores: Novos métodos de inicialização para instâncias do tipo.
- Conformidade a protocolos: Fazer um tipo conformar a um protocolo existente.

### Uso Básico
Para criar uma extensão, você utiliza a palavra-chave `extension` seguida do nome do tipo que deseja estender. A sintaxe básica é a seguinte:

```swift
extension NomeDoTipo {
    // Novas funcionalidades
}
```

### Detalhes
As extensões não podem adicionar propriedades armazenadas, mas podem adicionar propriedades computadas. Além disso, você pode usar extensões para adicionar inicializadores, mas não pode desinicializar um tipo. As extensões são uma maneira ideal de organizar o código, especialmente quando você deseja separar a implementação de funcionalidades em diferentes arquivos.

## Exemplos
### Exemplo 1: Adicionando um Método
```swift
extension Int {
    func isEven() -> Bool {
        return self % 2 == 0
    }
}

let number = 4
print(number.isEven()) // Saída: true
```

### Exemplo 2: Adicionando uma Propriedade Computada
```swift
extension String {
    var reversed: String {
        return String(self.reversed())
    }
}

let greeting = "Olá"
print(greeting.reversed) // Saída: alO
```

### Exemplo 3: Adicionando Conformidade a um Protocolo
```swift
protocol Descritivel {
    var descricao: String { get }
}

extension Int: Descritivel {
    var descricao: String {
        return "O número é \(self)"
    }
}

let numero = 10
print(numero.descricao) // Saída: O número é 10
```

## Explicação
Embora extensões sejam poderosas, é importante ter cuidado com a ambiguidade de métodos. Se um método com o mesmo nome já existir, pode ocorrer conflito. Além disso, extensões não podem ser usadas para modificar o comportamento de tipos de terceiros, como os da biblioteca padrão, a menos que você tenha controle sobre eles. Outro ponto a considerar é que as extensões são aplicadas em tempo de compilação, o que significa que não podem ser usadas para alterar a implementação de um tipo após ele ter sido definido.

## Resumo em Uma Linha
Extensões em Swift permitem adicionar novas funcionalidades a tipos existentes, promovendo a modularização e a reutilização do código.