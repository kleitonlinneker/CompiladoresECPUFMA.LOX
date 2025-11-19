
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
**Progresso até:** Seção **6.4 – Wiring up the Parser**

---

## 📂 Estrutura do Projeto

src/
└── com/
└── craftinginterpreters/
├── lox/
│ ├── Lox.java
│ ├── Token.java
│ ├── TokenType.java
│ ├── Scanner.java
│ ├── Parser.java
│ ├── Expr.java ← Gerado automaticamente
│ └── AstPrinter.java
└── tool/
└── GenerateAst.java



🧪 Testando o Parser

Você pode testar a geração da AST usando um código simples, como:

(1 + 2) * (3 - 4) == 7




## 🛠️ Tecnologias Utilizadas

- Linguagem: **Java 21**
- IDE: **IntelliJ IDEA 2025.2.3 (Ultimate Edition)**
- Git + GitHub
