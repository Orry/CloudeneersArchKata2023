# 2. UI scopes

## Status
Accepted

## Context
Requirement interpretation: 
Requirement refers to the "active users" amount. We need to separate Active and other users naming.
Also defining how to distinguish active users.

# Decision
* **Active users** - those who are in the travel mode based on the travel date/time.
* **Inactive users** - those who's travel date/time are not right now.

# Consequences
1. SLA's definition based on the load are affected. 
2. Load calculation method affected.
