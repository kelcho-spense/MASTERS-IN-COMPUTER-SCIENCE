## Introduction to Artificial Intelligence

### What is Artificial Intelligence (AI)?

Artificial Intelligence (AI) refers to the field of study and engineering focused on building machines or systems that can simulate human intelligence. AI aims to not only understand how humans think and reason but to replicate and create intelligent behavior in machines. The term was coined in 1956, and since then, AI has been divided into various subfields, such as machine learning, robotics, natural language processing, and expert systems.

AI can be understood through different approaches:
1. **Acting Humanly (Behavioral Approach)**: This approach seeks to make machines exhibit intelligent behavior similar to humans. The Turing Test, proposed by Alan Turing in 1950, is one way to evaluate this by testing if a machine's responses are indistinguishable from those of a human in a conversation.
  
2. **Thinking Humanly (Cognitive Approach)**: This approach involves understanding how human beings think, using cognitive science methods such as psychological experiments and brain imaging to model human cognition in machines.
  
3. **Thinking Rationally (Logical Approach)**: This approach is grounded in logic and reasoning. The idea is to formalize the process of correct reasoning and use it in machines to perform tasks based on rational decision-making.

4. **Acting Rationally (Rational Agent Approach)**: A rational agent is an entity that acts to achieve the best outcome based on its knowledge. This approach emphasizes building intelligent systems that make decisions to achieve defined goals, even if there’s uncertainty involved.

---

### The Foundations of Artificial Intelligence

AI's foundations draw from several disciplines, each contributing essential ideas and methods:

1. **Philosophy**: 
   - Ancient philosophers like Aristotle focused on reasoning and logic, shaping the foundation for formal logic used in AI. Philosophical questions such as "How does the mind arise from the brain?" and "Where does knowledge come from?" are key to understanding AI’s objectives.

2. **Mathematics**: 
   - Mathematics, particularly in logic and computation, is central to AI. Key developments in formal logic (e.g., George Boole’s Boolean logic and Gottlob Frege’s first-order logic) laid the groundwork for building algorithms capable of deduction and reasoning.
   - The concept of computation, introduced by pioneers like Alan Turing, defines what can and cannot be computed, providing a theoretical basis for AI.

3. **Neuroscience**: 
   - Neuroscience has provided insights into how the brain processes information, offering inspiration for neural networks and understanding complex cognitive functions. Concepts such as neurons and their connections influence the design of AI systems that mimic brain-like functions.

4. **Psychology**: 
   - The study of human and animal cognition has informed the development of AI models that simulate mental processes. Psychological theories about memory, perception, and reasoning have been instrumental in shaping AI research.

5. **Economics and Decision Theory**: 
   - Decision theory, particularly from economists like John von Neumann, has contributed to AI's focus on optimal decision-making. AI models often incorporate probabilistic reasoning and utility theory to make decisions under uncertainty.

6. **Computer Engineering**: 
   - Advances in computer hardware and software have enabled the rapid growth of AI. From early computers to modern machines capable of processing vast amounts of data, the development of computational tools has been crucial for the realization of AI.

7. **Control Theory and Cybernetics**: 
   - Control theory focuses on building systems that can autonomously regulate themselves based on feedback from the environment. This idea influenced the development of AI systems capable of operating autonomously and adapting to changing conditions.

8. **Linguistics**: 
   - Linguistics, particularly computational linguistics, has significantly influenced natural language processing in AI. Understanding how humans use and process language has been key to building AI systems that can communicate effectively.

---
## Intelligent Agents

### Agents and Environment

**1. Agents and their Environment**
   - **Agent**: An agent is anything that perceives its environment through sensors and acts upon it via actuators. For example:
     - A human agent uses eyes, ears, and limbs as sensors and actuators.
     - A robotic agent may use cameras, infrared sensors, and motors.
     - A software agent uses digital inputs like keystrokes and network packets and outputs via the screen, files, or network.
   - **Percepts**: The immediate sensory inputs an agent receives.
   - **Percept Sequence**: The history of all perceptions the agent has experienced.
   - **Agent Function**: A mathematical description that maps percept sequences to actions.
   - **Agent Program**: The practical implementation of the agent function, which is executed within a physical system (like a robot or computer).

**Example**: A vacuum cleaner agent in a simple world with two locations (A and B) can decide actions like moving or sucking dirt based on the percepts (location and cleanliness) it receives.

---

### Good Behavior - Concept of Rationality

