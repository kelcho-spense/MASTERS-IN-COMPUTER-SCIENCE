# **Summarized Notes: Formal Methods lecture 2**

# Propositional Logic

#### **Introduction**
- **Formal Methods**: Mathematical techniques for specifying, developing, and verifying software/hardware systems.
  - Aim: Enhance reliability and correctness through rigorous reasoning frameworks.
  - Applications: Designing digital circuits, constructing, and verifying programs.

- **Logic in Formal Methods**:
  - Provides:
    - A precise language for expressing statements.
    - Systematic methods for analyzing truth and validity.
    - Foundation for formal reasoning in computer science.
  - Focus on:
    - **Propositional Logic**: Deals with true/false propositions.
    - **First-Order Logic**: Extends propositional logic by introducing variables, quantifiers, and predicates for more complex reasoning.

---

#### **Propositional Logic**
**1. Syntax**  
Defines rules for constructing **well-formed formulas** (WFFs) using:
- **Propositional Variables**: \( p, q, r \) represent propositions.
- **Logical Connectives**:
  - **Negation (¬)**: Negates a proposition, e.g., ¬p ("not p").
  - **Conjunction (\( \land \))**: Combines propositions, e.g., \( p \land q \) ("p and q").
  - **Disjunction (\( \lor \))**: Indicates alternation, e.g., \( p \lor q \) ("p or q").
  - **Implication (\( \to \))**: Logical relationship, e.g., \( p \to q \) ("if p, then q").
  - **Biconditional (\( \leftrightarrow \))**: Equivalence, e.g., \( p \leftrightarrow q \) ("p if and only if q").
- Examples:
  - Valid: \( (p \lor q) \to r \).
  - Invalid: \( p \lor q \to \).

**2. Semantics**  
Defines the meaning of WFFs by assigning truth values:
- **Truth Tables**: Systematically evaluate truth values based on all combinations of propositional variables.
  - True = 1, False = 0.

**Key Insights**:
- **Syntax**: Focuses on structure and grammatical correctness.
- **Semantics**: Assigns meaning/truth values to formulas using connectives and variables.

**3. Truth Tables**
- Visualize truth values of propositions.
- Example Connective Truth Tables:
  - **Negation**: \( p \) | \( ¬p \):  
    \( T \to F \), \( F \to T \).  
  - **Conjunction**: \( p \land q \) is true only if both \( p \) and \( q \) are true.  
  - **Disjunction**: \( p \lor q \) is true if either \( p \) or \( q \) is true.  

---
#### **Logical Connectives**
Logical connectives are used to build more complex statements from simpler ones, and truth values of these complex statements depend on their components. Let's dive deeper into the logical connectives and their truth tables.

---

#### **1. Negation (¬p)**
Negation is a unary operator (it applies to a single proposition). If \( p \) is a proposition, the negation \( \neg p \) is true if \( p \) is false, and false if \( p \) is true.

| \( p \) | \( \neg p \) |
|--------|-------------|
| T      | F           |
| F      | T           |

Example:
- If \( p \): "It is sunny," then \( \neg p \): "It is not sunny."

---

#### **2. Conjunction (\( p \land q \))**
Conjunction is a binary operator. The conjunction of \( p \) and \( q \) (denoted \( p \land q \)) is true **only if both \( p \) and \( q \) are true**. Otherwise, it is false.

| \( p \) | \( q \) | \( p \land q \) |
|--------|--------|----------------|
| T      | T      | T              |
| T      | F      | F              |
| F      | T      | F              |
| F      | F      | F              |

Example:
- \( p \): "It is sunny," \( q \): "It is warm."
  - \( p \land q \): "It is sunny and warm." This is true only when both conditions are true.

---

#### **3. Disjunction (\( p \lor q \))**
Disjunction is a binary operator. The disjunction of \( p \) and \( q \) (denoted \( p \lor q \)) is true if **either \( p \), \( q \), or both are true**. It is false only when both \( p \) and \( q \) are false.

| \( p \) | \( q \) | \( p \lor q \) |
|--------|--------|----------------|
| T      | T      | T              |
| T      | F      | T              |
| F      | T      | T              |
| F      | F      | F              |

Example:
- \( p \): "It is sunny," \( q \): "It is warm."
  - \( p \lor q \): "It is sunny or warm." This is true if at least one of the conditions is true.

---

#### **4. Implication (\( p \rightarrow q \))**
Implication is a conditional statement. The statement \( p \rightarrow q \) (read as "if \( p \), then \( q \)") is false **only when \( p \) is true and \( q \) is false**. In all other cases, it is true.

