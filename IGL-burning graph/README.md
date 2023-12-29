# Burning Graph at the *Illinois Geometry Lab*
## Overview
My journey to research took place at the *Illinois Geometry Lab*, an environment dedicated to geometry-centered projects. The *Burning Graph* project, my first research experience, involved collaborating with four fellow undergraduates with the ambitious goal of proving the *Burning Number Conjecture*.
## Prerequisite
To grasp the intricacies of our work, it's essential to delve into the concepts of graph burning, the burning process, and the burning number. If these concepts are strange to you and you would like to know more about this project, feel free to view the [concepts & details](https://github.com/jadestreet/Jade-Xu-graduate-application-material/blob/main/IGL-burning%20graph/concepts%20%26%20details.md) file.
## Accomplishments: Proving & Simulation
My contributions to the Burning Graph project were twofold: **mathematical theorem proving** and **the implementation of the first simulation algorithm**.
I participated in proving the theory by finding a contradiction in the **Minimal Counterexample** (the smallest example that falsifies a claim). In the realm of mathematical proofs, we successfully demonstrated the conjecture in two specific cases[^1], but applying it broadly posed challenges.To break through the bottleneck, our mentor advised a shift toward implementing a simulation algorithm.
### Challenges Faced
Notably, this wasn't the typical computer science task. As mandated by my mentor, I was tasked with designing an algorithm that could uncover all possible burning scenarios, rather than finding the optimal one. The lack of existing simulation algorithms in this mathematical domain and my group members' unfamiliarity with algorithm design led me to take the initiative. Despite my coding experience, my knowledge leaned heavily towards data structures. I lacked familiarity with dynamic programming, a crucial aspect given the mathematical nature of the topic. Additionally, my mentor's expertise lay in pure mathematics, limiting his assistance with this particular task. 
### Algorithm Design and Implementation
In overcoming these obstacles, I dedicated myself to continuous self-study and iterative refinement. To bridge the gap between mathematical abstraction and computer science application, I systematically broke down the complex structure into its fundamental components. \
Recognizing the inadequacy of existing data structures for constructing the algorithm, I innovatively devised a flexible composite version of a stack. This new version of stack contains a big stack outside that represents the burning process for the graph, and progress stack inside corresponds to all possible burning scenarios at a given round. This innovation efficiently managed memory resources, generating new cases while eliminating duplicates for precision and optimized performance. \
Finally, I successfully implemented an algorithm capable of simulating all burning situations for given graphs that containing fewer than one thousand nodes (n < 1000).

## Incident and Resolution
While this new structure successfully simulated the burning process, adapting to Python, our chosen programming language, presented challenges in certain edge cases. Collective troubleshooting efforts within the group led to identifying the issue, and I adjusted the algorithm structure to align with Python's return property. This meticulous process marked my initiation into designing complex simulations for theoretical graphs, sparking a lasting interest in graph-structured data.

[^1]: The proof is given in the report, the overview is in the poster.
