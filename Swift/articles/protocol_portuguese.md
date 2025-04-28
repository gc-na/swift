<!--
Meta Description: # Protocolos em Swift: Compreendendo a Base da Programação Orientada a Protocolos ## Sinopse Os protocolos em Swift são uma poderosa funcionalidade qu...
Meta Keywords: protocolos, swift, que, func, protocol
-->

# Protocolos em Swift: Compreendendo a Base da Programação Orientada a Protocolos

## Sinopse
Os protocolos em Swift são uma poderosa funcionalidade que permite definir um conjunto de métodos e propriedades que podem ser adotados por classes, estruturas e enums, promovendo a flexibilidade e a reutilização de código.

## Documentação
Os protocolos são fundamentais na programação orientada a protocolos em Swift. Eles servem como contratos que estabelecem quais métodos e propriedades uma classe ou estrutura deve implementar. Um protocolo pode incluir métodos, propriedades e outros requisitos, mas não fornece implementações. 

### Propósito
Os protocolos permitem que diferentes tipos adotem a mesma interface, facilitando a troca de implementações e a escrita de código que é genérico e reutilizável.

### Uso
Para definir um protocolo, utiliza-se a palavra-chave `protocol`, seguida pelo nome do protocolo e um bloco de requisitos. Por exemplo:

```swift
protocol NomeDoProtocolo {
    var propriedade: Tipo { get set }
    func metodo()
}
```

Uma classe ou estrutura pode adotar um protocolo usando a sintaxe `: NomeDoProtocolo` após o nome da classe ou estrutura:

```swift
struct Implementacao: NomeDoProtocolo {
    var propriedade: Tipo
    func metodo() {
        // implementação do método
    }
}
```

### Detalhes
Os protocolos podem ser adotados por qualquer tipo, incluindo classes, structs e enums. Além disso, os protocolos podem herdar de outros protocolos, permitindo a construção de hierarquias de protocolos. Swift também suporta protocolos com implementações de métodos padrão usando extensões, o que melhora ainda mais a reutilização de código.

## Exemplos
Aqui estão alguns exemplos básicos de como usar protocolos em Swift:

### Exemplo 1: Definindo e Implementando um Protocolo

```swift
protocol Desenhavel {
    func desenhar()
}

class Círculo: Desenhavel {
    func desenhar() {
        print("Desenhando um círculo")
    }
}

class Quadrado: Desenhavel {
    func desenhar() {
        print("Desenhando um quadrado")
    }
}

let formas: [Desenhavel] = [Círculo(), Quadrado()]
for forma in formas {
    forma.desenhar()
}
```

### Exemplo 2: Protocolos com Propriedades

```swift
protocol Identificável {
    var id: Int { get }
}

struct Usuario: Identificável {
    var id: Int
}

let usuario = Usuario(id: 1)
print("ID do usuário: \(usuario.id)")
```

### Exemplo 3: Herança de Protocolos

```swift
protocol Veiculo {
    func mover()
}

protocol Carro: Veiculo {
    func abrirPorta()
}

class Sedan: Carro {
    func mover() {
        print("O carro está se movendo")
    }

    func abrirPorta() {
        print("A porta do carro foi aberta")
    }
}
```

## Explicação
Um dos erros comuns ao usar protocolos é não implementar todos os requisitos definidos. Isso resultará em um erro de compilação. Outro ponto a ser observado é que protocolos não podem armazenar dados, somente definir requisitos. Além disso, uma classe pode adotar múltiplos protocolos, mas é importante garantir que não haja conflitos entre os métodos e propriedades exigidos.

## Resumo em Uma Linha
Os protocolos em Swift são contratos que definem requisitos que classes, structs e enums devem implementar, promovendo a flexibilidade e a reutilização de código.