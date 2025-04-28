<!--
Meta Description: # Estrutura Condicional "else" em Swift: Entenda Como Funciona ## Sinopse O comando "else" em Swift é uma parte fundamental das estruturas condicionai...
Meta Keywords: else, que, uma, código, swift
-->

# Estrutura Condicional "else" em Swift: Entenda Como Funciona

## Sinopse
O comando "else" em Swift é uma parte fundamental das estruturas condicionais que permite a execução de um bloco de código alternativo quando uma condição especificada não é atendida.

## Documentação
A estrutura condicional "else" é utilizada em conjunto com a instrução "if" para criar decisões lógicas em um programa Swift. A sintaxe básica para utilizar o "else" é a seguinte:

```swift
if condição {
    // Código a ser executado se a condição for verdadeira
} else {
    // Código a ser executado se a condição for falsa
}
```

### Propósito
O principal objetivo do "else" é fornecer uma alternativa para o fluxo de execução do programa, permitindo que diferentes blocos de código sejam executados dependendo do resultado de uma condição.

### Uso
O "else" é utilizado sempre que desejamos lidar com situações em que a condição especificada não se verifica. Além disso, o "else" pode ser combinado com "if" e "else if" para criar estruturas de decisão mais complexas.

### Detalhes
- O bloco de código dentro do "else" é opcional, mas é necessário que o "if" seja seguido por um bloco de código ou uma instrução.
- O uso de chaves `{}` é recomendado para delimitar claramente o bloco de código, especialmente em estruturas mais longas.

## Exemplos

### Exemplo Simples
```swift
let numero = 10

if numero > 5 {
    print("O número é maior que 5.")
} else {
    print("O número é 5 ou menor.")
}
```
Saída:
```
O número é maior que 5.
```

### Exemplo com "else if"
```swift
let nota = 75

if nota >= 90 {
    print("Excelente")
} else if nota >= 70 {
    print("Bom")
} else {
    print("Precisa melhorar")
}
```
Saída:
```
Bom
```

## Explicação
Um dos erros comuns ao trabalhar com estruturas condicionais é a omissão das chaves `{}` em blocos de código que contêm mais de uma linha. Embora Swift permita omitir chaves para um único comando, isso pode levar a confusões e bugs, principalmente em códigos mais complexos.

Outro ponto importante é que as instruções "if", "else if" e "else" são avaliadas sequencialmente, e assim que uma condição verdadeira é encontrada, os blocos subsequentes não são executados. Portanto, a ordem das condições pode afetar o resultado final.

## Resumo em Uma Linha
O "else" em Swift é uma estrutura condicional que permite a execução de um bloco de código alternativo quando a condição do "if" não é atendida.