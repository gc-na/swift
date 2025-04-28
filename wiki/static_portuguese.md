<!--
Meta Description: # Entendendo o "static" em Swift: Como e Quando Usar ## Sinopse O modificador `static` em Swift permite que você defina propriedades e métodos que per...
Meta Keywords: static, que, uma, swift, propriedades
-->

# Entendendo o "static" em Swift: Como e Quando Usar

## Sinopse
O modificador `static` em Swift permite que você defina propriedades e métodos que pertencem à classe ou estrutura em vez de a uma instância específica. Isso é fundamental para otimizar o uso de memória e organizar o código de maneira mais eficiente.

## Documentação
### Propósito
O `static` é utilizado para declarar membros (propriedades e métodos) que são compartilhados por todas as instâncias de uma classe ou estrutura. Isso significa que você pode acessar essas propriedades e métodos sem a necessidade de criar uma instância do tipo.

### Uso
A palavra-chave `static` pode ser aplicada em classes, estruturas e enumerações. Quando um membro é declarado como `static`, ele se torna acessível diretamente através do tipo, sem a necessidade de um objeto.

### Detalhes
- **Propriedades estáticas**: São armazenadas em um único local na memória, economizando espaço quando o mesmo valor é necessário em várias instâncias.
- **Métodos estáticos**: Permitem que você execute funções relacionadas ao tipo sem precisar instanciar a classe ou estrutura.
- **Enumeradores estáticos**: Também podem ter membros estáticos, permitindo agrupar funcionalidades relacionadas.

## Exemplos
### Exemplo 1: Propriedade Estática
```swift
struct Contador {
    static var totalContagens = 0

    static func incrementar() {
        totalContagens += 1
    }
}

Contador.incrementar()
print(Contador.totalContagens)  // Saída: 1
```

### Exemplo 2: Método Estático
```swift
class Calculadora {
    static func somar(a: Int, b: Int) -> Int {
        return a + b
    }
}

let resultado = Calculadora.somar(a: 5, b: 3)
print(resultado)  // Saída: 8
```

### Exemplo 3: Propriedade Estática em Enumeração
```swift
enum Direcao {
    static let norte = "Norte"
    static let sul = "Sul"
    
    static func descricao() -> String {
        return "As direções disponíveis são \(norte) e \(sul)."
    }
}

print(Direcao.descricao())  // Saída: As direções disponíveis são Norte e Sul.
```

## Explicação
Um dos erros mais comuns ao usar `static` é tentar acessar membros estáticos usando uma instância do tipo, o que resultará em um erro de compilação. Além disso, é importante lembrar que as propriedades `static` não podem ser modificadas em instâncias específicas, pois pertencem à classe ou estrutura como um todo. Outro ponto a ser destacado é que, ao usar `static` em enumerações, você pode criar uma organização clara dos valores e funcionalidades associadas a elas, mas deve-se ter cuidado para não sobrecarregar a enumeração com muitos membros estáticos.

## Resumo em Uma Linha
O modificador `static` em Swift permite definir propriedades e métodos que são compartilhados entre todas as instâncias de uma classe ou estrutura, otimizando o uso de memória e a organização do código.