# Video Script
Below you will find the exact script used in the technical presentation video structured by title.

# Context / Problem Statement
Picture this: A business traveler, jet-lagged, weary, and burdened by a jumbled mix of flight schedules, hotel reservations, and car rental bookings. They're struggling to keep track of changes, cancellations, and updates.
In the midst of this chaos, the Road Warrior app emerges as a beacon of relief.
Road Warrior, a startup with a vision to revolutionize trip management, presents an online dashboard that neatly organizes your travel itinerary, either on the web or on your mobile device.
Imagine having all your reservations at your fingertips, updated in real time, with the ability to manually add, update, or delete items.
This is the ease that Road Warrior promises.

# Technical Choices
Born out of the need for a user-friendly, efficient, and responsive trip management tool, Road Warrior made strategic technical choices to ensure it delivers on its promise.

## Architecture Style Decision
The startup decided to use a microservice architecture in combination with serverless computing for cost optimization, ensuring scalability and availability.

## Containerization
Road Warrior's self-healing capabilities guarantee a maximum system downtime of up to five minutes per month.
Leveraging cloud-native technologies like Serverless Computing, Kubernetes and Docker, ensures efficient
resource usage and significantly reduces CO2 emissions, representing a foundational step towards a green architecture.

## E-Mail Management
We also leveraged Natural Language Processing (NLP) to extract content from emails, making it easier for the system to find travel-related emails and update the dashboard.
To maintain our system's stability, we've decoupled email scanning, email parsing, and updates merging into the trip database.
And a shared highly available database as the sole source of truth.

## Seamless Integration
The Road Warrior system is designed to work internationally and seamlessly interfaces with existing airline, hotel, and car rental systems like SABRE and APOLLO, ensuring updates are reflected in the app within five minutes - a speed that outpaces the competition.
It also partners with preferred travel agencies for quick problem resolution.

## Rich User Interface
We chose a Progressive Web Application (PWA) for the front-end, ensuring a rich user interface across all deployment platforms (web and mobile) with an optimal response time.
For seamless integration and real-time updates, we adopted GraphQL for flexible API integration.


## Notifications
Travel updates are required to be presented in the app within five minutes.
Server Send Events (SSE) are used to send instant notifications to the client side.
Mentioning that, we all know that networks in the airports and tunnels are not reliable.
Standard web-based notifications would not work.
Considering that, the system ensures that the user receives notification within 5 minutes by sending SMS in addition.

## Social Media Sharing
Moreover, Road Warrior allows travelers to share their trip information through standard social media sites, or with specific people.
Traveling with a companion has never been more convenient - a simple text containing flight and hotel details can be sent to your partner for coordinated seat bookings.
These specifics can be effortlessly shared through a private message on your preferred social media platform such as WhatsApp or Instagram.
We prioritize both, your safety and minimizing your wait time.
Keep your partner, friends, and family
informed by effortlessly sharing flight, hotel, and booking specifics using our intuitive social sharing feature.

Additionally, a concise link enables taxis to promptly check your arrival status for on-time pickups.

## Data Analytics and Reporting
Beyond trip management, Road Warrior gathers analytical data from users' trips to identify travel trends, preferences, and update frequencies.
Spark or RedShift aids in gathering and analyzing content within semi-structured distributed databases.
Furthermore, it provides personalized end-of-year summary reports, offering users a wide range of metrics concerning their travel patterns.
A scalable microservice operating in the background efficiently generates end-of-year reports for our extensive user base of 15 million.



## Conclusion
To summarize, Road Warrior is a next-generation trip management tool that offers a seamless, efficient, and user-friendly experience.
Its technical choices ensure scalability, availability, and responsiveness.
It not only organizes your travel itinerary but also provides valuable insights into your travel trends.
Road Warrior is more than just an app; it's your personal travel assistant, designed to make your journey smoother and more enjoyable.
So, the next time you find yourself overwhelmed by your travel plans, remember the Road Warrior is here to take the stress out of your journey.
Let the Road Warrior guide you through your travels, and experience the future of trip management.

## The Team
As we conclude, the Cloudeneers team expresses gratitude to O'Reilly for making this challenge a reality.
The experience has been enlightening, and we eagerly anticipate integrating these newfound insights into our daily operations.
Thanks a lot for that. The Cloudeneers.