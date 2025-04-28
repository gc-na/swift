<!--
Meta Description: # O Comando "return" em Swift: Funcionalidade e Uso ## Sinopse O comando `return` em Swift é utilizado para finalizar a execução de uma função e, opci...
Meta Keywords: return, função, swift, uma, para
-->

# O Comando "return" em Swift: Funcionalidade e Uso

## Sinopse
O comando `return` em Swift é utilizado para finalizar a execução de uma função e, opcionalmente, retornar um valor ao chamador.

## Documentação
O comando `return` tem um papel fundamental na programação em Swift, permitindo que funções enviem de volta valores para o local onde foram chamadas. Ao usar `return`, a execução da função é encerrada imediatamente, e o controle é passado de volta para o código que fez a chamada.

### Propósito
- Finalizar a execução de uma função.
- Retornar um valor a partir de funções que têm um tipo de retorno definido.

### Uso
O uso básico do `return` é simples. Dentro de uma função, você coloca a palavra-chave `return` seguida do valor que deseja retornar. Para funções que não retornam um valor, o uso de `return` é opcional, mas é uma boa prática incluí-lo para deixar o código mais claro.

#### Sintaxe Básica
```swift
func nomeDaFuncao() -> TipoRetorno {
    // lógica da função
    return valor
}
```

## Exemplos
### Exemplo 1: Função Simples com Retorno
```swift
func soma(a: Int, b: Int) -> Int {
    return a + b
}

let resultado = soma(a: 5, b: 3) // resultado será 8
```

### Exemplo 2: Função sem Retorno
```swift
func imprimeMensagem() {
    print("Olá, Mundo!")
    return // Opcional, mas pode ser utilizado para clareza
}

imprimeMensagem() // Saída: Olá, Mundo!
```

### Exemplo 3: Retorno Condicional
```swift
func verificaParImpar(numero: Int) -> String {
    if numero % 2 == 0 {
        return "Par"
    } else {
        return "Ímpar"
    }
}

let resultado = verificaParImpar(numero: 4) // resultado será "Par"
```

## Explicação
Embora o comando `return` seja bastante direto, existem algumas armadilhas comuns a serem observadas:

- **Falta de Tipo de Retorno**: Se uma função é definida para retornar um tipo específico e não há um `return` correspondente, o compilador gerará um erro.
  
- **Múltiplos `return`**: É possível ter múltiplas instruções `return` em uma única função, mas isso pode tornar o fluxo de execução confuso. É recomendável que a lógica seja clara e que o fluxo de controle seja fácil de seguir.

- **Uso em Closures**: Em closures, o comando `return` é usado da mesma forma, mas a sintaxe pode variar dependendo do contexto.

## Resumo em Uma Linha
O comando `return` em Swift finaliza a execução de uma função e permite o envio de valores de volta ao chamador.