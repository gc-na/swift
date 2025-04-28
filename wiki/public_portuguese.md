<!--
Meta Description: # Modificador "public" em Swift: Acesso e Visibilidade em Programação ## Sinopse O modificador `public` em Swift é utilizado para controlar a visibili...
Meta Keywords: public, que, swift, módulo, membro
-->

# Modificador "public" em Swift: Acesso e Visibilidade em Programação

## Sinopse
O modificador `public` em Swift é utilizado para controlar a visibilidade de classes, estruturas, enums, e suas propriedades e métodos, permitindo que sejam acessados fora do módulo onde foram definidos.

## Documentação
O modificador `public` é uma das três opções de controle de acesso em Swift, sendo as outras `internal` e `private`. Quando um membro é declarado como `public`, ele pode ser acessado de qualquer lugar, seja dentro do mesmo módulo ou em módulos que importam o módulo onde o membro foi definido.

### Propósito
- Permitir que classes, funções e variáveis sejam acessíveis fora do módulo, promovendo a reutilização de código e criando APIs públicas.

### Uso
Para declarar um elemento como público, basta precedê-lo com a palavra-chave `public`. Veja a estrutura básica:

```swift
public class MinhaClasse {
    public var minhaPropriedade: Int
    
    public init(propriedade: Int) {
        self.minhaPropriedade = propriedade
    }
    
    public func meuMetodo() {
        print("Método chamado!")
    }
}
```

### Detalhes
- O modificador `public` pode ser aplicado a classes, estruturas, enums, propriedades e métodos.
- Ao usar `public` em uma classe, todos os seus membros também devem ser visíveis, a menos que sejam especificados como `private` ou `fileprivate`.

## Exemplos
### Exemplo 1: Classe pública
```swift
public class Carro {
    public var modelo: String
    
    public init(modelo: String) {
        self.modelo = modelo
    }
    
    public func exibirModelo() {
        print("Modelo do carro: \(modelo)")
    }
}
```

### Exemplo 2: Estrutura pública
```swift
public struct Ponto {
    public var x: Double
    public var y: Double
    
    public init(x: Double, y: Double) {
        self.x = x
        self.y = y
    }
}
```

## Explicação
### Armadilhas Comuns
- **Uso Excessivo**: Declarar tudo como `public` pode causar problemas de encapsulamento. É importante avaliar se realmente é necessário expor um membro ao público.
- **Restrições de Módulo**: Um membro `public` só pode ser acessado em módulos que o importam. Se você tentar acessar um membro `public` de um módulo onde ele não foi importado, resultará em erro.
- **Combinação com Outros Modificadores**: O uso de `public` com outros modificadores pode levar a confusões. Por exemplo, um membro `public` em uma classe `private` não será acessível externamente, mesmo que o membro em si seja `public`.

## Resumo em Uma Linha
O modificador `public` em Swift permite que classes, métodos e propriedades sejam acessíveis fora do módulo em que foram definidos, facilitando a criação de APIs reutilizáveis.