| \( p \) | \( q \) | \( p \rightarrow q \) |
|--------|--------|-----------------------|
| T      | T      | T                     |
| T      | F      | F                     |
| F      | T      | T                     |
| F      | F      | T                     |

Example:
- \( p \): "If it rains," \( q \): "The ground will be wet."
  - \( p \rightarrow q \): "If it rains, then the ground will be wet." This is false only if it rains and the ground is not wet.

---

### Summary of Connectives

| Operator       | Symbol  | Description                                          |
|----------------|---------|------------------------------------------------------|
| Negation       | \( \neg \) | Reverses the truth value of a proposition              |
| Conjunction    | \( \land \) | True only when both propositions are true            |
| Disjunction    | \( \lor \) | True when at least one of the propositions is true    |
| Implication    | \( \rightarrow \) | False only when the first proposition is true, and the second is false |

---

### Visualizing Truth Tables
Each connective has a corresponding truth table, which shows how the truth value of a complex proposition depends on the truth values of its components.

Propositional logic forms the foundation for reasoning in mathematics, computer science, and philosophy. These logical operators are used to construct more complex logical formulas and evaluate their truthfulness systematically.

Let's break this proof step by step and clearly explain the reasoning for each step of the natural deduction proof of the proposition \( (A \land B) \to (B \land A) \):

---

### **1. Assumption**
We start by assuming \( A \land B \). This is the antecedent of the implication \( (A \land B) \to (B \land A) \).

- \( A \land B \) (Assumption)

---

### **2. \(\land\)-Elimination**
Using the **\(\land\)-elimination rule**, we can extract the individual components of a conjunction. If \( A \land B \) is true, both \( A \) and \( B \) must also be true. Therefore:

- \( A \) (\(\land\)-elimination on step 1)
- \( B \) (\(\land\)-elimination on step 1)

---

### **3. \(\land\)-Introduction**
Using the **\(\land\)-introduction rule**, we can combine two separate propositions \( B \) and \( A \) into a single conjunction \( B \land A \). If \( B \) and \( A \) are both true, then \( B \land A \) is true.

- \( B \land A \) (\(\land\)-introduction using steps 2 and 3)

---

### **4. \(\to\)-Introduction**
Finally, we use the **\(\to\)-introduction rule**. This rule allows us to conclude that \( (A \land B) \to (B \land A) \) is true if, assuming \( A \land B \), we can derive \( B \land A \).

- \( (A \land B) \to (B \land A) \) (\(\to\)-introduction from steps 1-4)

---

### **Explanation of Rules Used**

1. **\(\land\)-Elimination Rule**: This rule states that if \( A \land B \) is true, then we can infer \( A \) is true and \( B \) is true individually.
2. **\(\land\)-Introduction Rule**: This rule states that if \( A \) is true and \( B \) is true, we can infer \( A \land B \) is true.
3. **\(\to\)-Introduction Rule**: This rule states that if, assuming \( P \), we can derive \( Q \), then \( P \to Q \) is true.

---

### **Proof Recap in Natural Deduction**
1. \( A \land B \) (Assumption)
2. \( A \) (\(\land\)-elimination on 1)
3. \( B \) (\(\land\)-elimination on 1)
4. \( B \land A \) (\(\land\)-introduction using 2 and 3)
5. \( (A \land B) \to (B \land A) \) (\(\to\)-introduction, 1–4)

This demonstrates that \( (A \land B) \to (B \land A) \) is a logically valid proposition!

#### **Resolution**
- **Definition**: 
  - A rule of inference used in theorem-proving for **propositional logic** and **first-order logic**.
  - Enables a refutation-complete proof technique.
- **Mechanism**:
  - Applies to two clauses containing complementary literals.
  - Example: From clauses \(\{p, q\}\) and \(\{\neg p, r\}\), derive \(\{q, r\}\).

---

#### **Applications of Propositional Logic**
1. **System Specifications**:
   - Converts system requirements from natural language into logical expressions for clarity and precision.
2. **Logical Puzzles**:
   - Solves puzzles like the "muddy children puzzle" or "knights and knaves."
3. **Boolean Searches**:
   - Search engines use logical operators like AND, OR, and NOT for filtering results.
4. **Circuit Design**:
   - Logical connectives in propositional logic map directly to **logic gates** in hardware design.

---

#### **Limitations of Propositional Logic**
1. **Limited Expressiveness**:
   - Cannot express statements involving quantifiers or relations.
   - Example: "All men are mortal" cannot be represented.
2. **Lack of Representation for Individuals/Objects**:
   - No support for variables or predicates to express statements about specific entities.

---

### First-Order Logic

#### **Transition to First-Order Logic**
- To overcome the limitations of propositional logic, **first-order logic** introduces:
  - Variables
  - Quantifiers (e.g., \(\forall\), \(\exists\))
  - Predicates
