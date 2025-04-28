<!--
Meta Description: # var em Swift: Definição, Uso e Exemplos ## Sinopse A palavra-chave `var` no Swift é utilizada para declarar variáveis que podem ter seus valores alt...
Meta Keywords: var, swift, uma, tipo, que
-->

# var em Swift: Definição, Uso e Exemplos

## Sinopse
A palavra-chave `var` no Swift é utilizada para declarar variáveis que podem ter seus valores alterados ao longo do tempo, permitindo a manipulação flexível de dados em um programa.

## Documentação
No Swift, `var` é uma das principais maneiras de declarar variáveis. Ao contrário de `let`, que é utilizada para declarar constantes, `var` permite que o valor atribuído a uma variável possa ser modificado após sua inicialização.

### Propósito
O propósito de `var` é oferecer uma maneira de armazenar dados que podem mudar durante a execução de um programa. Isso é essencial para manipulações dinâmicas de dados, como contadores, estados de jogos, ou qualquer situação onde os dados precisam ser atualizados.

### Uso
Para declarar uma variável em Swift, você deve usar a seguinte sintaxe:

```swift
var nomeDaVariavel: Tipo = valorInicial
```

- `nomeDaVariavel`: O nome que você deseja dar à sua variável.
- `Tipo`: O tipo de dado da variável, como `Int`, `String`, `Double`, etc.
- `valorInicial`: O valor inicial que você deseja atribuir à variável.

Se o tipo da variável puder ser inferido pelo compilador, você pode omitir a anotação de tipo:

```swift
var idade = 30 // O tipo é inferido como Int
```

## Exemplos
### Exemplo 1: Declaração e Inicialização
```swift
var nome = "Maria"
print(nome) // Saída: Maria
```

### Exemplo 2: Modificação do Valor
```swift
var contagem = 1
contagem += 1
print(contagem) // Saída: 2
```

### Exemplo 3: Variáveis de Diferentes Tipos
```swift
var altura: Double = 1.75
var ativo: Bool = true
print("Altura: \(altura), Ativo: \(ativo)") // Saída: Altura: 1.75, Ativo: true
```

## Explicação
Embora `var` seja uma ferramenta poderosa, existem algumas armadilhas comuns a serem evitadas:

- **Tipo de Dados**: Ao usar `var`, é importante lembrar que o tipo de dado deve ser consistente. Mudar o tipo de uma variável após sua declaração causará um erro de compilação.
  
- **Escopo**: Variáveis declaradas com `var` têm escopo no bloco onde foram criadas. Se uma variável for declarada dentro de uma função, ela não estará acessível fora dessa função.

- **Imutabilidade**: Em alguns casos, pode ser tentador usar `var` onde `let` seria mais apropriado. Usar `let` para constantes quando você sabe que o valor não mudará pode ajudar a evitar bugs.

## Resumo em Uma Linha
A palavra-chave `var` no Swift é utilizada para declarar variáveis mutáveis, permitindo a alteração de seus valores durante a execução do programa.