# Requirement Overview
## What is Road Warrior?
A new startup wants to build the next generation online trip management dashboard to allow travelers to see all
of their existing reservations organized by trip either online (web) or through their mobile device.

# vison
"All your travel information in on place world wide"

## Essential Features
- Poll email looking for travel-related emails
- Filter and whitelist certain emails
- Add, update, or delete existing reservations manually
- Items in the dashboard should be able to be grouped by trip, 
- Automatically remove completed trips from the dashboard.
- Users should also be able to share their trip information (Social Media or private Links)
- Provide end-of-year summary reports for users
- Must integrate seamlessly with existing travel systems (i.e, SABRE, APOLLO)

## Key Quality Characteristics
The following table describes the key quality characteristics of Road Warrior. The order of the goals gives you a rough idea of their importance and was made based on the
[Architecture Characteristics Worksheet](../images/ARCH-KATA-07_Architecture_Characteristics_Worksheet.png) by Marc Richards. The identified qualitiy characteristics are the main driver for our architecture style decision (refer to: [0010-architectural-style-decision](../ADRs/0010-architectural-style-decision.md)).

| Quality Goal      |                                                                                                                                                                                                                               Motivation                                                                                                                                                                                                                                |
|-------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------:|
| High Availability |                                                                                          Based on the technical requirement discussed with the stakeholder the users must be able to access the system at all times (max 5 minutes per month of unplanned downtime). Along with that Travel updates must be presented in the app within 5 minutes of generation by the source.                                                                                          |
| Scalability       |                                                                                                                                                                                Ensuring that the system can handle the two million active users per week and support international usage                                                                                                                                                                                |
| Responsiveness    |                                                                                                                                                                                           Response time from web (800ms) and mobile (First-contentful paint of under 1.4 sec)                                                                                                                                                                                           |

Other architectural characteristics (especially Interoperability) which as well impact the decision on which architecture style to choose are described in [07_Architectural_Characteristics](07_Architectural_Characteristics.md).

## Stakeholders
The table below lists all the stakeholders and their expectations.

| Role                |                                                                Motivation                                                                |
|---------------------|:----------------------------------------------------------------------------------------------------------------------------------------:|
| Judges of the Kata  |                                 The Kata judges will assess and evaluate the architecture documentation.                                 |
| Cloudeneers         | Enhance your proficiency in architecture documentation through the Road Warrior challenge, which offers a practical learning opportunity. |
| Future Participants |                                       Prospective participants will gain insight into the prerequisites for joining these Katas.|
