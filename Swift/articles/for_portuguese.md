<!--
Meta Description: # O Comando "for" em Swift: Iteração Simplificada ## Sinopse O comando "for" em Swift é uma estrutura de controle fundamental que permite iterar sobre...
Meta Keywords: swift, para, loop, intervalo, uma
-->

# O Comando "for" em Swift: Iteração Simplificada

## Sinopse
O comando "for" em Swift é uma estrutura de controle fundamental que permite iterar sobre sequências como arrays, dicionários e intervalos, facilitando a execução de operações repetitivas de maneira eficiente.

## Documentação
O "for" em Swift é utilizado para percorrer coleções de dados e executar um bloco de código para cada item. Existem duas sintaxes principais para o uso do comando "for":

1. **For-in Loop**: Itera sobre os elementos de uma coleção (como arrays ou dicionários).
2. **For Loop com Intervalo**: Executa um bloco de código um número específico de vezes, utilizando intervalos.

### Sintaxe
```swift
// For-in Loop
for item in collection {
    // código a ser executado para cada item
}

// For Loop com Intervalo
for index in start...end {
    // código a ser executado para cada índice
}
```

### Componentes
- `item`: Variável que representa o elemento atual da coleção durante a iteração.
- `collection`: A sequência de dados que está sendo percorrida, como um array ou um dicionário.
- `start` e `end`: Limites do intervalo que determina quantas vezes o código será executado.

## Exemplos

### Exemplo 1: Usando For-in Loop
```swift
let frutas = ["Maçã", "Banana", "Laranja"]

for fruta in frutas {
    print("Eu gosto de \(fruta)")
}
```

### Exemplo 2: Usando For Loop com Intervalo
```swift
for index in 1...5 {
    print("Número \(index)")
}
```

### Exemplo 3: Iterando sobre um dicionário
```swift
let idade = ["Ana": 25, "Bruno": 30, "Carlos": 22]

for (nome, idade) in idade {
    print("\(nome) tem \(idade) anos")
}
```

## Explicação
Embora o uso do "for" em Swift seja bastante intuitivo, existem algumas armadilhas comuns a serem evitadas:

- **Intervalos Exclusivos**: O uso do operador `...` cria um intervalo inclusivo, enquanto o operador `..<` cria um intervalo exclusivo. É importante escolher o operador correto para o resultado desejado.
  
- **Modificação da Coleção**: Tentar modificar uma coleção enquanto a percorre pode resultar em comportamento inesperado ou erros de execução. Para evitar isso, é recomendável criar uma cópia da coleção se você precisar modificar os elementos.

- **Tipos de Dados**: Certifique-se de que os tipos de dados são compatíveis, especialmente ao iterar por dicionários, onde a ordem não é garantida.

## Resumo em Uma Linha
O comando "for" em Swift permite iterar de forma eficiente sobre coleções e intervalos, facilitando a execução de operações repetitivas.