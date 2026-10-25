# CS 230: Draw It or Lose It Software Design

This repository contains my completed software design document for The Gaming Room's *Draw It or Lose It* application. The project focuses on designing a web-based version of an existing Android game that can support players using different devices and operating systems.

## Software Design Document

[View the completed software design document](./CS%20230%20Project%20Three%20-%20William%20Burns.docx)

## Project Reflection

### Briefly summarize The Gaming Room client and their software requirements. Who was the client? What type of software did they want you to design?

The Gaming Room was the client for this project. The company wanted to expand its Android game, *Draw It or Lose It*, into a web-based application that people could access from different operating systems and devices. The software needed to support multiple games, teams, and players while keeping the information organized. Each game, team, and player needed a unique identifier, and the application had to prevent duplicate game and team names. The design also needed to account for multiple users accessing the game over a network.

### What did you do particularly well in developing this documentation?

I think I did particularly well explaining how the application's requirements connected to its class structure and platform choices. The UML diagram showed how the Entity, Game, Team, Player, and GameService classes worked together, including the use of inheritance and the Singleton design pattern. I also compared several operating platforms rather than choosing one without justification. Looking at compatibility, scalability, and cost helped me explain why Linux was a practical choice for hosting the game.

### What about the process of working through a design document did you find helpful when developing the code?

Working through the design document helped me understand how the different parts of the application needed to fit together. The domain model made the relationships between games, teams, and players easier to follow, while the requirements gave me specific behaviors to check in the code. For example, the design clarified why shared properties belonged in the Entity class and why GameService needed to use a single instance. Having those decisions documented made it easier to review the program's structure and keep the code aligned with the requirements.

### If you could choose one part of your work on these documents to revise, what would you pick? How would you improve it?

I would expand the distributed systems portion of the design. My document discusses network connections, server availability, backups, and the possibility of adding server capacity, but I could provide more detail about how the application would handle many players interacting at the same time. I would improve this section by describing how shared game information would stay consistent, what would happen when a player lost their connection, and how multiple servers might coordinate as the application grew.

### How did you interpret the user's needs and implement them into your software design? Why is it so important to consider the user's needs when designing?

I started with the client's main needs: broader device support, organized game information, and reliable access for multiple players. I reflected those requirements in the Java class design by giving games, teams, and players unique identifiers, checking for duplicate names, and using GameService to manage active games. For the proposed web version, I recommended a Linux server with browser-based access so different client platforms could use the same application. Considering user needs is important because a design can be technically sound but still fail if it does not solve the problems people actually have.

### How did you approach designing software? What techniques or strategies would you use in the future to analyze and design a similar software application?

I approached the project by identifying the requirements first, organizing the main objects and their relationships, and then comparing possible operating platforms. UML helped me visualize the class structure, and evaluating Linux, Windows, macOS, and mobile devices helped me consider the larger environment where the software would run. In future projects, I would continue using requirements analysis and diagrams, but I would also create small prototypes and test cases earlier in the process. Testing situations such as duplicate names, simultaneous users, and interrupted connections would help me find design problems before they became more difficult to fix.