**2. Rational Agent**
   - **Rationality**: The agent's behavior is considered rational if it maximizes its performance measure, based on its perceptions and built-in knowledge of the environment.
   - **Performance Measure**: A function that defines how to evaluate the agent’s actions based on the environment's states.
   - **Rational Agent Definition**: An agent is rational if it selects actions that maximize its expected performance measure, given its percept sequence and knowledge.
   - **Rationality vs. Omniscience**: Rational agents are not omniscient and do not know the outcome of their actions in advance; they act based on expected outcomes.

---

### Nature of Environment

**3. Task Environment**
   - **PEAS**: Performance measure, Environment, Actuators, and Sensors.
   - **Task Environment Specification**: Defines the parameters and constraints within which an agent operates. The environment may vary in complexity and limitations, which affects the agent design.

**Key Properties of Task Environments**:
   - **Observability**: Fully observable or partially observable based on available sensors.
   - **Determinism**: Whether the environment’s state is fully determined by the agent’s actions (deterministic) or involves some randomness (stochastic).
   - **Episodic vs. Sequential**: In episodic environments, actions do not affect future decisions, while in sequential environments, past actions influence future decisions.
   - **Dynamic vs. Static**: Dynamic environments change while the agent is deliberating, whereas static ones do not.
   - **Discrete vs. Continuous**: The state of the environment, time, and actions can be discrete or continuous.
   - **Known vs. Unknown**: Whether the agent has full knowledge of the environment's rules or has to learn over time.

---

### Structure of Agents

**4. Structure of Intelligent Agents**
   - **Agent Program**: This program dictates the actions based on the agent’s perceptions.
   - **Architecture**: The underlying computing system that runs the agent program and interacts with the environment through sensors and actuators.
   - **Agent Types**:
     1. **Simple Reflex Agents**: Act based on the current percept, with no memory of previous states.
     2. **Model-based Reflex Agents**: Maintain an internal state to handle partial observability by keeping track of unobserved parts of the environment.
     3. **Goal-based Agents**: Use goals to guide action selection, considering future consequences and sequences of actions.
     4. **Utility-based Agents**: Consider not just achieving goals but doing so in the best possible way by maximizing utility.

**Example of a Simple Reflex Agent**: A vacuum agent that performs the action "Suck" if the square is dirty and moves in another direction otherwise.

**Goal-based and Utility-based Agents**:
   - Goal-based agents make decisions based on achieving specific goals, whereas utility-based agents aim to maximize a utility function that evaluates different outcomes of an action.

**5. Learning Agents**
   - **Learning Element**: This component learns from experience and feedback to improve future performance.
   - **Performance Element**: The part of the agent that selects actions based on its current knowledge.
   - **Critic**: Provides feedback on the agent’s performance to guide learning.
   - **Problem Generator**: Suggests actions for the agent to explore, helping it learn better strategies.

Learning agents improve their behavior over time, adapting to changing environments and new challenges.

This framework helps in understanding the vast diversity of intelligent agents and how they can be designed to operate effectively in various environments.

---
## Problem Solving Agents

### **Problem-Solving Agents**

In this section, we explore **problem-solving agents**, which are goal-based agents that aim to find a sequence of actions to achieve a goal when no single action will suffice. The agent starts from an **initial state** and proceeds through a sequence of actions to reach the **goal state**.

#### **1. Types of Agents:**
- **Reflex Agents**: These are simple agents that act based on a direct mapping from states to actions. They don’t consider future actions or long-term consequences.
- **Goal-Based Agents**: These agents consider future actions and their outcomes. They are more flexible and can solve complex problems by adopting specific goals.
- **Problem-Solving Agents**: These are a specific type of goal-based agent. They use **atomic representations** (states of the world are considered as wholes) to navigate problem spaces, as described in **Section 2.4.7**.

#### **2. Problem Formulation**:
A **problem** consists of five components:
- **Initial State**: The starting state of the agent. For example, in the Romania problem, the agent starts in the city of Arad.
- **Actions**: The possible actions that the agent can take. For example, in the Romania problem, the agent can go from one town to another.
- **Transition Model**: Describes the effect of each action. For example, moving from Arad to Sibiu leads to the new state of being in Sibiu.
- **Goal Test**: A test that checks if the agent has reached the goal state (e.g., in Romania, the goal is to reach Bucharest).
- **Path Cost**: The cost associated with each action. For example, the cost of traveling between cities could be measured in distance (kilometers).