- This allows for more complex and expressive reasoning about objects and their relationships.

#### **1. Syntax**
First-Order Logic (FOL) extends propositional logic by introducing:
- **Variables**: Represent objects in the domain of discourse.
- **Quantifiers**:
  - **Universal Quantifier (\( \forall \))**: "For all," e.g., \( \forall x \, P(x) \) ("For all \( x \), \( P(x) \) is true").
  - **Existential Quantifier (\( \exists \))**: "There exists," e.g., \( \exists x \, P(x) \) ("There exists an \( x \) such that \( P(x) \) is true").
- **Predicates**: Express properties or relationships between objects, e.g., \( even(x) \) ("\( x \) is even").
- **Functions**: Map objects to other objects.
- **Constants**: Represent specific objects.

---

#### **2. Semantics**
- **Model**: Provides meaning to formulas by defining:
  - **Domain of Discourse**: A set of objects.
  - **Interpretation**: Assigns meanings to predicates, functions, and constants.
- **Example**:
  - Domain: Natural numbers.
  - Predicate: \( even(x) \) is true if \( x \) is even.
  - Formula \( \exists x \, even(x) \): True, as there exists an even natural number.

---

#### **3. Quantifiers**
- **Universal Quantifier (\( \forall \))**:
  - Represents "for all."
  - Example: \( \forall x \, P(x) \): \( P(x) \) is true for all \( x \) in the domain.
- **Existential Quantifier (\( \exists \))**:
  - Represents "there exists."
  - Example: \( \exists x \, P(x) \): There exists at least one \( x \) such that \( P(x) \) is true.

**Key Insight**:
- Quantifiers enable FOL to reason about collections of objects and express complex generalizations.

---

#### **4. Proof Systems**
Proof systems in FOL extend propositional logic systems to handle quantifiers and predicates:
- **Natural Deduction**: Used for step-by-step derivation of conclusions.
- **Sequent Calculus**: Formal proof system to manipulate logical formulas.
- **Other Proof Methods**:
  - **Axiom Systems**: Use schemas as templates for generating axioms.
  - **Herbrand's Theorem**: Relates FOL validity to the satisfiability of propositional formulas.
  - **Automated Theorem Proving**: Resolution-based techniques for computer-assisted proof generation.

---

#### **5. Applications of First-Order Logic**

#### **1. Knowledge Representation**
- **Role of FOL**:
  - First-Order Logic provides a structured framework for representing complex relationships, properties, and facts in a given domain.
  - Example: In a knowledge base for medicine, FOL can represent facts like "All patients with condition \( X \) must be given treatment \( Y \)" as:
    \[
    \forall x \, (Patient(x) \land HasCondition(x, X) \to Prescribe(x, Y))
    \]
- **Applications**:
  - **Semantic Web**: FOL forms the basis for ontology languages (e.g., OWL) used to represent relationships in web-based knowledge systems.
  - **AI Knowledge Graphs**: Captures and queries relationships in large datasets like Google Knowledge Graph.

---

#### **2. Automated Theorem Proving**
- **FOL in Proving Correctness**:
  - Automated theorem proving (ATP) uses FOL to prove or disprove logical statements automatically.
  - Example: Verifying a software algorithm satisfies a specification:
    \[
    \forall input \, (Valid(input) \to CorrectOutput(input))
    \]
- **Practical Use Cases**:
  - **Software Verification**:
    - Ensures programs behave correctly under all inputs.
    - Used in critical systems like aerospace or medical devices.
  - **Hardware Design Verification**:
    - Validates correctness of hardware circuits and designs, detecting design errors early in development.
  - **Mathematical Proofs**:
    - Proves conjectures and theorems by transforming them into logical formulas.

---

#### **3. Natural Language Processing (NLP)**
- **Role of FOL in NLP**:
  - Converts natural language sentences into formal logical expressions for easier processing by machines.
  - Example: The sentence "Every human is mortal" is represented as:
    \[
    \forall x \, (Human(x) \to Mortal(x))
    \]
- **Applications**:
  - **Question Answering Systems**:
    - Translates user queries into logical expressions, retrieves relevant data, and formulates answers.
  - **Semantic Analysis**:
    - FOL helps analyze meaning and relationships between words in sentences for better context understanding.
  - **Chatbots and Virtual Assistants**:
    - Encodes and interprets rules for dialogue understanding and reasoning about user inputs.

---

#### **4. Expert Systems**
- **Definition**:
  - Expert systems are AI systems designed to simulate the decision-making ability of a human expert.
  - FOL encodes rules and facts in the knowledge base to reason about complex problems.
