
☕ Lox – Interpretador (Parser + Avaliação de Expressões)

Disciplina: Compiladores – Engenharia da Computação (UFMA)
Professor: Sérgio Costa

Desenvolvedores:

Kleiton Linneker Barbosa Pinheiro; Isabel Silva de Araujo


🎯 Objetivo do Projeto

Este projeto implementa um interpretador parcial da linguagem Lox, seguindo o livro Crafting Interpreters de Robert Nystrom.

O objetivo é construir passo a passo os componentes fundamentais de um interpretador:
✔️ Scanner (Analisador Léxico)
✔️ Parser (Analisador Sintático) – recursivo descendente
✔️ AST (Árvore Sintática Abstrata)
✔️ Interpretador de expressões (avaliação de literais, agrupamentos, unários e binários)

Até esta etapa, o sistema já é capaz de executar expressões matemáticas e lógicas, como:

1 + 2 * 3
"ab" + "cd"
!(false)
(1 + 2) * 3
---

## 📘 Referência
**Livro:** *[Crafting Interpreters – Robert Nystrom](https://craftinginterpreters.com/)*  
**Capítulo:** 4 – *Scanning*  
**Capítulo:** 5 – *Representing Code*  
**Capítulo:** 6 – *Parsing Expressions*  
**Progresso até:** Seção **6.4 – Wiring up the Parser**

---

## 📂 Estrutura do Projeto

```text
src/
└── com/
    └── craftinginterpreters/
        ├── lox/
        │   ├── AstPrinter.java
        │   ├── Expr.java
        │   ├── Interpreter.java
        │   ├── RuntimeError.java
        │   ├── Lox.java
        │   ├── Parser.java
        │   ├── Scanner.java
        │   ├── Token.java
        │   └── TokenType.java
        └── tool/
            └── GenerateAst.java
```

---


## 🧪 Testando o Parser


Para testar o parser do projeto, você pode usar a seguinte expressão simples:

Execute `Lox`:
```
(1 + 2) * (3 - 4) == 7
```

A saída esperada do `Lox` é:

```
(== (* (group (+ 1.0 2.0)) (group (- 3.0 4.0))) 7.0)

```

### 🧩 Como interpretar essa estrutura

O formato de impressão da AST segue o estilo usado no livro *Crafting Interpreters*, representando nós da árvore como expressões aninhadas:

- `(+ 1.0 2.0)` representa a soma.
- `(- 3.0 4.0)` representa a subtração.
- `group (...)` representa parênteses explícitos no código-fonte.
- `(* ... ...)` representa a multiplicação entre os dois grupos.
- `(== ... 7.0)` compara o resultado da multiplicação com o literal `7.0`.

🧪 Como Testar o Interpretador
No terminal:
java -cp src com.craftinginterpreters.lox.Lox

Exemplos de entrada e saída:
> 1+2
3

> 1+2*3
7

> (1+2)*3
9

> !false
true

> "ab" + "cd"
abcd

🧩 Como interpretar a AST (modo debug)

Quando usado com o AstPrinter, a árvore sintática é exibida em forma de expressões aninhadas:

(== (* (group (+ 1.0 2.0)) (group (- 3.0 4.0))) 7.0)


Significa:

(+ 1.0 2.0) → soma

(- 3.0 4.0) → subtração

group(...) → expressões entre parênteses

(* ... ...) → multiplicação

(== ... 7.0) → comparação final

---

## 🛠️ Tecnologias Utilizadas

- Linguagem: **Java 21**
- IDE: **IntelliJ IDEA 2025.2.3 (Ultimate Edition)**; **Visual Studio Code**
- Git + GitHub
- Linguagem: Java 21
- Terminal: PowerShell / Windows CMD
