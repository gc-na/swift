<!--
Meta Description: # Comando "break" no Swift: Interrompendo Fluxos de Controle ## Sinopse O comando `break` em Swift é utilizado para interromper a execução de loops e ...
Meta Keywords: break, switch, loop, swift, para
-->

# Comando "break" no Swift: Interrompendo Fluxos de Controle

## Sinopse
O comando `break` em Swift é utilizado para interromper a execução de loops e switch cases. Ele é uma ferramenta essencial para controlar o fluxo de execução em estruturas de repetição e condicionais.

## Documentação
O `break` é uma instrução que encerra a execução do loop mais interno ou do case atual em uma estrutura `switch`. Quando o `break` é encontrado, o controle do programa é transferido para a próxima instrução após o loop ou switch.

### Propósito
O principal propósito do `break` é permitir que os desenvolvedores interrompam loops ou cases de forma programática, oferecendo maior controle sobre o fluxo de execução.

### Uso
O `break` pode ser utilizado em:
- Loops (`for`, `while`, `repeat-while`)
- Estruturas `switch`

### Detalhes
- Quando usado em um loop, o `break` finaliza o loop imediatamente.
- Dentro de um `switch`, o `break` é automaticamente adicionado após cada case, mas pode ser explicitamente utilizado para interromper a execução quando necessário.

## Exemplos

### Exemplo 1: Usando `break` em um loop `for`
```swift
for i in 1...10 {
    if i == 5 {
        break
    }
    print(i)
}
// Saída: 1, 2, 3, 4
```

### Exemplo 2: Usando `break` em um loop `while`
```swift
var count = 0
while count < 10 {
    if count == 5 {
        break
    }
    print(count)
    count += 1
}
// Saída: 0, 1, 2, 3, 4
```

### Exemplo 3: Usando `break` em um `switch`
```swift
let number = 2
switch number {
case 1:
    print("Um")
case 2:
    print("Dois")
    break
case 3:
    print("Três")
default:
    print("Outro número")
}
// Saída: Dois
```

## Explicação
Um erro comum ao utilizar o `break` é esquecê-lo dentro de um `switch`, o que pode levar a comportamentos inesperados, especialmente se não houver um `break` entre os cases. Outro ponto a considerar é que o `break` só afeta o loop ou switch mais próximo, sendo que loops aninhados requerem o uso de múltiplos comandos `break` para interromper cada um deles.

## Resumo em Uma Linha
O comando `break` em Swift é utilizado para interromper loops e switch cases, controlando o fluxo da execução do programa.