- **How FOL is Used**:
  - Rules like "If a patient has a fever and cough, prescribe medicine X" are written as:
    \[
    \forall x \, (HasSymptom(x, Fever) \land HasSymptom(x, Cough) \to Prescribe(x, MedicineX))
    \]
- **Applications**:
  - **Medical Diagnosis**:
    - Expert systems like MYCIN use FOL to infer diagnoses and suggest treatments.
  - **Legal Decision-Making**:
    - Encodes legal rules to simulate legal reasoning for case-based decision support.
  - **Business Systems**:
    - Assists in decision-making for finance, customer service, or operations by reasoning over encoded business rules.

---

#### **5. Robotics and Planning**
- **Role of FOL**:
  - Models tasks and environments for robots to make decisions and plan actions.
  - Example: "If a robot is at location A and the path to B is clear, then move to B."
    \[
    At(Robot, A) \land ClearPath(A, B) \to MoveTo(Robot, B)
    \]
- **Applications**:
  - **Pathfinding and Navigation**:
    - Used in autonomous robots to reason about the best paths and actions.
  - **Human-Robot Interaction**:
    - Encodes and interprets logical instructions from humans for task execution.

---

#### **6. Database Querying**
- **Role of FOL**:
  - Forms the theoretical foundation for query languages like SQL, used to extract and manipulate data.
  - Queries like "Find all employees who work in department X" are expressed in FOL:
    \[
    \exists e \, (Employee(e) \land WorksIn(e, X))
    \]
- **Applications**:
  - Complex searches in relational and graph databases.
  - Used in enterprise-level applications for managing large data repositories.

---

#### **7. Multi-Agent Systems**
- **FOL in Multi-Agent Reasoning**:
  - FOL models the knowledge, goals, and actions of multiple agents.
  - Example: "If Agent A knows Agent B has completed Task X, then Agent A should start Task Y."
    \[
    Knows(A, Completed(B, X)) \to Start(A, Y)
    \]
- **Applications**:
  - **Game Theory**:
    - Models strategies and interactions between agents.
  - **Collaborative AI**:
    - Enables multiple AI agents to coordinate and reason about shared goals.

---

#### **8. Scientific Research**
- **Use in Formalizing Theories**:
  - Scientists use FOL to represent and reason about scientific hypotheses and relationships.
  - Example: Representing Newton's laws or molecular interactions in physics and chemistry.
- **Applications**:
  - Biology, physics, and chemistry simulations.
  - Representing and reasoning about scientific data and predictions.

---

#### **Key Takeaway**

- First-Order Logic is a cornerstone of AI and computational reasoning, enabling applications ranging from automated reasoning and knowledge representation to robotics and NLP. Its ability to model relationships, quantify over objects, and reason systematically makes it indispensable across domains.
---

#### **6. Limitations of First-Order Logic**

#### **1. Computational Complexity**
- **Reasoning Challenges**:
  - The process of reasoning with First-Order Logic (FOL) involves searching for valid proofs, which can become computationally **expensive** as the size of the knowledge base grows.
  - Many inference problems in FOL are classified as **semi-decidable**, meaning algorithms may not terminate for some inputs.
- **Factors Contributing to Complexity**:
  - **Large Domains of Discourse**:
    - When the domain of objects is large, reasoning involves examining a potentially enormous number of objects and their relationships.
  - **Complex Predicates and Quantifiers**:
    - Evaluating logical formulas with nested quantifiers (\( \forall \) and \( \exists \)) is computationally intensive.
  - **Non-Determinism**:
    - Automated theorem proving or model-checking requires exploring all possible interpretations of formulas, which may not converge efficiently.
- **Example**:
  - Verifying the truth of \( \forall x \, \exists y \, P(x, y) \) over a large dataset requires checking for every \( x \), whether there exists a corresponding \( y \) such that \( P(x, y) \) holds.

---

#### **2. Expressiveness vs. Decidability**
- **Trade-Off**:
  - FOL is highly expressive, allowing complex statements about objects, relationships, and properties.
  - However, this expressiveness introduces **undecidability**, meaning no general algorithm can determine the truth of all FOL statements.
- **Undecidability in FOL**:
  - For example, statements involving self-reference or infinite domains can lead to undecidable problems.
  - Gödel’s incompleteness theorem demonstrates that FOL systems capable of arithmetic cannot prove all true statements within their framework.
- **Decidability vs. Expressiveness**:
  - To make reasoning decidable, expressiveness is often restricted, as in:
    - **Propositional Logic**: Decidable but less expressive.
    - **Description Logic**: Decidable fragment of FOL, widely used in ontologies and semantic web applications.
