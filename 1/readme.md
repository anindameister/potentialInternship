## Context, Motivation and Objectives
- Ethics describe in relative way what is fair or unfair according to a set of values.
- An agent behaves ethically if she is able to justify and make her decision in accordance to a set of values
- Modeling such an ethical decision making
may consist in representing it with an **argumentation** process. 
- argumentation: the action or process of reasoning systematically in support of an idea, action, or theory.
- This last one, is represented by a Dung’s framework [[1]](#1) which is a graph where nodes represent arguments and edges represent attacks between arguments.
- Dung’s framework does not consider the notion of values, and it has been extended to value based argumentation framework which associates values with arguments [[2]](#2).
- However, since it is an abstract argumentation approach, no explicit mechanism to build this argumentation graph has been specified.
- The global objective of this internship will be to implement a value-based argumentation framework enabling agents to make ethical decisions in a simulated environment.
-  It will be applied to the domain of the regulation of urban traffic
where we will design a responsible routing service for travelers.
- The theoretical objective is to delegate the decision process (here the argumentation process)of an agent, which is associated to the traveler, in order to define a decision as a compromise between the characteristics of the traveler (including her values)and the characteristics of the system (including global values).
- Classically, agent decision is constrained by the existing alternatives (i.e. his possible plans) and traveler features (e.g. does the traveler own a car ?), and it has to respect, as far as possible, the travelers’ preferences.
- However to be sustainable, the agent decisions must also consider society objectives, as the decrease of pollution.
- These two points of view, i.e. travelers’ preferences and society objectives, refer to distinct values: individual values and collective values.
- A microscopic simulator embedded in the plateforme Territoire will be used
to build the argumentation graph the agents will use to make decisions.
- Considering a car trip, this simulator computes alternatives by considering different modes (public transport, car, walking, etc.) or avoiding the regulated area.
- Because it simulates the car trip of the traveler, it may compute indicators about the state of the current traffic.
- It also computes indicators for evaluating the initial trip and the alternatives.
- Thus, these computed indicators will be used
to validate arguments and attack relations between arguments.
- For instance,thanks to these indicators, we will be able to generate arguments as a couple(supports, conclusion) where supports would be "Taking the car at 5.30 pm to go from A to B will contribute to generate a CO2 emission rate of X” and a conclusion of this argument would be ”therefore X is higher than the pollution threshold set by the policies”. 
- This argument may be associated with the value ”Environmental Sustainability” and can attack all arguments that would defend
the position ”taking car”.
- Finally, agents will only make decisions that they can defend by at least one preferred set1 of arguments calculated by the system.
- However enumerating all preferred sets of arguments takes too much time to be reactive for individual agent’s decisions [[5]](#5) and since we only need one set of arguments to defend the agent’s decision, a challenge will be to propose a relevant heuristic to choose a good preferred set of arguments that respect the user’s preferences as much as
possible.

## Expected results
- State of the art on how argumentation is currently used in a simulated
environment.
- Application of the value based argumentation framework [[3]](#)[[5]](#5) for the
transportation domain. Definition of agents’ values shared in the system.


## References
<a id="1">[1]</a> 
 Dung, P. M. (1995). On the acceptability of arguments and its fundamental role
in nonmonotonic reasoning, logic programming and n-person games. Artificial intelligence, 77(2), 321-357.

<a id="2">[2]</a>
Bench-Capon, T. J. (2003). Persuasion in practical argument using value-based
argumentation frameworks. Journal of Logic and Computation, 13(3), 429-448.

<a id="5">[5]</a>
Kr¨oll, M., Pichler, R., Woltran, S. (2017). On the complexity of enumerating
the extensions of abstract argumentation frameworks. In Proceedings of the 26th International Joint Conference on Artificial Intelligence (pp. 1145-1152).


<a id="3">[3]</a>
Souhila Kaci et Lendeert van der Torre (2007). Preference-based argumentation:
argument supporting multiple values.
