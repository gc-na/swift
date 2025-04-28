<!--
Meta Description: # Enum em Swift: Entendendo as Enumerações na Linguagem ## Sinopse As `enum` (enumerações) em Swift são um tipo de dado que permite agrupar valores re...
Meta Keywords: enum, que, swift, valores, case
-->

# Enum em Swift: Entendendo as Enumerações na Linguagem

## Sinopse
As `enum` (enumerações) em Swift são um tipo de dado que permite agrupar valores relacionados, tornando o código mais legível e seguro. Elas são utilizadas para definir um conjunto de casos que podem ser utilizados em diferentes contextos.

## Documentação
As enumerações são uma das características mais poderosas do Swift, permitindo a criação de tipos que podem ter um número limitado de valores possíveis. Ao contrário de outras linguagens, as enums em Swift podem ter propriedades e métodos associados, tornando-as extremamente versáteis.

### Propósito
O principal objetivo das `enum` é representar um conjunto fixo de valores, como estados, opções ou categorias, e garantir que somente esses valores possam ser utilizados. Isso melhora a segurança do tipo e a legibilidade do código.

### Uso
Para definir uma enumeração em Swift, utiliza-se a palavra-chave `enum`, seguida pelo nome da enum e seus casos. Cada caso pode ser um valor simples ou pode ter valores associados.

### Detalhes
- As enums podem ter métodos e propriedades.
- Podem conformar a protocolos.
- É possível usar `switch` para verificar os casos de uma enum.
- É recomendável usar enums quando há um número limitado de estados ou opções.

## Exemplos

### Exemplo Básico de Enum

```swift
enum Direcao {
    case norte
    case sul
    case leste
    case oeste
}

let minhaDirecao = Direcao.norte
```

### Exemplo com Valores Associados

```swift
enum Bebida {
    case agua(volume: Int)
    case refrigerante(sabor: String, volume: Int)
}

let minhaBebida = Bebida.refrigerante(sabor: "Coca-Cola", volume: 350)
```

### Usando Switch com Enum

```swift
func descricaoBebida(bebida: Bebida) {
    switch bebida {
    case .agua(let volume):
        print("Água com \(volume)ml")
    case .refrigerante(let sabor, let volume):
        print("Refrigerante \(sabor) com \(volume)ml")
    }
}

descricaoBebida(bebida: minhaBebida)
```

## Explicação
Um dos principais erros que os desenvolvedores iniciantes cometem ao trabalhar com enums é não usar o `switch` corretamente. É importante lembrar que todos os casos devem ser cobertos ou um caso `default` deve ser utilizado. Além disso, não é possível instanciar uma enum diretamente como se fosse uma classe ou estrutura sem especificar um caso.

Outro ponto a se considerar é que, ao usar valores associados, os desenvolvedores devem ter cuidado com os tipos de dados que estão utilizando, garantindo que o tipo esperado seja passado.

## Resumo em Uma Linha
Enums em Swift são um poderoso recurso que permite agrupar valores relacionados de forma segura e legível, oferecendo funcionalidades adicionais como métodos e propriedades.