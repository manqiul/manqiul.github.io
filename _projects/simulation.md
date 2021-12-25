---
layout: page
title: Pandemic Flu Spread Simulation
description: Simulated how a pandemic could develop within a class under different conditions.
img: assets/img/flu_simulation.png
importance: 5
category: work
---
## Team
Ahmed Rabbani, Manqiu Liu, Sai Yang  

## Problem Statement 

 - In this simulation project, we consider the spread of a pandemic flu in a classroom of 21 elementary school kids. At the beginning of the simulation, 20 of the kids are healthy and susceptible to the flu, and one kid (Tommy) is infected with the flu virus. The infected kid has the chance of contacting everyone in the classroom and spreading the flu to anyone he meets, at a probability p of 0.02 per day. For our initial deterministic model, we assume that, as in the problem description, any infected person will be infectious for 3 consecutive days. On any of the three days, any individual susceptible kid has a chance of 0.02 of getting infected by the infectious person. After 3 days of infection, the infected kid will fully recover and is immune to the flu.  

## Approach 

1.	Building a deterministic simulation model with the parameters given in the problem description, such as probability of being infected, time for recovery, and capable infection scope of every infected kid, and analyzing simulation output.	  

2.	Creating a stochastic model to treat the key parameters given in the problem as unknown, introduce random variables as estimators for those parameters, and simulate the results for different distributions of the random variables in multiple replications.	  

3.	Performing scenario and sensitivity analysis to determine the impact of e.g. class size, infection rate, required recovery time to develop immunity. Based on this, we can recommend relevant protection and precaution measures, e.g. isolation policy, optimal class size, intervention activity, etc. to contain the pandemic. 



## Conclusion

 - We first investigated a deterministic method for estimating the number of infected students each day. Then we experimented with converting determined values into variables and comparing the results of uniform, exponential, and normal distributions. In addition, we used sensitivity analysis on our models to determine the importance of each parameter in our model.    

 - In the deterministic scenario, we described our model in terms of difference equations and set the initial parameters β as a constant value which was derived from infection rate and average number of contacts per day. Moreover, we updated our R category as such that the first entry in this category would be 1 followed by the number of students who were infected four days earlier. From deterministic simulation, we were able to determine that after 28 days, the pandemic ends since by then more than 20 students have recovered with immunity and the number of infected and susceptible students have declined to zero.     

 - For stochastic simulation, we find that adding randomness into our model can bring different outcomes each round, while if we keep the distribution symmetric and have higher variances, the peak point of infection and equilibrium point of the system would be similar to the deterministic case. Besides, we also found that if the school taking strict social distancing policies, the flu could be stopped in early stage.     

 - In the sensitivity analysis, we used the deterministic model as the baseline and tested different combinations of the parameters for the simulation. We found that the spread of pandemic flu is closely related to the infection probability of an individual, the recovery time from the disease, and the class size. To successfully contain the pandemic, it is crucial to identify the virus early and take precautionary measures such as isolating infected people and keeping social distancing before the flu evolves.      

 - We conclude our report with a project summary and discussion on the further improvement for our model. Our models were all predicated on the assumption that the classroom is a closed system, that the flu is not contagious, and so on. In reality, however, the situations are far more complicated. So, in the following steps, we'll try to simulate in a more open system and experiment with a larger number of parameters.      

 - Besides, when we were considering the daily variation of students’ contact rate, we used random numbers to simulate the variation. We could improve our simulation by collecting real world data of student’s everyday activities and make our simulation model more accurate.

