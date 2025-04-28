<!--
Meta Description: # Entendendo o "do" em Swift: Comandos e Estruturas de Controle ## Sinopse O comando "do" em Swift é utilizado para criar blocos de código que tratam ...
Meta Keywords: que, erro, catch, erros, swift
-->

# Entendendo o "do" em Swift: Comandos e Estruturas de Controle

## Sinopse
O comando "do" em Swift é utilizado para criar blocos de código que tratam exceções ou realizam operações assíncronas, integrando-se completamente ao sistema de tratamento de erros da linguagem. Ele é essencial para garantir que erros sejam manejados de forma segura e eficiente.

## Documentação
O "do" é uma estrutura de controle em Swift que permite agrupar código e lidar com exceções que podem ocorrer durante a execução. O bloco "do" é frequentemente utilizado em conjunto com o tratamento de erros, permitindo que os desenvolvedores capturem e tratem falhas que podem ser lançadas durante a execução de funções que podem gerar erros.

### Propósito
O objetivo principal do "do" é proporcionar um mecanismo para executar código que pode falhar e, em seguida, capturar e lidar com esses erros usando a palavra-chave "catch".

### Uso
A estrutura básica do comando "do" é a seguinte:

```swift
do {
    // Código que pode lançar um erro
} catch {
    // Código para tratar o erro
}
```

Dentro do bloco "do", você pode chamar funções que estão marcadas como `throwing`, o que indica que elas podem lançar erros. Se um erro for lançado, a execução do código no bloco "do" será interrompida e o controle será passado para o bloco "catch".

## Exemplos

### Exemplo 1: Uso básico do "do-catch"
```swift
enum Erro: Error {
    case erroExemplo
}

func funcaoQueLancaErro() throws {
    throw Erro.erroExemplo
}

do {
    try funcaoQueLancaErro()
} catch Erro.erroExemplo {
    print("Um erro ocorreu: erroExemplo")
} catch {
    print("Um erro desconhecido ocorreu")
}
```

### Exemplo 2: Tratamento de erro com múltiplos casos
```swift
enum ErroDeRede: Error {
    case semConexao
    case tempoEsgotado
}

func requisicaoDeRede() throws {
    throw ErroDeRede.semConexao
}

do {
    try requisicaoDeRede()
} catch ErroDeRede.semConexao {
    print("Erro: Sem conexão com a rede.")
} catch ErroDeRede.tempoEsgotado {
    print("Erro: Tempo de espera esgotado.")
} catch {
    print("Erro desconhecido.")
}
```

## Explicação
Um erro comum ao usar "do" é esquecer de usar a palavra-chave "try" ao chamar funções que podem lançar erros. Isso resultará em um erro de compilação. Além disso, é importante lembrar que, ao capturar erros, você pode especificar múltiplos blocos "catch" para diferentes tipos de erros, permitindo um tratamento mais granular.

Outro ponto a ser observado é que o bloco "catch" pode capturar erros de forma genérica, utilizando apenas a palavra-chave "catch", o que é útil quando não se sabe exatamente qual erro pode ser lançado.

## Resumo em uma linha
O "do" em Swift permite agrupar códigos que podem lançar exceções e tratá-los de maneira segura com o uso da estrutura "do-catch".