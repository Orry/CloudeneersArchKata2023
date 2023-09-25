# Risks and Technical Debts

> This section contains a list of identified technical risks or technical debts, ordered by priority.

# Technical Depts

| Dept |                                                                                    Description                                                                                    | 
|------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| D1   | No fitness test functions to control our quality goals. The team has to implement fitness test functions to control our quality goals in their development lifecycle (DevSecOps). |

### Consequences
-  reduction the technical debt to guarantee the reach of the  quality goals
-  implement and measure results
-  plan improvements

### Recommendation: 
The technical debts should be manageable in normal sprints with a technical user story.

## Risks

| Risk |                                            Description                                             | 
|------|:--------------------------------------------------------------------------------------------------:|
| R1   |                           Underestimated global user traffic prediction.                           |
| R2   | Measurements the scalability and client latency (connections time out) on each production region.  |
| R3   | If the latency from more distant regions is by factor 2 higher than in the home region prediction. |

### Probability:
30%

### Mitigation:
* We use CDN and edge functions to shift the load as close to the user
* use lazy loading in UI
* compress delivered frontend elements
* think about using another region, if user base is big enough and latency is not acceptable for mobile users 

[<<Previous Page](./07_Architectural_Characteristics.md) ---- [Next Page >>](./09_Glossary.md)
