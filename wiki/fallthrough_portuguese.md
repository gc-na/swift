<!--
Meta Description: # Fallthrough em Swift: Entenda Como Funciona ## Sinopse O comando `fallthrough` em Swift é utilizado em estruturas de controle `switch`, permitindo q...
Meta Keywords: fallthrough, caso, que, não, print
-->

# Fallthrough em Swift: Entenda Como Funciona

## Sinopse
O comando `fallthrough` em Swift é utilizado em estruturas de controle `switch`, permitindo que a execução continue em caso de correspondência de um caso, mesmo que não haja um `break` explícito. Essa funcionalidade é útil para compartilhar código entre diferentes casos.

## Documentação
O `fallthrough` é um recurso do Swift que permite que a execução de um bloco de código continue para o próximo caso em uma instrução `switch`. Diferentemente de outras linguagens onde a execução em `switch` é automática, em Swift, cada caso é encerrado após sua execução, a menos que o `fallthrough` seja especificado.

### Propósito
O principal propósito do `fallthrough` é permitir que múltiplos casos compartilhem um conjunto de instruções, o que pode resultar em um código mais limpo e organizado.

### Uso
Para usar `fallthrough`, você deve colocá-lo no final do bloco de código de um caso. Isso fará com que a execução continue no próximo caso, mesmo que não haja um `break`.

### Detalhes
- O `fallthrough` deve ser usado apenas em casos que não precisam de lógica adicional, pois ele simplesmente passa para o próximo caso.
- Não é possível usar `fallthrough` para saltar diretamente para um caso não adjacente.

## Exemplos

### Exemplo Básico
```swift
let numero = 2

switch numero {
case 1:
    print("Número é 1")
case 2:
    print("Número é 2")
    fallthrough
case 3:
    print("Número é 3")
default:
    print("Número não é 1, 2 ou 3")
}
```
**Saída:**
```
Número é 2
Número é 3
```

### Exemplo com Múltiplos Casos
```swift
let dia = 5

switch dia {
case 1:
    print("Domingo")
case 2:
    print("Segunda-feira")
    fallthrough
case 3:
    print("Terça-feira")
    fallthrough
case 4:
    print("Quarta-feira")
    fallthrough
case 5:
    print("Quinta-feira")
default:
    print("Fim da semana")
}
```
**Saída:**
```
Quinta-feira
```

## Explicação
### Armadilhas Comuns
- **Uso Indevido**: `fallthrough` não deve ser usado se houver lógica diferente em cada caso. Ele é adequado apenas quando a lógica é compartilhada.
- **Controle de Fluxo**: Lembre-se de que `fallthrough` não verifica a condição do próximo caso, ele simplesmente continua a execução. Isso pode causar comportamentos inesperados se não estiver claro o que cada caso está fazendo.
- **Cuidado com o Último Caso**: Se o último caso de um `switch` usar `fallthrough`, ele continuará a execução para o próximo caso, que pode não existir, resultando em um erro.

## Resumo em Uma Linha
O `fallthrough` em Swift permite que a execução continue para o próximo caso em um bloco `switch`, facilitando o compartilhamento de lógica entre casos.