#### **3. Goal Formulation and Problem Solving**:
- **Goal Formulation**: The process of defining the desired goal(s) and deciding which states are considered part of the goal. It limits the problem-solving process by focusing on relevant objectives.
- **Problem Formulation**: Deciding which states and actions to consider for the goal. The level of abstraction is crucial here. For example, in a navigation problem, the agent may choose to abstract the problem at the level of towns rather than focusing on individual streets.

#### **4. Search Process**:
The agent uses a search algorithm to find a sequence of actions that leads to the goal. This process involves:
1. **Problem Formulation**: Defining the problem space (initial state, actions, transition model, etc.).
2. **Search**: The agent uses a search algorithm (uninformed or informed) to explore possible paths and find a solution.
3. **Execution**: Once the solution (action sequence) is found, the agent follows it step by step to reach the goal.

- **Uninformed Search**: These search algorithms have no additional information about the problem other than its definition. Examples include **breadth-first search** and **depth-first search**.
- **Informed Search**: These algorithms use additional knowledge (heuristics) to guide the search and make it more efficient. Examples include **A* search**.

#### **5. Solution Representation**:
- A **solution** to a problem is a sequence of actions that transforms the initial state to the goal state.
- **Optimal Solution**: This is the solution with the lowest path cost among all possible solutions.

---

### **Example Problems**:

#### **1. Toy Problems**:
- **Vacuum World**: A simple environment where an agent moves between two locations, cleaning them. The goal is to clean both locations.
  - **States**: The state is determined by the agent’s location and whether the locations are clean.
  - **Actions**: Move Left, Move Right, Suck.
  - **Goal Test**: All locations are clean.
  - **Path Cost**: Each step has a cost of 1.

- **8-Puzzle**: A sliding puzzle with a 3×3 board, where the goal is to arrange tiles in a specific order.
  - **States**: The position of the 8 tiles and the blank space.
  - **Actions**: Slide tiles (Left, Right, Up, Down).
  - **Goal Test**: The tiles are arranged in a specific goal configuration.
  - **Path Cost**: Each move has a cost of 1.

- **8-Queens Problem**: Place 8 queens on a chessboard such that no queen attacks another.
  - **States**: Any arrangement of 0 to 8 queens on the board.
  - **Actions**: Add a queen to an empty square.
  - **Goal Test**: 8 queens are on the board, none attacked.
  - **Path Cost**: The path cost is irrelevant, only the final configuration matters.
 
    Here is the full problem description with requirements and a breakdown of **States**, **Actions**, **Goal Test**, and **Path Cost** for both the **Missionaries and Cannibals Problem** and the **Water Jug Problem**:

---

### **Missionaries and Cannibals Problem**

#### **Problem Description:**
There are three missionaries and three cannibals on one side of a river. They need to cross the river using a boat that can hold at most two people. The challenge is to transport all the missionaries and cannibals to the opposite side without violating the rule that at no point on either side of the river can the cannibals outnumber the missionaries. If the cannibals outnumber the missionaries on either side, the cannibals will eat the missionaries. 

#### **Requirements:**
- The boat can hold only two people at a time.
- The goal is to get all the missionaries and cannibals to the opposite bank.
- The number of cannibals cannot exceed the number of missionaries on either side of the river at any point.

#### **Problem Formulation:**

1. **States**:
   - A state can be represented as a tuple `(M_left, C_left, M_right, C_right, Boat)`, where:  
     - `M_left`: The number of missionaries on the left bank.  
     - `C_left`: The number of cannibals on the left bank.  
     - `M_right`: The number of missionaries on the right bank.  
     - `C_right`: The number of cannibals on the right bank.  
     - `Boat`: Denotes where the boat is (either left or right bank).  

   **Example state**: `(3, 3, 0, 0, 'left')` means all three missionaries and all three cannibals are on the left bank, and the boat is on the left side.

2. **Actions**:
   - **Send 1 missionary across**: Move 1 missionary from one side to the other.
   - **Send 1 cannibal across**: Move 1 cannibal from one side to the other.
   - **Send 2 missionaries across**: Move 2 missionaries from one side to the other.
   - **Send 2 cannibals across**: Move 2 cannibals from one side to the other.
   - **Send 1 missionary and 1 cannibal across**: Move 1 missionary and 1 cannibal from one side to the other.
   - **Bring 1 person back**: Move 1 person (either a missionary or a cannibal) back to the starting bank.

3. **Goal Test**:  
   - The goal is to have all the missionaries and cannibals on the right bank with the boat on the right side: `(0, 0, 3, 3, 'right')`.

