
# ☕ Lox – Interpretador Parcial


Disciplina **Compiladores** – Engenharia da Computação UFMA

Professor: Sérgio Costa

Desenvolvedores: Kleiton Linneker Barbosa Pinheiro; Isabel Silva de Araujo


## 🎯 Objetivo
Desenvolvimento de um interpretador para a linguagem **Lox**, seguindo o conteúdo do livro *Crafting Interpreters* (Robert Nystrom).  
Até esta etapa implementamos: o **Parser de Expressões da Linguagem**, responsável por analisar as expressões da linguagem **Lox**, transformando a sequência de tokens produzidos pelo scanner em estruturas da AST, de acordo com a gramática da linguagem. Ele é um parser recursivo descendente.

---

## 📘 Referência
**Livro:** *[Crafting Interpreters – Robert Nystrom](https://craftinginterpreters.com/)*  
**Capítulo:** 4 – *Scanning*  
**Capítulo:** 5 – *Representing Code*  
**Capítulo:** 6 – *Parsing Expressions*  
**Capítulo:** 7 – *Evaluating Expressions*  
**Progresso até:** Seção **7.4 – Hooking Up the Interpreter**

---

## 📂 Estrutura do Projeto

```text
src/
└── com/
    └── craftinginterpreters/
        ├── lox/
        │   ├── AstPrinter.java
        │   ├── Expr.java
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

---

## 🛠️ Tecnologias Utilizadas

- Linguagem: **Java 21**
- IDE: **IntelliJ IDEA 2025.2.3 (Ultimate Edition)**
- Git + GitHub
