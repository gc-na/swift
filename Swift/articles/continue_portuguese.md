<!--
Meta Description: # Comando "continue" em Swift: Controle de Fluxo em Laços ## Sinopse O comando `continue` em Swift é utilizado para interromper a iteração atual de um...
Meta Keywords: continue, swift, iteração, loop, não
-->

# Comando "continue" em Swift: Controle de Fluxo em Laços

## Sinopse
O comando `continue` em Swift é utilizado para interromper a iteração atual de um laço, passando imediatamente para a próxima iteração. Essa funcionalidade é especialmente útil em loops quando se deseja ignorar certas condições e continuar o processamento.

## Documentação
O `continue` é uma instrução de controle de fluxo que pode ser aplicada em loops como `for`, `while` e `repeat-while`. Quando o `continue` é encontrado, a execução do loop não para; em vez disso, ele salta para a próxima iteração do loop, ignorando qualquer código restante na iteração atual.

### Uso
A sintaxe básica do `continue` é simples. Ele é colocado dentro do bloco do loop e, quando uma condição específica é atendida, o `continue` é executado. O código após o `continue` na iteração atual não será executado.

#### Estrutura:
```swift
for item in collection {
    if condition {
        continue
    }
    // Código a ser executado se a condição não for atendida
}
```

## Exemplos

### Exemplo 1: Ignorar Números Pares
```swift
for number in 1...10 {
    if number % 2 == 0 {
        continue
    }
    print(number) // Apenas números ímpares serão impressos
}
```

### Exemplo 2: Ignorar Palavras Específicas
```swift
let palavras = ["Swift", "programação", "continue", "exemplo", "pular"]
for palavra in palavras {
    if palavra == "pular" {
        continue
    }
    print(palavra) // "pular" será ignorada
}
```

## Explicação
Um dos erros comuns ao usar o `continue` é não compreender onde ele se aplica dentro dos loops. O `continue` só afeta a iteração atual e não o loop inteiro. Além disso, é importante lembrar que, se o `continue` for colocado em loops aninhados, ele afetará apenas o loop mais interno.

Outra armadilha comum é a utilização de `continue` em laços que não têm um bloco de código a seguir, o que pode levar a confusões ou a um comportamento inesperado.

## Resumo em uma Linha
O comando `continue` em Swift permite que você ignore a iteração atual de um loop e avance para a próxima, facilitando o controle de fluxo em situações específicas.