# Project Ogre

![Project Ogre Logo](screenshots/project_ogre_logo.png)

Welcome to Project Ogre, an epic and immersive gaming experience where you can embark on thrilling adventures, engage in intense battles, and explore a vast world of magic and mystery. With a wide array of features and limitless possibilities for character customization and exploration, Project Ogre offers an unforgettable journey for both solo players and competitive enthusiasts.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Architecture Overview](#architecture-overview)
- [Getting Started](#getting-started)
- [API Documentation](#api-documentation)
- [Contributing](#contributing)
- [License](#license)

## Introduction
### Game Summary

Welcome to **Project Ogre**, an online Strategy RPG that sets itself apart by valuing meaningful choices, trade-offs, diminishing returns, and ingenuity over the typical MMO gear treadmills or real-time strategy "actions per minute." Embrace a world of infinite complexity without the grind or APM pressure.

#### Game Mechanics

In **Project Ogre**, your decisions matter more than ever. The game is designed to emphasize the importance of thoughtful choices, where every move and action carries significant weight. Trade-offs play a crucial role in shaping your character's journey, party dynamics, and resource management. No longer will you find yourself caught in endless gear grind cycles; instead, you'll discover a deeply rewarding experience that favors intelligence and cunning over repetitive tasks.

#### Infinite Complexity

Prepare to immerse yourself in a realm of boundless complexity. **Project Ogre** thrives on providing players with infinite possibilities and intricate interactions. Embrace the challenge of navigating through a world that continuously adapts and evolves based on your decisions. Uncover the depth of the game through inventive strategies, unique character builds, and creative combinations of various game elements.

## ##No Grind or APM Pressure

Bid farewell to the days of tedious grinding and the constant pressure of actions per minute. **Project Ogre** embraces a refreshing approach that prioritizes the enjoyment of the gameplay experience. Immerse yourself in a world where tactical planning, strategy, and creative thinking are celebrated, and where every moment spent in the game feels meaningful and rewarding.

Whether you're a seasoned Strategy RPG veteran or new to the genre, **Project Ogre** welcomes you to a captivating realm where your choices shape your destiny, and where the pursuit of depth and ingenuity takes center stage.

Are you ready to embark on an epic adventure, where your intellect and creativity are your greatest assets? Join the world of **Project Ogre** today!

## Features

Project Ogre offers a rich and immersive gaming experience with a plethora of exciting features:

- **Character Customization**: Create your hero from scratch, with a variety of appearance options, attributes, and traits, ensuring a one-of-a-kind character.

- **Party Configurations**: Formulate the perfect team by selecting members from your pool of characters to create a versatile and powerful party.

- **Diverse Character Classes**: Choose from over 32 character classes, each with unique skills and abilities, shaping the way your character engages in battles.

- **Character Equipment**: Outfit your characters with a wide array of weapons, armor, and accessories, enhancing their capabilities and customizing their playstyle.

- **Procedurally-Generated Spells**: Discover an ever-expanding library of spells, generated procedurally to keep gameplay fresh and exciting.

- **Complex Spell Effects**: Unleash a myriad of spell effects, from damage over time and healing over time to buffs, debuffs, and various stat alterations, bringing depth to combat strategies.

- **Player vs Player (PvP)**: Compete against other players in thrilling PvP battles, testing your strategic prowess and character strength.

- **ELO Ranking System**: Earn and climb the ELO ranking system, showcasing your skills and achievements to the game's community.

- **Engaging Single Player Campaigns**: Embark on captivating single-player campaigns, immersing yourself in rich narratives and epic quests, tailored to your character's choices.

- **Character and Player-Specific Narratives**: Your character's actions and choices impact the unfolding narrative, making each playthrough unique and engaging.

- **Pixel Art Graphics**: Immerse yourself in the charm of pixel art, bringing a nostalgic and visually appealing experience to the game.

- **Available on Web and Mobile (PWA)**: Enjoy Project Ogre's adventures on the go with a Progressive Web App (PWA) compatible on both web browsers and mobile devices.

- **Party Formations and Character Synergies**: Experiment with different party formations and character combinations to discover powerful synergies and strategies.

- **Billions of Unique Character Combinations**: With extensive customization options, unleash your creativity to create billions of unique character combinations.

- **Dozens of Weapons and Armor Types**: Equip your characters with an impressive assortment of weapons and armor, tailoring their gear to your preferred playstyle.

Project Ogre delivers an ever-evolving world filled with epic battles, intriguing challenges, and limitless possibilities for character growth and exploration. Immerse yourself in this fantasy realm and embark on a journey that will test your tactical prowess and forge legends.

---

## Technologies Used

Project Ogre utilizes the following technologies to deliver a seamless and enjoyable gaming experience:

- Angular 16: Powering the intuitive user interface and dynamic interactions. [UI](https://project-ogre-ui.azurewebsites.net)
- PixiJS: Enabling smooth and captivating pixel art graphics rendering.
- C# .NET 7: The backbone of the API layer, providing a reliable and scalable infrastructure. [API Documentation](https://project-ogre-api.azurewebsites.net)
- Azure Services: Leveraging Azure BLOB storage, Azure SQL, and Azure Cosmos DB for data storage and management.
- Azure Event Hubs with Kafka API: Handling real-time event processing.
- Azure Databricks with Apache Spark: Generating real-time analytics and insights.
- Azure OpenAI: Dynamically creating captivating in-game content through serverless functions.
- 
```plaintext
Game Architecture

Player (via Angular App)  ---> | Azure Kubernetes Services (API Microservices) | ---> Azure SQL Database
                                 |     (Load Balanced and Traffic Managed)    | ---> Azure Storage
                                 |                                          | <--- Azure Cosmos DB   |
                                 |                                          |                         |
                                 |------------------> Azure OpenAI Service   |   Azure Functions <----|
                                 |                                          |
                                 |------------------> Azure Event Hubs (Kafka Interface)
                                                       |
                                                       V
                                                 Azure DataBricks (Apache Spark)

```

## Architectural Components

### UI (Angular App)

The front-end of the game where users interact with the game's user interface. You can access the UI by visiting [Project Ogre UI](https://project-ogre-ui.azurewebsites.net/).

### API (Azure Kubernetes Services)

The API layer consists of a set of microservices hosted on Azure Kubernetes Services (AKS) handling player interactions and data storage. To access the API, use [Project Ogre API](https://project-ogre-api.azurewebsites.net/).

### Player (via Angular App)

The Angular-based web application serves as the player's interface to the game. Players interact with the UI to view and edit characters and parties, manage their inventory, and initiate quests and PvP battles.

### Azure Kubernetes Services (API Microservices)

The API layer consists of a set of microservices hosted on Azure Kubernetes Services (AKS). These microservices handle interactions between the player's UI and various data storage components. They receive information from the Angular App related to character and party changes, inventory management, quests, and PvP battles.

### Azure SQL Database

A fully managed relational database used to store critical game-related data, including player characters, parties, inventory, and quest progress. The API microservices communicate with the database to read and update player information based on user interactions.

### Azure Storage (Azure BLOB Cold Storage)

The battle data resulting from PvP battles is stored in Azure BLOB cold storage. This data is primarily used for two purposes: the initial replay by the user to review the battle and analytics processing through Azure DataBricks.

### Azure Cosmos DB

A NoSQL database that stores graph and unstructured narrative data related to characters, players, and the game world. It captures and manages complex narrative elements and world events that evolve based on player actions.

### Azure OpenAI Service

This service enhances the game's narrative during player versus environment (PvE) questing events. Azure Functions utilize the OpenAI Service to dynamically generate and evolve the narrative based on player choices and outcomes during quests.

### Azure Functions

Azure Functions play a crucial role in handling backend tasks. They react to PvE questing events initiated by players and use the Azure OpenAI Service to generate the next increment of the narrative. Additionally, Azure Functions detect the creation of new blobs in Azure Storage (resulting from PvP battles), parse these files, and emit events into Azure Event Hubs.

### Azure Event Hubs (with Kafka interface)

Azure Event Hubs serves as a real-time data ingestion service, receiving events emitted by Azure Functions. It handles both battle data events from Azure Storage and PvE questing events generated by Azure OpenAI Service, making them available for consumption by downstream components.

### Azure DataBricks (Apache Spark)

Azure DataBricks provides an Apache Spark-based analytics platform for real-time analytics on battle data events coming from Azure Event Hubs. This analytics pipeline processes, aggregates, and derives insights from the battle data, helping to improve game balance and understand player behavior.

## Getting Started

To begin your adventure in Project Ogre, follow the steps in [Getting Started](link_to_getting_started_guide.md) to set up the game, create your character, and explore the fantastical world.
