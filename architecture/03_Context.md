# Context
3. [Context](#context)
    1. [Business Context](#business-context)
    2. [Technical Context](#technical-context)

> Defines the boundaries between the system and its communication counterparts (adjacent systems and users). It outlines the external interfaces, presenting both a business/domain viewpoint and a technical standpoint.

## Business Context
We concentrate here on the main actors and external systems. We differentiate communication and supplier external systems. Some grey systems are for future use, but not used for the first Road Warrior product.

![context](../diagrams/ARCH-KATA-00_System_business_context.png)

### Travel Assistant
Actor which acts as the preferred travel agency agent for quick problem resolution.
### Traveler
The actual Traveler interacting with the Road Warrior system.
### Email Integration
The module responsible for polling and processing travel-related emails.
### Sharing and Social Media Integration
The module responsible for enabling users to share trip information on social media platforms.
### Travel Systems Integration
The component that interfaces with external travel systems (e.g., SABRE, APOLLO, Hotel, car rental) for real-time updates.
### Suppliers help support
The help line for travelers to suppliers. They have read access to shared trips of travellers.

## Technical Context
We only name the name protocols and formats, which must be refined later.

![context](../diagrams/ARCH-KATA-00_System_technical_context.png)

We support standard web protocols (https, SMTP, VPN) and formats (json).
For Authentication we will use ID Provider which support OAuth/OID protocol.

## Use Cases
### Actors Relations
![context](../diagrams/Road_Warrior_UseCases-Actors_relations.png)

**Traveller** - Person who travel and need to get all of the data.

**Co-traveller** - Person who wants to travel together and need to book same flight/hotel.

**Travel Observer** - Person who tracks the trip progress. For example transfer service or close friend.

**Secretary or Travel Assistant** - Some person who assists with booking and tracking changes. For most of users it will be probably wife or husband.

**RoadWarrior employees** receive feedback via fmb. Normally no direct communication required.

**Supplier contact** contact from Airlines, Taxi, Bus or other trip supplier for emergency situations.


### Traveller's
![context](../diagrams/Road_Warrior_UseCases-UC_Traveller.png)

**Get Upcoming trips** - basic view to the trips that are not ended

**Get all of the trips** - to have full list of trips

**Get passeed trips** - get list of trips that are already ended. It might be required for travel reporting. 

**Get Trip overicew** - basic functionality to view certain trip details.

**Create new shoulder** - manuall adding of the new information part. Like new taxi or nre train.

**Get shoulder details** - get all of the details for particular part of the trip. That should include the booking number all necessary identification data like QR or bar codes.

**Edit shoulder** - change booking details in the system according to other changes. Most usable case is that we have new updates received via alternative channel (like by phone) or email was not parsed.

**Delete shoulder** - remove current supplier information. 

**Get supplier contacts** - getting first contact information for supplier for emergency case. For example taxi didn't appear - where to call.

**Observe sharings** - get list of shared links. 

**Create sharing link** - create new link to share with observer.

**Revoke link** - revoke link if it was shared to a wrong round.

**Create text export** - create export for Co-traveller that can be shared in a text format for similar bookings.

**Send text booking export** - send created text export to Co-traveller.

**Get trip change notification** - receive notification about urgent update.

**Yearly report** - receive yearly report about travel information, routes, frequency and so on...

**Email feedback channel** - send feedback to developers.

### Co-Traveller's
![context](../diagrams/Road_Warrior_UseCases-UC_Co-traveller.png)

### Observer
![context](../diagrams/Road_Warrior_UseCases-UC_Observer.png)

### Secretary
![context](../diagrams/Road_Warrior_UseCases-UC_Secretary.png)

[<<Previous Page](./02_Constraints.md) ---- [Next Page >>](./04_Solution_Strategy.md)

