<!--
Meta Description: # Comando "if" no Swift: Estruturas de Controle Condicional ## Sinopse O comando "if" em Swift é uma estrutura de controle condicional que permite exe...
Meta Keywords: else, swift, código, print, nota
-->

# Comando "if" no Swift: Estruturas de Controle Condicional

## Sinopse
O comando "if" em Swift é uma estrutura de controle condicional que permite executar um bloco de código com base na avaliação de uma expressão booleana. Ele é fundamental para implementar lógica condicional em aplicativos e scripts.

## Documentação
O comando "if" é usado para tomar decisões dentro do código, permitindo executar diferentes seções de código dependendo se uma condição é verdadeira ou falsa. A sua sintaxe básica é a seguinte:

```swift
if condição {
    // Código a ser executado se a condição for verdadeira
}
```

### Uso
O uso do comando "if" é simples e intuitivo. Você pode usá-lo para verificar qualquer expressão que retorne um valor booleano (true ou false). Além disso, o Swift permite encadear múltiplas condições usando "else if" e "else".

### Estrutura Completa
```swift
if condição1 {
    // Código se condição1 for verdadeira
} else if condição2 {
    // Código se condição2 for verdadeira
} else {
    // Código se nenhuma das condições anteriores for verdadeira
}
```

## Exemplos

### Exemplo Básico
```swift
let idade = 18

if idade >= 18 {
    print("Você é maior de idade.")
} else {
    print("Você é menor de idade.")
}
```

### Encadeamento de Condições
```swift
let nota = 85

if nota >= 90 {
    print("Nota A")
} else if nota >= 80 {
    print("Nota B")
} else if nota >= 70 {
    print("Nota C")
} else {
    print("Nota D ou F")
}
```

### Condições Múltiplas
```swift
let temperatura = 30

if temperatura > 25 {
    print("Está quente!")
} else if temperatura < 15 {
    print("Está frio!")
} else {
    print("Está agradável.")
}
```

## Explicação
Um dos erros comuns ao usar o comando "if" é esquecer de usar chaves `{}` ao definir blocos de código, especialmente quando um único comando é executado. Além disso, é importante lembrar que as condições são avaliadas na ordem em que são escritas; assim, a ordem das verificações pode afetar o resultado.

Outra armadilha é a comparação de tipos diferentes sem a devida conversão, o que pode levar a resultados inesperados. Sempre verifique se as variáveis sendo comparadas são do tipo apropriado.

## Resumo em Uma Linha
O comando "if" em Swift permite a execução condicional de código com base na avaliação de expressões booleanas, facilitando a implementação de lógica em aplicativos.