- **Practical Implication**:
  - In AI, engineers must balance the need for expressive representations with computational feasibility. Too much expressiveness can make reasoning tasks intractable.

---

#### **3. Limited Handling of Non-Logical Reasoning**
- **Lack of Probabilistic Reasoning**:
  - FOL is deterministic and does not natively handle uncertainty or probabilistic relationships.
  - Example: "There is a 70% chance it will rain tomorrow" cannot be directly expressed in FOL.
- **Practical Need**:
  - Many AI applications (e.g., natural language understanding, robotics) require probabilistic or fuzzy logic extensions for dealing with uncertain or incomplete information.

---

#### **4. Incompleteness of Reasoning**
- **Dependence on Axiomatization**:
  - The effectiveness of FOL depends heavily on how the knowledge base is axiomatized.
  - Incomplete or incorrect axioms can lead to incorrect or incomplete reasoning.
- **Example**:
  - If the axioms fail to capture all relevant domain knowledge, the reasoning system may fail to derive valid conclusions.

---

#### **5. Inefficiency in Large-Scale Applications**
- **Scalability Issues**:
  - FOL reasoning does not scale well with large, distributed, or dynamic knowledge bases.
  - Example: In real-time systems or dynamic environments, constant updates to the knowledge base may render FOL reasoning inefficient.
- **Alternative Approaches**:
  - For practical applications, researchers often combine FOL with heuristic methods or less expressive but faster systems like rule-based engines.

---

#### **6. Limited Time Representation**
- **Static Nature of FOL**:
  - FOL does not inherently support temporal reasoning (reasoning about time or dynamic systems).
  - Example: Representing "John was at the library yesterday but is at home now" requires extensions like temporal logic.

---

### **Key Takeaways**
- **FOL's Power and Challenges**:
  - While FOL is highly expressive and versatile, its computational complexity and undecidability issues pose significant challenges in large-scale or real-time applications.
- **Practical Adjustments**:
  - To mitigate these limitations, engineers often:
    - Restrict the domain (e.g., using decidable fragments like Description Logic).
    - Combine FOL with probabilistic models (e.g., Bayesian networks) or temporal logics.
    - Use heuristic or approximate reasoning for large-scale systems.

# **lecture 3: Program Semantics and Specification**

**Introduction to Program Semantics and Specification:**
- **Program semantics**: This is about giving a precise meaning to programs, telling us what each part of the program does.
- **Program specification**: This describes the desired behavior of a program clearly and unambiguously, allowing us to set expectations for what the program should do.
  
These concepts are crucial in **formal methods**, which use mathematical techniques to design, develop, and verify software and hardware. Formal methods help ensure the **reliability** and **correctness** of systems, particularly in safety-critical environments like **aviation**, **medical devices**, and **nuclear plants**.

By applying formal methods, we can eliminate **errors** and **inconsistencies** in the design process and **automate program analysis**.

---

### **Key Roles of Program Semantics and Specification:**
- **Understand program behavior**: Semantics helps us model how a program behaves.
  - Example: Understanding how a loop in a program will iterate based on conditions.
  
- **Specify behavior**: A program’s specification describes exactly what the program should do, ensuring that it behaves as expected.
  - Example: Specifying that a function should return a positive integer only.
  
- **Verify correctness**: By combining both, we can prove that the program follows its specification.
  - Example: Verifying that a sorting algorithm actually sorts the list as specified.

- **Reason about program properties**: It helps us understand important characteristics like termination (will it finish running?) or security (is it safe from attacks?).
  - Example: Verifying that a program terminates and does not run indefinitely.

---

### **Operational Semantics:**
**Operational semantics** explains how a program executes by describing its **step-by-step execution**. It's like providing a detailed instruction manual for running a program.

- **Small-step semantics**: This method breaks down the program into small steps, detailing how each instruction affects the state of the program at each point in time.
  - **Example**: In a simple program where a variable `x` is incremented, small-step semantics would show how `x` changes value at each step.

- **Big-step semantics**: This method focuses on the overall result of the program. It describes the end result after executing all instructions.
  - **Example**: If a program adds two numbers, big-step semantics would just tell you the final result without showing the individual steps.

---

### **Abstract Machines:**
An **abstract machine** is a hypothetical computer that helps define operational semantics. It shows how a program is executed by explaining how its instructions are carried out and how the program's state is updated.

- **SECD machine**: A classic example of an abstract machine developed to interpret the **lambda calculus**. It uses four components:
  1. **S (Stack)**: Stores partial results of calculations.
  2. **E (Environment)**: Stores variable bindings (i.e., the values of variables).
  3. **C (Control)**: Stores instructions to be executed.
  4. **D (Dump)**: Stores machine states for function calls.
  
  This machine helps explain how the state of a program changes when instructions are executed, providing a clear picture of program behavior.

