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

In Project Ogre, players dive into a realm of fantasy where they can create unique characters, assemble powerful parties, and strategize to conquer challenges. The game boasts an array of features, including character customization, party configurations, complex spell effects, PvP battles, ELO ranking, engaging single-player campaigns, and a captivating narrative that unfolds based on character and player actions.

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

<details>
<summary>Architecture Overview</summary>
<pre>
  +-----------------+
  | User Interface  |  [Angular 16](https://example.com/ui) [PixiJS](https://example.com/ui)
  | (Angular 16,    |  
  |   PixiJS)       |  
  +-------+---------+  
          |  
          |  
          v  
  +-----------------+  
  |   API Layer     |  [C# .NET 7](https://example.com/api-docs)
  | (C# .NET 7)     |  
  +-------+---------+  
          |  
          |  
          v  
  +-----------------+  
  | Data Storage    |  
  | +-------------+ |    [Azure BLOB Storage](https://example.com/blobs)  
  | | Azure BLOB  | |    [Azure SQL](https://example.com/sql)  
  | |  Storage    | |    [Azure Cosmos DB](https://example.com/cosmos)  
  | +-------------+ |  
  | +-------------+ |  
  | | Azure SQL   | |  
  | +-------------+ |  
  | +-------------+ |  
  | |Azure Cosmos | |  
  | |   DB        | |  
  | +-------------+ |  
  +-------+---------+  
          |  
          |  
          v  
  +-----------------+  
  |Event Processing |   [Azure Event Hubs](https://example.com/event-hubs)  
  | (Azure Event    |   [Azure Databricks](https://example.com/databricks)  
  |  Hubs, Kafka    |  
  |    API)         |  
  |                 |  
  +-------+---------+  
          |  
          |  
          v  
  +-----------------+  
  | Real-time       |  
  |  Analytics      |  
  | (Azure Databricks|  
  |  with Apache    |  
  |      Spark)     |  
  +-------+---------+  
          |  
          |  
          v  
  +-----------------+  
  |Serverless       |  
  |  Functions      |   [Azure OpenAI](https://example.com/openai)  
  | (Azure OpenAI)  |  
  +-----------------+
</pre>
</details>

## Getting Started

To begin your adventure in Project Ogre, follow the steps in [Getting Started](link_to_getting_started_guide.md) to set up the game, create your character, and explore the fantastical world.

## API Documentation

The API documentation is available [here](https://example.com/api-docs) to help you understand the available endpoints and interact with the game's API.

## Contributing

We warmly welcome contributions from the community to enhance and expand Project Ogre. To learn more about how to contribute, check out our [Contribution Guidelines](link_to_contribution_guidelines.md).

## License

Project Ogre is open-source software licensed under the [MIT License](LICENSE.md).
