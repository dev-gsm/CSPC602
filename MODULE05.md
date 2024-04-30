# Module 05 - Logic and Inferences

## Propositional Logic

Propositional logic, also known as sentential logic, is a fundamental component of artificial intelligence (AI) and logic-based systems. It deals with propositions, which are statements that are either true or false. Propositions are typically represented using variables such as PP, QQ, RR, etc.

Example - "It is raining," "The sky is blue," and "2 + 2 = 5" are all propositions.

## Logical Connectives

These are symbols used to combine propositions and form compound propositions. Common logical connectives include:

**Conjunction**: ∧ (AND)

| P | Q | P ∧ Q |
| --- | --- | --- |
| false | false | false |
| false | true | false |
| true | false | false |
| true | true | true |

**Disjunction**: ∨ (OR)

| P | Q | P ∨ Q |
| --- | --- | --- |
| false | false | false |
| false | true | true |
| true | false | true |
| true | true | true |

**Negation**: ¬ (NOT)

| P | ¬P |
| --- | --- |
| true | false |
| false | true |

**Implication**: → (IF P THEN Q (if then))

| P | Q | P → Q [ ¬ P∨Q] |
| --- | --- | --- |
| false | false | true |
| false | true | true |
| true | false | flase |
| true | true | true |

**Biconditional**: ↔ (P IF AND ONLY IF Q (iff)) [if both true or both false then true]

| P | Q | P ↔ Q |
| --- | --- | --- |
| false | false | true |
| false | true | false |
| true | false | false |
| true | true | true |

## Concepts of Propositional Logic

**Tautology -** A tautology is a compound proposition that is always true.

Example:

P∨¬P

- Let P represent "It is raining." The compound proposition P∨¬P means "It is raining or it is not raining," which is always true, regardless of the weather conditions. This is a tautology because it covers all possible cases: either it is raining or it is not.

**Contradiction -** A contradiction is a compound proposition that is always false.

Example:

P∧¬P

- Using the same proposition P as above, P∧¬P means "It is raining and it is not raining," which is impossible and always false. This is a contradiction because it is logically impossible for both P and ¬P to be true simultaneously.

**Contingency -** A contingency is a compound proposition that is neither a tautology nor a contradiction. Its truth value depends on the truth values of its constituent propositions.

Example:

P∨Q

- Let P represent "It is raining" and Q represent "It is sunny." The compound proposition P∨Q means "It is raining or it is sunny." Depending on the weather conditions, this proposition can be true or false. If it is raining, P is true, making the compound proposition true. If it is sunny and not raining, Q is true, making the compound proposition true as well. However, if it is neither raining nor sunny, the proposition is false.

## First Order Logic (Predicate Logic)

First-order logic, also known as predicate logic, extends propositional logic by introducing the concept of predicates and quantifiers, allowing for more expressive and precise representation of knowledge.

## Concepts of FOL

**Predicates -** Predicates are statements or properties that can be true or false for objects in a domain of discourse. Predicates are denoted by symbols and they can take one or more arguments representing the objects as arguments to which the predicate applies.

Example:

P(x) might represent the predicate "x is a prime number," where xx is a variable ranging over integers.

**Quantifiers -** Quantifiers are fundamental elements in first-order logic that allow us to make statements about entire sets of objects rather than individual objects. 

**Universal Quantifier (∀)**:

Denoted by ∀, the universal quantifier asserts that a statement holds for all elements in the domain of discourse. It is used to express statements that apply to every object in a given domain.

**Syntax -** ∀ x P(x), where P(x) is a predicate and x is a variable ranging over all objects in the domain.

**Example -** ∀ x (x>0) asserts that "for all x, x is greater than 0.”

**Existential Quantifier (∃)**:

Denoted by ∃, the existential quantifier asserts that a statement holds for at least one element in the domain of discourse. It is used to express statements that apply to some objects in a given domain, without specifying which ones.

**Syntax -** ∃ x P(x), where P(x) is a predicate and x is a variable ranging over all objects in the domain.

**Example -** ∃ y (y is even) asserts that "there exists a y that is even.”

## Soundness and Completeness

**Soundness**

1. **Definition -** Soundness refers to the property of a logical system where every provable statement is true in all interpretations. In other words, if a statement can be derived or proved using the inference rules of a logical system, then it must be logically valid and true in all situations.
2. **Implication -** A sound logical system ensures that the conclusions drawn from valid reasoning are always true. For example, if an argument is sound, it means that if the premises are true, then the conclusion must also be true.

**Completeness**

1. **Definition -** Completeness refers to the property of a logical system where every true statement can be proved or derived within that system. A complete logical system ensures that all true statements within a given domain can be established through valid inference rules.
2. **Implication -** If a logical system is complete, it means that every logically valid statement can be proven or derived using the rules of inference. This property ensures that no true statement within the system remains unproven or undetermined.

**Summary**

- **Soundness** ensures that the conclusions drawn from valid reasoning are always true.
- **Completeness** ensures that all true statements within a given domain can be proven or derived within the logical system.

## Forward and Backward Chaining

**Inference Engine**

An inference engine is a component of an artificial intelligence (AI) system or a logical system that processes information and applies logical rules to derive new knowledge or make decisions.

**Inference Methods**

Forward chaining and backward chaining are two inference methods used in automated reasoning and expert systems to derive conclusions from a set of facts and rules. Both methods are commonly employed in rule-based systems, such as expert systems, where knowledge is represented in the form of rules.

**Forward Chaining**

Forward chaining, also known as data-driven reasoning or bottom-up reasoning, is an inference method used in automated reasoning and expert systems to derive conclusions from a set of facts and rules. It starts with the available facts and uses inference rules to derive new conclusions until a goal is reached or no more new facts can be inferred.

Forward chaining is particularly useful in situations where the system needs to react to new information or events and make decisions based on the current state of knowledge. It is commonly employed in expert systems, diagnostic systems, decision support systems, and other AI applications where logical reasoning and inference are required.

**Backward Chaining**

Backward chaining, also known as goal-driven reasoning or top-down reasoning, is an inference method used in automated reasoning and expert systems to derive conclusions starting from a specific goal or conclusion and working backward through the inference rules to find the facts that support that goal. It is particularly useful when the system needs to determine the conditions required to achieve a specific goal or outcome.

Backward chaining is commonly used in expert systems, diagnostic systems, planning systems, and other AI applications where the system needs to determine the conditions required to achieve a specific goal or outcome. It is particularly effective for problem-solving tasks where the desired outcome is known, and the system needs to work backward to identify the necessary conditions or steps to reach that outcome.


## Credit
- Prepared By **Aaniketh** (6th Semester, CST, 2023-24)

