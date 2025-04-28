<!--
Meta Description: # Operadores em Swift: Entenda como funcionam e como utilizá-los ## Sinopse Os operadores em Swift são símbolos que realizam operações em variáveis e ...
Meta Keywords: operadores, let, swift, como, que
-->

# Operadores em Swift: Entenda como funcionam e como utilizá-los

## Sinopse
Os operadores em Swift são símbolos que realizam operações em variáveis e valores. Eles desempenham um papel fundamental na manipulação de dados e na construção de lógica dentro de um programa.

## Documentação
Os operadores em Swift podem ser classificados em várias categorias, incluindo operadores aritméticos, operadores de comparação, operadores lógicos, operadores de atribuição, operadores de intervalo e operadores personalizados.

### Tipos de Operadores
1. **Operadores Aritméticos**: Realizam operações matemáticas básicas, como adição (+), subtração (-), multiplicação (*), divisão (/) e módulo (%).
2. **Operadores de Comparação**: Comparam valores e retornam um valor booleano (true ou false), como igual a (==), diferente de (!=), maior que (>), menor que (<), maior ou igual a (>=) e menor ou igual a (<=).
3. **Operadores Lógicos**: Usados para combinar expressões booleanas, como E lógico (&&), OU lógico (||) e NÃO lógico (!).
4. **Operadores de Atribuição**: Atribuem valores a variáveis, como o operador de atribuição simples (=) e operadores compostos (+=, -=, *=, etc.).
5. **Operadores de Intervalo**: Criam intervalos de valores, como o operador de intervalo fechado (a...b) e o operador de intervalo aberto (a..<b).

### Uso
Os operadores podem ser usados diretamente com variáveis e constantes. Por exemplo, para adicionar dois números inteiros, você pode usar o operador de adição (+):

```swift
let a = 5
let b = 10
let soma = a + b // soma é igual a 15
```

## Exemplos
### Operadores Aritméticos
```swift
let x = 10
let y = 3

let soma = x + y          // 13
let subtracao = x - y     // 7
let multiplicacao = x * y // 30
let divisao = x / y       // 3
let resto = x % y         // 1
```

### Operadores de Comparação
```swift
let num1 = 5
let num2 = 10

let igual = num1 == num2         // false
let diferente = num1 != num2      // true
let maior = num1 > num2           // false
let menor = num1 < num2           // true
```

### Operadores Lógicos
```swift
let cond1 = true
let cond2 = false

let resultadoE = cond1 && cond2   // false
let resultadoOU = cond1 || cond2   // true
let resultadoNAO = !cond1          // false
```

## Explicação
Um erro comum ao usar operadores é a precedência. A ordem em que os operadores são avaliados pode afetar o resultado final. Por exemplo, na expressão `3 + 4 * 2`, o operador de multiplicação (*) tem precedência sobre a adição (+), resultando em `3 + 8`, que é `11`, e não `14`.

Outro ponto a ser observado é que alguns operadores, como o operador de divisão, podem resultar em erros de execução se não forem tratados adequadamente. Dividir por zero, por exemplo, resultará em uma exceção.

## Resumo em Uma Linha
Os operadores em Swift permitem realizar operações em valores e variáveis, sendo fundamentais para a lógica e manipulação de dados em um programa.