- **Example**: Consider an abstract machine for a simple language with basic arithmetic operations like addition and subtraction. Here are some simple instructions:
  - **PUSH**: Pushes a number onto the stack.
  - **ADD**: Pops two numbers from the stack, adds them, and pushes the result back.
  - **SUB**: Pops two numbers from the stack, subtracts the second from the first, and pushes the result.
  - **PRINT**: Prints the value at the top of the stack.

---

### **Example in the Abstract Machine:**
Let’s consider a simple example using the abstract machine that supports basic arithmetic:

1. **PUSH 3**: Pushes the number `3` onto the stack.
2. **PUSH 5**: Pushes the number `5` onto the stack.
3. **ADD**: Pops `3` and `5` from the stack, adds them, and pushes the result `8` back onto the stack.
4. **PRINT**: Prints the value at the top of the stack, which is `8`.

The abstract machine keeps track of the state of the program at each step, helping to describe how the program’s state evolves as it runs.

---

**Summary**:
- **Program Semantics** helps us understand how a program behaves by giving precise meanings to its instructions.
- **Program Specification** defines what the program is supposed to do in a clear way, which is essential for verifying correctness.
- **Operational Semantics** is the technique used to describe a program’s behavior, either step-by-step (small-step) or overall result (big-step).
- **Abstract Machines** provide a hypothetical framework to explain how programs execute and how their states change.

This knowledge is crucial for designing reliable and error-free systems, especially in safety-critical applications.

### **Summary of Operational Semantics and Formal Methods**

**1. Introduction to Operational Semantics:**
Operational semantics defines the meaning of a program by explaining how it executes on an **abstract machine**. This method focuses on how the program's state changes step by step as instructions are executed.

#### Key Constructs in a Simple Language:
- **Arithmetic expressions**: Numerals (e.g., `5`), variables (e.g., `x`), addition (`e1 + e2`), and subtraction (`e1 - e2`).
- **Boolean expressions**: Constants `true` and `false`, equality (`e1 = e2`), less than (`e1 < e2`), and conjunction (`b1 and b2`).
- **Commands**: `skip` (does nothing), sequencing (`c1 ; c2`), assignment (`x := e`), conditional (`if b then c1 else c2`), and loop (`while b do c`).

These constructs are defined by inference rules, specifying how each construct is executed and how the state changes as a result.

---

**2. Examples of Operational Semantics Rules:**

- **Assignment**: 
  - **Rule**: `<x := e, σ> → σ[x v]` where `<e, σ> → v`
  - **Explanation**: To execute `x := e`, first evaluate `e` to obtain `v` in state `σ`, and then update the state by assigning `x` to `v`.
  - **Example**: If `x := 5` and `σ = {x: 3}`, then after execution, `σ = {x: 5}`.

- **Conditional**:
  - **Rule**: `<if true then c1 else c2, σ> → <c1, σ>`  
    `<if false then c1 else c2, σ> → <c2, σ>`
  - **Explanation**: If the condition is `true`, execute `c1`, otherwise execute `c2`.
  - **Example**: If `b = true`, then `<if true then x := 5 else y := 10, σ> → <x := 5, σ>`. Otherwise, execute the `else` part.

- **Loop**:
  - **Rule**: `<while b do c, σ> → <if b then (c ; while b do c) else skip, σ>`
  - **Explanation**: To execute a loop, if `b` is true, execute `c` and repeat the loop. If `b` is false, exit the loop by executing `skip`.
  - **Example**: If `b = true`, keep executing `c` in the loop; if `b = false`, exit the loop.

---

**3. Operational Semantics for Expressions:**

- **Arithmetic Expressions**:
  - **Numerals**: `<n, σ> → n`  
    Example: `<3, σ> → 3`.
  - **Variables**: `<x, σ> → σ(x)`  
    Example: If `σ = {x: 4}`, then `<x, σ> → 4`.
  - **Addition**: `<e1 + e2, σ> → n1 + n2` where `<e1, σ> → n1` and `<e2, σ> → n2`  
    Example: If `<3, σ> → 3` and `<2, σ> → 2`, then `<3 + 2, σ> → 5`.
  - **Subtraction**: `<e1 - e2, σ> → n1 - n2` where `<e1, σ> → n1` and `<e2, σ> → n2`  
    Example: If `<5, σ> → 5` and `<2, σ> → 2`, then `<5 - 2, σ> → 3`.

