<!--
Meta Description: # Função `func` no Swift: Como Declarar e Usar Funções ## Sinopse A palavra-chave `func` em Swift é utilizada para declarar funções, permitindo que os...
Meta Keywords: função, func, swift, funções, que
-->

# Função `func` no Swift: Como Declarar e Usar Funções

## Sinopse
A palavra-chave `func` em Swift é utilizada para declarar funções, permitindo que os desenvolvedores encapsulem código em blocos reutilizáveis, melhorando a legibilidade e a organização do código.

## Documentação
A declaração de funções em Swift é feita através da palavra-chave `func`, seguida pelo nome da função, parâmetros entre parênteses e um tipo de retorno opcional. Funções são fundamentais para a programação modular, pois permitem que você execute tarefas específicas de forma isolada.

### Estrutura Básica da Função
```swift
func nomeDaFuncao(parametro1: Tipo1, parametro2: Tipo2) -> TipoRetorno {
    // Corpo da função
}
```

### Componentes
- **nomeDaFuncao**: Identificador que invoca a função.
- **parametro1, parametro2**: Argumentos que a função recebe, cada um com um tipo definido.
- **TipoRetorno**: Tipo de dado que a função irá retornar. Se não houver retorno, use `Void` ou omita o tipo.

### Exemplo de Declaração de Função
```swift
func somar(a: Int, b: Int) -> Int {
    return a + b
}
```

## Exemplos
### Exemplo 1: Função Simples
```swift
func saudacao(nome: String) -> String {
    return "Olá, \(nome)!"
}

let mensagem = saudacao(nome: "Maria") // "Olá, Maria!"
```

### Exemplo 2: Função Sem Retorno
```swift
func imprimirMensagem() {
    print("Esta é uma mensagem.")
}

imprimirMensagem() // "Esta é uma mensagem."
```

### Exemplo 3: Função com Parâmetros Opcionais
```swift
func calcularPreco(preco: Double, desconto: Double = 0) -> Double {
    return preco - desconto
}

let precoFinal = calcularPreco(preco: 100.0) // 100.0
let precoComDesconto = calcularPreco(preco: 100.0, desconto: 20.0) // 80.0
```

## Explicação
Ao utilizar `func`, é importante prestar atenção aos tipos de parâmetro e retorno. Um erro comum é não especificar corretamente o tipo de retorno, resultando em erros de compilação. Além disso, as funções podem ter parâmetros com valores padrão, o que pode simplificar chamadas de função quando alguns valores não precisam ser especificados.

Outro ponto a considerar é que a ordem dos parâmetros é significativa e deve ser cuidadosamente planejada para evitar confusões durante a chamada da função. Além disso, funções podem ser aninhadas e até passadas como argumentos para outras funções, aumentando a flexibilidade do código.

## Resumo em Uma Linha
A palavra-chave `func` em Swift é usada para declarar funções, permitindo a criação de blocos de código reutilizáveis e organizados.