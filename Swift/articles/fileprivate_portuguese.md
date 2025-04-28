<!--
Meta Description: # A Profundidade do Modificador "fileprivate" em Swift: Acessibilidade de Módulos ## Sinopse O modificador de acesso `fileprivate` em Swift é utilizad...
Meta Keywords: fileprivate, swift, acesso, arquivo, nome
-->

# A Profundidade do Modificador "fileprivate" em Swift: Acessibilidade de Módulos

## Sinopse
O modificador de acesso `fileprivate` em Swift é utilizado para restringir a visibilidade de entidades a um único arquivo, permitindo um controle mais granular sobre a acessibilidade de classes, structs, enums e funções.

## Documentação
O `fileprivate` é um dos cinco níveis de controle de acesso em Swift, que também incluem `open`, `public`, `internal` e `private`. Quando uma entidade é marcada como `fileprivate`, ela só pode ser acessada dentro do mesmo arquivo onde foi declarada. Isso é útil para encapsular a implementação de certos componentes sem expô-los a outros arquivos do projeto.

### Propósito
O uso do `fileprivate` é ideal em situações onde você deseja compartilhar informações entre diferentes partes de um mesmo arquivo, mas deseja evitar que essas partes sejam acessíveis de fora desse arquivo. Isso ajuda a manter uma arquitetura de código mais limpa e organizada.

### Uso
Para declarar uma entidade como `fileprivate`, basta utilizar a palavra-chave antes da definição da entidade. Aqui está a sintaxe básica:

```swift
fileprivate class MinhaClasse {
    // Implementação da classe
}
```

## Exemplos

### Exemplo 1: Classe `fileprivate`
```swift
fileprivate class Usuario {
    var nome: String
    
    init(nome: String) {
        self.nome = nome
    }
    
    fileprivate func exibirNome() {
        print("Nome: \(nome)")
    }
}

func testeUsuario() {
    let usuario = Usuario(nome: "João")
    usuario.exibirNome() // Acesso permitido
}
```

### Exemplo 2: Estruturas e Métodos
```swift
fileprivate struct Computador {
    var modelo: String
    
    fileprivate func mostrarModelo() {
        print("Modelo: \(modelo)")
    }
}

func testeComputador() {
    let computador = Computador(modelo: "MacBook Pro")
    computador.mostrarModelo() // Acesso permitido
}
```

## Explicação
É importante notar que o `fileprivate` pode ser confundido com o `private`, que limita o acesso apenas à própria extensão ou classe. A decisão de usar `fileprivate` deve ser feita com cuidado, pois uma exposição excessiva pode levar a um código menos modular e mais difícil de manter. Um erro comum é tentar acessar uma entidade `fileprivate` de outro arquivo, o que resultará em um erro de compilação.

### Dicas:
- Utilize `fileprivate` quando precisar compartilhar métodos ou propriedades entre várias extensões ou classes dentro do mesmo arquivo.
- Evite o uso excessivo de `fileprivate` se não houver necessidade, pois isso pode aumentar a complexidade do código.

## Resumo em Uma Linha
O modificador `fileprivate` em Swift restringe o acesso a entidades a um único arquivo, promovendo um controle de acesso mais rigoroso no código.