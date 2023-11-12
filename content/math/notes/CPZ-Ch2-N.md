+++
title = "Mathematical Logic Notes"
date = 2023-11-11T00:12:25-07:00
tags = ["math", "notes", "CPZ"]
+++

### 2.1 
A **statement** is a declarative sentence or assertion that can be either true or false and is denoted by P or Q.

The **truth value** of a statement is denoted by T or F.

An **open sentence** is a statement where the truth value depends on a variable within the sentence and is NOT considered a statement. 

A **truth table** is a table containing all possible truth values for some given statements based on their relationships with each other

### 2.2
The **negation** of a statement reverses its truth value and is denoted by either **not P** or **~P**.

### 2.3
The **disjunction** of two statements P and Q (denoted by ⋁ ) is the statement *P or Q*, meaning that the disjunction is true if EITHER P OR Q is true.

The **conjunction** of two statements P and Q (denoted by ⋀) is the statement *P and Q*, meaning that the conjunction is true if BOTH P AND Q are true.


### 2.4
The **implication** or **conditional** is the statement "If P, Then Q", that is true when Q is true when P is true. It will always be true if P is false. 

This can be expressed using 
- If P, then Q
- Q if P
- P implies Q
- P only if Q
- P is sufficient for Q
- Q is necessary for P

### 2.5
Two open sentences using an implication, P1(x)⇒P2(x), is a statement.

With P⇒Q, the **hypothesis** is P and the **conclusion** is Q.

### 2.6
The **converse** of a statement P⇒Q is Q⇒P

The **biconditional** of P and Q is denoted by P⇔Q and is equivalent to (P⇒Q)⋀(Q⇒P)

This can be stated as
- P is equivalent to Q 
- P if and only if Q

### 2.7
The symbols ⋁, ⋀, ⇒, ⇔ and ~ are called **logical connectives** because they can be connected to form complex statements.

A **compound statement** is a statement formed by one or more statements, called the **component statements**, using logical connectives.

If a statement is always true it is a **tautology**, and if it is always false it is a **contradiction**.
- eg. If S is a tautology, ~S if a contradiction.

### 2.8
**logical equivalence** (denoted by ⇔): pretty self explanatory, if the truth values for given "inputs" are the same they are logically the same.

### 2.9
Logical equivalence is:
- Commutative
    - P!Q⇔Q!P for ! = ⋁ or ⋀a
- Associative
    - P!(Q!R)⇔Q!(P!R) for ! = ⋁ or ⋀
- Distributive
    - P!(Q?R)⇔(P!Q)?(P!R) for ! = ⋁ or ⋀ and ? = ⋀ or ⋁, respectively
- "DeMorgan-ive"
    - ~(P⋁Q)⇔(~P)⋀(~Q)
    - ~(P⋀Q)⇔(~P)⋁(~Q)

### 2.10
**P if and only if Q**, also represented by **iff** informally, is an important phrase because it means `P is necessary and sufficient for Q`, meaning that `if P, then Q, and, if Q, then P`. This allows statements of dependence to be made. This differs from *if P then Q* because `if` is used when P is **sufficient** for Q and `iff` is used when P is **necessary** for Q. Being necessary also implies being sufficient
- When P is **sufficient** for Q, then Q is true when P is true, but Q can also be true when P is false.
- When P is **necessary** for Q, then Q is only true when P is true.

For an element x in a set S, the **characterization** of P(x) is P(x)⇔Q(x). When P(x)⇔Q(x) is true, that means it's true ∀x∈S.

### 2.11
The symbol ∀ is called the **universal quantifier** and means "for all".

The symbol ∃ is called the **existential quantifier** and means "for at least one" or "there exists"

