# Logical representation: propositional logic and predicate logic

## Logical representation

**Logical representation** is a formal way to represent knowledge using symbols and rules in Artificial Intelligence (AI). It helps machines understand and reason about information.

- Provides a `structured way` way to represents facts
- Helps in `automate reasoning`(drawing conclusions)
- Used in expert systems, problem-solving, and decision making

## Logic

A language with concrete rules:

    No ambuity in representation (maybe other errors)
Allows ambuigious communication and processing

<br>
<br>
<br>

## Propositional Logic

**Definition:**\
&nbsp;&nbsp;&nbsp;&nbsp;**Propositional Logic(PL)**, also known as **Boolean Logic**, is the simplest form of logic where statements(propositional) are either **true(T)** or **false(F)**

**Key Elements:**

- **Propositional:** A declarative statement that either **true** or **false** but no both.
- **Logical Connectives:** Used to combine or modify **propositions**

**Logical Connectives and Their Meaning:**

| Symbol    | Word | Name | Priority |Meaning |
|---------- | - |----------|:-:| - |
|  ¬P or ~P | NOT | Negation      | 1 | **NOT P** (If P is true, ¬P is false)                                 |
|  P ∧ Q    | AND | Conjunction   | 2 | **P AND Q** (True only if both P and Q are true)                      |
|  P ∨ Q    | OR | Disjunction   | 3 | **P OR Q** (True if at least one is true)                             |
|  P → Q    | Implies | Implication   | 4 | **If P then Q** (False only if P is true and Q is false)              |
|  P ↔ Q    | If and only if | Biconditional | 5 | **P if and only if Q** (True when P and Q have the same truth value)  |

**Examples:**\
&emsp;1.\
&emsp;&emsp;Let:\
&emsp;&emsp;&emsp;P = "It is raining"\
&emsp;&emsp;&emsp;Q = "The ground is wet"\
&emsp;&emsp;Then:\
&emsp;&emsp;&emsp;**Implication:** P → Q = "If it is raining, then the ground is wet."\
&emsp;2. Truth Table for **P ∧ Q (AND opration)**

|P|Q|P ∧ Q|
|----------|----------|----------|
|T|T|T|
|T|F|F|
|F|T|F|
|F|T|F|

**Properties of Operators:**

- **Commutative:**
  - P ∧ Q = Q ∧ P
  - P ∨ Q = Q ∨ P
- **Associativity:**
  - (P ∧ Q) ∧ R = P ∧ (Q ∧ P)
  - (P ∨ Q) ∨ R = P ∨ (Q ∨ R)
- **Identity element:**
  - P ∧ True = P
  - P ∨ True = True
- **Distributive:**
  - P∧ (Q ∧ R) = (P ∧ Q) ∧ (P ∧ P)
  - P ∨ (Q ∨ R) = (P ∨ Q) ∨ (P ∨ P)
- **DE Morgan's Law:**
  - ¬ (P ∧ Q) = (¬P) ∧ (¬Q)
  - ¬ (P ∨ Q) = (¬P) ∨ (¬Q)
- **Double-negation elimination:**
  - ¬ (¬P) = P

<br>
<br>
<br>
<br>
<br>
<br>

# **Predicate Logic (First-Order Logic - *FOL*)**

**Definition:**\
&emsp;**Predicate Logic** extends **Propositional Logic** by allowing **_quantifiers_** and **_relations_** between objects

**Key Elements:**

1. **Predicate (P(x))**: Represents a property of objects.\
&emsp;Example:
    - "x is a student" → Student(x)
    - "x is greater than y" → Greater(x, y)
2. **Quantifiers:**

| Symbol&emsp;&emsp;&emsp;| Name | Meaning | Example | Interpretation |
|-|-|-|-|-|
| ∀x P(x) | **Universal Quantifier** | "For all x, P(x) is true"|∀x Student(x) → Smart(x) | "All students are smart." |
| ∃x P(x) | **Existential Quantifier** | "There exists at least one x such that P(x) is true" | ∃x Student(x) ∧ PlaysGuitar(x) | "There is at least one student who plays guitar." |
| ∄x P(x) | **Negated Existential Quantifier** | "There does not exist any x such that P(x) is true" | ∄x Human(x) ∧ Immortal(x) | "There is no human who is immortal." |
| ∀x ∃y P(x, y) | **Universal-Existential Quantifier** | "For every x, there exists at least one y such that P(x, y) is true" | ∀x ∃y Loves(x, y) | "Everyone loves someone." |
| ∃x ∀y P(x, y) | **Existential-Universal Quantifier** | "There exists at least one x such that for every y, P(x, y) is true" | ∃x ∀y Knows(x, y) | "There is someone who knows everyone." |

**Examples:**\
&emsp;1.\
&emsp;&emsp;Let:\
&emsp;&emsp;&emsp;Hates(x, y) means "x hates y"\
&emsp;&emsp;&emsp;Human(x) means "x is a human"\
&emsp;&emsp;Then:\
&emsp;&emsp;&emsp;1. **∀x Human(x) → Mortal(x)**\
&emsp;&emsp;&emsp;&emsp;&emsp; - "All humans are mortal."\
&emsp;&emsp;&emsp;2. **∃x Hates(x, Maria)**\
&emsp;&emsp;&emsp;&emsp;&emsp; - "There exists someone who loves Maria."\

<!-- predicate logic: -->
    <!-- Syntax, semantics, instance and its relationships -->

<!-- https://www.slideshare.net/slideshow/logic-in-predicate-and-propositional-logic/267172670#1 -->