4. **Path Cost**:  
   - The path cost can be the number of actions (steps) taken to reach the goal. Each action can have a uniform cost (e.g., cost = 1 per action).

---

### **Water Jug Problem**

#### **Problem Description:**
You are given two empty water jugs:
- One jug holds 4 gallons of water.
- The other jug holds 3 gallons of water.

The task is to fill the 4-gallon jug with exactly 2 gallons of water using the jugs and performing the appropriate actions.

#### **Requirements:**
- You can fill either jug from a water source or pour water from one jug to the other.
- The goal is to get exactly 2 gallons of water in the 4-gallon jug.
- You are only allowed to work with the two jugs (4-gallon and 3-gallon), and their capacities are fixed.

#### **Problem Formulation:**

1. **States**:
   - A state can be represented as a tuple `(jug_4, jug_3)`, where:
     - `jug_4`: The amount of water in the 4-gallon jug (ranging from 0 to 4 gallons).  
     - `jug_3`: The amount of water in the 3-gallon jug (ranging from 0 to 3 gallons).  

   **Example state**: `(4, 0)` means the 4-gallon jug is full (4 gallons), and the 3-gallon jug is empty.

2. **Actions**:
   - **Fill 4-gallon jug**: Fill the 4-gallon jug to its capacity.
   - **Fill 3-gallon jug**: Fill the 3-gallon jug to its capacity.
   - **Pour from 4-gallon jug to 3-gallon jug**: Pour water from the 4-gallon jug into the 3-gallon jug until the 3-gallon jug is full or the 4-gallon jug is empty.
   - **Pour from 3-gallon jug to 4-gallon jug**: Pour water from the 3-gallon jug into the 4-gallon jug until the 4-gallon jug is full or the 3-gallon jug is empty.
   - **Empty the 4-gallon jug**: Empty all the water in the 4-gallon jug.
   - **Empty the 3-gallon jug**: Empty all the water in the 3-gallon jug.

3. **Goal Test**:  
   - The goal is to have exactly **2 gallons** of water in the 4-gallon jug. Therefore, the goal state is `(2, x)` where `x` can be any amount of water in the 3-gallon jug (0 ≤ x ≤ 3).

4. **Path Cost**:  
   - The path cost can be the number of actions (steps) taken to reach the goal. Each action can have a uniform cost (e.g., cost = 1 per action).

---

### Summary of Problem Formulation for Both Problems:

#### **Missionaries and Cannibals**:
- **States**: A tuple of missionaries and cannibals on both banks and the position of the boat.
- **Actions**: Sending missionaries and cannibals across the river.
- **Goal Test**: All missionaries and cannibals are on the right bank.
- **Path Cost**: Number of actions taken to reach the goal.

#### **Water Jug**:
- **States**: Amount of water in both the 4-gallon and 3-gallon jugs.
- **Actions**: Fill and pour between the jugs.
- **Goal Test**: Exactly 2 gallons of water in the 4-gallon jug.
- **Path Cost**: Number of actions taken to achieve the goal.

These formulations help define the problem-solving process, guiding an AI agent in finding a solution using algorithms such as search or planning.

#### **2. Real-World Problems**:
- **Route-Finding Problem**: Find the shortest route between two locations, such as in the Romania problem.
  - **States**: Locations, times, and other relevant information.
  - **Actions**: Travel from one location to another.
  - **Goal Test**: Reaching the destination.
  - **Path Cost**: Depends on distance, time, and other factors like cost and delays.

- **Touring Problem**: Visit every city at least once and return to the starting point, similar to the **Traveling Salesperson Problem (TSP)**.
  - **States**: The set of cities visited.
  - **Actions**: Move between cities.
  - **Goal Test**: All cities have been visited, and the agent has returned to the start.
  - **Path Cost**: Minimize the total distance traveled.

- **Protein Design**: Finding the sequence of amino acids that will fold into a protein with the desired properties.
  - **States**: Possible sequences of amino acids.
  - **Actions**: Mutate or rearrange the sequence.
  - **Goal Test**: The protein folds correctly to meet the desired properties.
  - **Path Cost**: Depends on the computational cost of evaluating protein folds.

---

This summary provides a clear breakdown of the problem-solving agent approach, problem formulation, and the types of problems (both toy and real-world) that AI agents can address. The key concepts—such as state space, goal test, and search algorithms—are crucial for developing intelligent systems capable of solving complex tasks.
