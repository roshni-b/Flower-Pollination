# Flower Pollination Algorithm Implementation
Flower pollination algorithm is a metaheuristic algorithm that was developed by [https://en.wikipedia.org/wiki/Xin-She_Yang](Xin-She Yang), based on the pollination process of flowering plants.

This algorithm has 4 rules or assumptions:
1. Biotic and cross-pollination is considered as a global pollination process with pollen carrying pollinators performing Levy flights.
2. Abiotic and self-pollination are considered as local pollination.
3. Flower constancy can be considered as the reproduction probability is proportional to the similarity of two flowers involved.
4. Local and global pollination are controlled by a switch probability {\displaystyle p\in [0,1]} {\displaystyle p\in [0,1]}. Due to the physical proximity and other factors such as wind, local pollination can have a significant fraction q in the overall pollination activities.

These rules can be translated into the following updating equations:
{\displaystyle x_{i}^{t+1}=x_{i}^{t}+L(x_{i}^{t}-g_{*})} {\displaystyle x_{i}^{t+1}=x_{i}^{t}+L(x_{i}^{t}-g_{*})}
{\displaystyle x_{i}^{t+1}=x_{i}^{t}+\epsilon (x_{i}^{t}-x_{k}^{t})} {\displaystyle x_{i}^{t+1}=x_{i}^{t}+\epsilon (x_{i}^{t}-x_{k}^{t})}
where {\displaystyle x_{i}^{t}} {\displaystyle x_{i}^{t}} is the solution vector and {\displaystyle g_{*}} {\displaystyle g_{*}} is the current best found so far during iteration. The switch probability between two equations during iterations is {\displaystyle p} p. In addition, {\displaystyle \epsilon } \epsilon  is a random number drawn from a uniform distribution. {\displaystyle L} L is a step size drawn from a Lévy distribution.

Lévy flights using Lévy steps is a powerful random walk because both global and local search capabilities can be carried out at the same time. In contrast with standard Random walks, Lévy flights have occasional long jumps, which enable the algorithm to jump out any local valleys. Lévy steps obey the following approximation:

{\displaystyle L\sim {\frac {1}{s^{1+\beta }}},} {\displaystyle L\sim {\frac {1}{s^{1+\beta }}},}
where {\displaystyle \beta } \beta  is the Lévy exponent. It may be challenging to draw Lévy steps properly, and a simple way of generating Lévy flights {\displaystyle s} s is to use two normal distributions {\displaystyle u} u and {\displaystyle v} v by a transform[49]

{\displaystyle s={\frac {u}{|v|^{1+\beta }}},} {\displaystyle s={\frac {u}{|v|^{1+\beta }}},}
with
{\displaystyle u\sim N(0,\sigma ^{2}),\quad v\sim N(0,1),} {\displaystyle u\sim N(0,\sigma ^{2}),\quad v\sim N(0,1),}
where {\displaystyle \sigma } \sigma  is a function of {\displaystyle \beta } \beta .
