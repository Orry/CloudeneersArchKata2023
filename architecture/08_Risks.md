# Risks

This section contains a list of identified technical risks or technical debts, ordered by priority.

# Debt: No fitness test functions to control our quality goals
The team has to implement fitness test functions to control our quality goals in their development lifecyle (DevSecOps).

## Consequences
-  reduction the technical debt to garantie the reach of the  quality goals
-  implement and measure results
-  plan impovements

## Recommendation: 
The technical debts should be managable in normal sprints with a technical user story.

# Risk: Underestimated global user traffic prediction 
Measurements the scalability and client latency (connections time out) on each production region.
If the latency from some farer regions is by factor 2 higher than in the home region
prediction.

## Probability: 30%

## Mitigation:
* We use CDN and edge functions to shift the load as close to the user
* use lazy loading in UI
* compress delivered frontend elements
* think about using another region, if user base is big enough and latency is not acceptabel for mobile users ther 

[<<Previous Page](./07_Architectural_Characteristics.md) ---- [Next Page >>](./09_Glossary.md)
