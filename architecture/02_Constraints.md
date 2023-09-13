# Constraints
2. [Constraints](#constraints)
    1. [Assumptions](d#assumptions)
    2. [Technical Constraints](#technical-constraints)
    3. [Organizational Constraints](#organizational-constraints)
    4. [Conventions](#conventions)

At the project's outset, several constraints were incorporated into the design of Road Warrior, and these constraints continue to influence the solution. This section outlines these limitations and, when applicable, provides the reasons behind their implementation.

## Assumptions
> While working on the Kata challenge we are forced to make some assumptions about the system.
> In the following table we will list all assumptions made for this solution.

| Assumptions          |                                                                                                                      Description                                                                                                                       |
|----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Email polling        |                                                                   The Email polling will take place every 3 minutes. Thus, this component can be extracted as a serverless function.                                                                   |
| Social Media Sharing | When we share travel information on social media, we limit it to basic text-based details. In contrast, when we share travel information with specific individuals, we grant them read-only access to our dashboard by providing a link. |
| Costs                |                                                          Cost considerations do not play a significant role for Road Warrior, as our assumption is that they are supported by a sponsor who is eager to fund our solution.                                                         |


## Technical Constraints
The following technical constraints must be respected:

| Constraint            |                                                                          Motivation                                                                          | 
|-----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Operating System      |    The online web application must ensure seamless PWA (Progressive-Web-Application) functionality across all supported web browsers and mobile devices.     |
| Cloud Agnostic Design |                                          The online web application must be able to run across any cloud provider.                                           |
| Containerization      |                   Use containerization (e.g., Docker) and container orchestration (e.g., Kubernetes) for easy deployment and scalability.                    |


## Organizational Constraints
The following organizational constraints are defined:

| Constraint                   |                                                                                   Motivation                                                                                   | 
|------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Team                         |                           The [Cloudeneers](../team/introduction.md)  supported by materials and resources provided by Marc Richards and Neal Ford.                            |
| Timeline                     |                         Start of the Kata was the 11th of september 2023. Solutions in the Github repos are due by 11:59pm ET Saturday, September 16.                          |
| Tools and version management | Generating ideas in Miro, managing tasks through GitHub Projects, creating designs with draw.io, and documenting outcomes within GitHub, with updates pushed using IntelliJ IDE. |
| Business Model               |             As a startup we use the fremium model for road worrior. We are financed by seed fund for the first round and by the affiliate fees from teh partners.              |


## Conventions
During the Kata challenge the below conventions are mandatory:

| Conventions                |                                                                         Motivation                                                                          | 
|----------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------:|
| Architecture documentation |                                           Terminology and structure according to the arc42 template, version 8.0.                                           |
| Repository                 | Commits must be linked to a task on the GitHub Project Board to ensure traceability and a clean commit history (e.g. "ARCH-KATA-00: Requirements Analysis") |


[<<Previous Page](./01_Introduction_And_Goals.md) ---- [Next Page >>](./03_Context.md)