- **Boolean Expressions**:
  - **True/False**: `<true, σ> → true`, `<false, σ> → false`
  - **Equality**:  
    `<e1 = e2, σ> → true` if `<e1, σ> → v1` and `<e2, σ> → v2` and `v1 = v2`  
    `<e1 = e2, σ> → false` if `<e1, σ> → v1` and `<e2, σ> → v2` and `v1 ≠ v2`
    - Example: If `<3, σ> → 3` and `<3, σ> → 3`, then `<3 = 3, σ> → true`. If `<3, σ> → 3` and `<4, σ> → 4`, then `<3 = 4, σ> → false`.

---

**4. Denotational Semantics:**
Denotational semantics describes the meaning of a program by mapping it to a mathematical object like a function or a set. It focuses on the overall effect of the program, rather than step-by-step execution.

- **Examples of Denotational Mappings**:
  - **Arithmetic Expressions**:
    - `n = n`
    - `x σ = σ(x)`
    - `e1 + e2 σ = e1 σ + e2 σ`
  - **Boolean Expressions**:
    - `true σ = true`
    - `false σ = false`
    - `e1 = e2 σ = true` if `e1 σ = e2 σ`
    - `e1 = e2 σ = false` if `e1 σ ≠ e2 σ`

---

**5. Axiomatic Semantics:**
Axiomatic semantics defines the meaning of a program by specifying its effect on assertions about the program state, using logical formulas. **Hoare Logic** is a well-known example.

- **Assignment**:  
  `{P[e/x]} x := e {P}`  
  This rule states that if the assertion `P[e/x]` holds before the assignment, then `P` holds after the assignment.
  - Example: If `P` is the assertion `x > 0` and `e = 5`, after `x := 5`, we can say `x > 0`.

- **Conditional**:  
  `{P and b} c1 {Q} {P and not b} c2 {Q}`  
  This rule means that if `P and b` holds before executing `c1`, and `P and not b` holds before executing `c2`, then the assertion `P` holds after either branch.
  - Example: If `x > 0`, then depending on the value of `b`, execute either `c1` or `c2`.

- **Loop**:  
  `{P and b} c {P}`  
  This rule ensures that if the assertion `P` holds before executing `c`, it holds again after each iteration of the loop, and `P and not b` holds when the loop ends.
  - Example: If `P` is `x < 10` and `b` is `x < 10`, the loop will keep iterating until `x` becomes 10 or greater.

---

#### Example of Full Program: Let’s combine these rules in an example program:

Let’s combine these rules in an example program:

```plaintext
x := 5;
y := 10;
if x < y then x := x + 1 else y := y + 1;
while x < y do x := x + 1;
```

**Step-by-step Evaluation**:
1. `<x := 5, σ> → σ[x 5]` → `{x: 5, y: 10}`
2. `<y := 10, σ> → σ[y 10]` → `{x: 5, y: 10}`
3. `<if x < y then x := x + 1 else y := y + 1, σ>` → Evaluate `x < y` → true, so we execute `x := x + 1`.
   - `<x := x + 1, σ> → σ[x 6]` → `{x: 6, y: 10}`
4. `<while x < y do x := x + 1, σ>` → Since `x < y` (6 < 10), execute `x := x + 1`:
   - `<x := x + 1, σ> → σ[x 7]` → `{x: 7, y: 10}`
5. Repeat the loop, `x` becomes 8, 9, and finally 10.
6. Once `x = 10`, `x < y` is false, so the loop exits.

**Final State**: `{x: 10, y: 10}`.

### **Conclusion**:
- **Operational semantics** defines how a program is executed step by step.
- **Denotational semantics** maps the program to a mathematical object to describe its overall effect.
- **Axiomatic semantics** focuses on logical assertions about the state before and after commands are executed.

These semantics provide different ways to understand and reason about the behavior of programs, helping ensure correctness and reliability in software and hardware systems.

### **Summary of Relationships Between Semantic Approaches and Program Specification Techniques**

---

### **1. Relationships Between Semantic Approaches:**

- **Operational Semantics vs. Denotational Semantics**:
  - **Complementary Approaches**: Operational semantics provides a **concrete and intuitive** understanding of how a program executes, focusing on **step-by-step** execution and changes in state. Denotational semantics, on the other hand, offers a **more abstract, mathematical** approach, focusing on the overall effect of the program.
    - **Example**: 
      - In operational semantics, we might focus on the sequence of steps to compute the result of an arithmetic expression like `3 + 4`.
      - In denotational semantics, we would focus on mapping the entire expression `3 + 4` to its resulting value `7` using a mathematical function.

