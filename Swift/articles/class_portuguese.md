<!--
Meta Description: # Classe em Swift: Entendendo a Estrutura de Dados Fundamental ## Sinopse A classe em Swift é uma estrutura que permite criar tipos de dados personali...
Meta Keywords: tipo, classes, swift, classe, uma
-->

# Classe em Swift: Entendendo a Estrutura de Dados Fundamental

## Sinopse
A classe em Swift é uma estrutura que permite criar tipos de dados personalizados, encapsulando dados e comportamentos relacionados, e é fundamental para a programação orientada a objetos na linguagem Swift.

## Documentação
As classes em Swift são definidas usando a palavra-chave `class` e podem conter propriedades (variáveis) e métodos (funções) que operam sobre essas propriedades. Ao contrário das estruturas, as classes são tipos de referência, o que significa que quando uma instância de classe é atribuída a uma nova variável ou constante, ambas as referências apontam para o mesmo objeto.

### Propósito
O principal propósito das classes é organizar o código em componentes reutilizáveis e encapsulados, facilitando a manutenção e a escalabilidade de aplicações.

### Uso
Para definir uma classe, usamos a seguinte sintaxe:

```swift
class NomeDaClasse {
    // Propriedades
    var propriedade: Tipo

    // Inicializador
    init(propriedade: Tipo) {
        self.propriedade = propriedade
    }

    // Métodos
    func metodo() {
        // Lógica do método
    }
}
```

### Detalhes
- **Herança**: As classes podem herdar de outras classes, permitindo a reutilização de código.
- **Inicializadores**: Classes podem ter múltiplos inicializadores e o inicializador padrão é gerado automaticamente se não houver inicializadores personalizados.
- **Desinicializadores**: Usamos `deinit` para liberar os recursos antes que a instância da classe seja desalocada.

## Exemplos
### Exemplo Básico de Classe

```swift
class Carro {
    var modelo: String
    var ano: Int

    init(modelo: String, ano: Int) {
        self.modelo = modelo
        self.ano = ano
    }

    func descricao() -> String {
        return "Carro: \(modelo), Ano: \(ano)"
    }
}

let meuCarro = Carro(modelo: "Fusca", ano: 1970)
print(meuCarro.descricao())
```

### Herança de Classe

```swift
class Veiculo {
    var tipo: String

    init(tipo: String) {
        self.tipo = tipo
    }

    func detalhes() -> String {
        return "Tipo: \(tipo)"
    }
}

class Moto: Veiculo {
    var cilindrada: Int

    init(tipo: String, cilindrada: Int) {
        self.cilindrada = cilindrada
        super.init(tipo: tipo)
    }

    override func detalhes() -> String {
        return "\(super.detalhes()), Cilindrada: \(cilindrada)cc"
    }
}

let minhaMoto = Moto(tipo: "Esportiva", cilindrada: 600)
print(minhaMoto.detalhes())
```

## Explicação
Um erro comum ao trabalhar com classes em Swift é confundir tipos de valor (como estruturas) com tipos de referência (como classes). Lembre-se de que, ao passar uma classe como argumento, você está passando uma referência ao objeto, não uma cópia dele. Isso pode levar a efeitos colaterais indesejados se não for gerenciado adequadamente.

Outro ponto importante é o uso de inicializadores. Se não forem definidos de maneira adequada, pode ocorrer um erro de compilação. Além disso, as classes não podem ser definidas como `final` se você pretende que elas sejam herdadas.

## Resumo em Uma Frase
As classes em Swift são tipos de referência que permitem a criação de estruturas de dados personalizadas, encapsulando dados e comportamentos relacionados, fundamentais para a programação orientada a objetos.