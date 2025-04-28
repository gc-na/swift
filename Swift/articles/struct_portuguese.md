<!--
Meta Description: # Estruturas em Swift: Tudo o que Você Precisa Saber ## Sinopse As estruturas (structs) em Swift são tipos de dados que permitem agrupar dados e funci...
Meta Keywords: uma, que, são, structs, struct
-->

# Estruturas em Swift: Tudo o que Você Precisa Saber

## Sinopse
As estruturas (structs) em Swift são tipos de dados que permitem agrupar dados e funcionalidades em uma única entidade, sendo essenciais para a programação orientada a objetos e programação funcional.

## Documentação
As estruturas em Swift são um dos elementos fundamentais da linguagem, oferecendo uma maneira de encapsular dados e comportamentos relacionados. Ao contrário das classes, as structs são tipos de valor, o que significa que são copiadas quando atribuídas a uma nova variável ou constante, ou quando passadas para uma função.

### Propósito
O principal propósito das structs é organizar dados de maneira lógica e eficaz, permitindo que desenvolvedores criem modelos de dados claros e concisos.

### Uso
Para declarar uma struct, utilizamos a palavra-chave `struct`, seguida pelo nome da estrutura e um bloco de código que define suas propriedades e métodos. As structs podem ter propriedades, inicializadores e métodos, além de conformar-se a protocolos.

### Detalhes
- **Propriedades**: Podem ser variáveis (`var`) ou constantes (`let`).
- **Métodos**: São funções que pertencem à estrutura e podem manipular suas propriedades.
- **Inicializadores**: São usados para criar instâncias da estrutura.

## Exemplos

### Exemplo Básico de Estrutura

```swift
struct Pessoa {
    var nome: String
    var idade: Int

    func descrever() -> String {
        return "Nome: \(nome), Idade: \(idade)"
    }
}

let pessoa1 = Pessoa(nome: "João", idade: 30)
print(pessoa1.descrever())
```

### Estruturas com Inicializadores Personalizados

```swift
struct Retangulo {
    var largura: Double
    var altura: Double

    init(largura: Double, altura: Double) {
        self.largura = largura
        self.altura = altura
    }

    func area() -> Double {
        return largura * altura
    }
}

let retangulo = Retangulo(largura: 5.0, altura: 3.0)
print("Área do retângulo: \(retangulo.area())")
```

## Explicação
Um dos principais cuidados ao trabalhar com structs é entender que, como tipos de valor, as alterações em uma instância de uma struct não afetam outras instâncias. Isso pode levar a comportamentos inesperados se não for bem compreendido. Além disso, structs não suportam herança como as classes, mas podem conformar-se a protocolos, permitindo uma forma de reutilização de código.

Outro ponto importante é que as structs são copiados por valor. Quando você passa uma struct para uma função ou a atribui a uma nova variável, uma cópia da struct é criada. Isso pode ser vantajoso em termos de segurança, pois evita efeitos colaterais inesperados.

## Resumo em Uma Linha
As estruturas em Swift são tipos de valor que agrupam dados e comportamentos, oferecendo uma maneira eficiente e organizada de modelar informações.