- **Equivalence of Operational and Denotational Semantics**:
  - In many cases, the two approaches are **equivalent**, meaning they describe the **same meaning** of a program but in different ways. This proves that different formal techniques can describe the same program behavior.
  - **Full Abstraction**: A denotational semantics is considered **fully abstract** with respect to operational semantics if two programs are considered equivalent in denotational semantics **if and only if** they are **observationally equivalent** in operational semantics. This ensures that the denotational semantics faithfully represents all observable behaviors of the program.
    - **Example**: Two programs that produce the same outputs under all possible inputs should be considered equivalent in both semantic approaches.

- **Axiomatic Semantics and Operational Semantics**:
  - Axiomatic semantics, which defines the meaning of a program through logical assertions about its state before and after execution, can be used to **prove properties** about operational semantics. 
  - **Example**: Using axiomatic semantics, we could prove that a program terminates or that it satisfies certain **safety** properties (e.g., no division by zero).

---

### **2. Program Specification Techniques:**

**Program specification** techniques describe the desired behavior of a program. These formal methods ensure that the program does what it is intended to do. Common specification techniques include:

- **Pre- and Post-Conditions**: These define the conditions that must hold **before** and **after** a program or method executes.
  - **Example**: For a sorting function:
    - **Pre-condition**: The input is an unsorted array of integers.
    - **Post-condition**: The array is sorted in ascending order.

- **Invariants**: These are conditions that must hold **throughout** the execution of a program or loop.
  - **Example**: For a loop calculating the factorial of a number, an invariant could be:
    - `result = factorial(i)` holds at each iteration.

- **State Machines**: A model that describes the different states a program can be in and the transitions between those states.
  - **Example**: A **traffic light** state machine could have states like `green`, `yellow`, and `red`, with transitions triggered by timers or sensor inputs.

- **Algebraic Specifications**: These describe the behavior of a program using algebraic equations. It’s particularly useful for defining abstract data types (e.g., lists, sets).
  - **Example**: A **queue** can be specified algebraically with operations like `enqueue(x)` and `dequeue()`.

---

### **3. Deterministic vs. Non-Deterministic Specifications**:

- **Deterministic Specifications**: These are precise and guarantee that any implementation will always produce the same result for the same inputs.
  - **Example**: A deterministic specification for a sorting algorithm might state that it must sort a list in **ascending order**.

- **Non-Deterministic Specifications**: These allow for some flexibility in the implementation, meaning that different implementations might produce different results, as long as they all satisfy the specification.
  - **Example**: A non-deterministic specification for a sorting algorithm might state that it should return any **permutation** of the input list, without specifying the exact order of elements.

---

### **4. Examples of Program Specification Techniques for Different Constructs**:

- **Assignment**:
  - **Pre-condition**: `{x = 5}`
  - **Post-condition**: `{x = 6}`
  - This states that before the assignment `x := x + 1`, `x` is 5, and after the assignment, `x` becomes 6.

- **Conditional**:
  - **Pre-condition**: `{x > 0}`
  - **Post-condition**: `{y > 0}`
  - This states that if `x > 0`, the conditional `if x > 5 then y := 10 else y := 20` ensures that `y` is greater than 0.

- **Loop**:
  - **Pre-condition**: `{i = 0 and sum = 0}`
  - **Post-condition**: `{sum = 45}`
  - This specifies that while `i < 10`, the loop adds `i` to `sum`, and after the loop finishes, `sum` will be 45 (for example, summing the first 9 integers).

---

### **5. Lesson Summary**:

- **Program semantics and specification** are critical for designing, developing, and verifying correct and reliable systems.
- **Formal methods** provide a solid foundation for reasoning about program behavior and ensuring correctness.
- The lecture explored the **key approaches** to defining program meaning, such as **operational semantics**, **denotational semantics**, and **axiomatic semantics**.
- **Program specification techniques** like pre/post-conditions, invariants, and state machines help specify program behavior and ensure correctness.
- Understanding these techniques allows us to **improve software and hardware designs** and ensure they meet their intended requirements.

---

### **Summary Table**: 

| **Approach**          | **Key Characteristics**                                      | **Advantages**                              | **Disadvantages**                                    |
|-----------------------|---------------------------------------------------------------|---------------------------------------------|------------------------------------------------------|
| **Operational Semantics** | Defines meaning by describing execution on an abstract machine | Intuitive, easy to understand, good for complex languages | Can be difficult to reason about program properties |
| **Denotational Semantics** | Defines meaning by mapping programs to mathematical objects  | Abstract, good for reasoning about program properties | Can be difficult to define for complex languages     |
| **Axiomatic Semantics** | Defines meaning by specifying effects on assertions           | Good for proving program correctness        | Can be difficult to define axioms and inference rules |

---

By understanding and applying **operational**, **denotational**, and **axiomatic semantics**, along with **program specification techniques**, we can ensure our software and hardware meet the intended **correctness**, **safety**, and **reliability** standards.