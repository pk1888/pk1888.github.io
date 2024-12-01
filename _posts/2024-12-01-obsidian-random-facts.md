---
title: "Obsidian Random Facts"
date: 2024-12-01 13:43:00 +0800
categories: 
  - Obsidian
  - Dataview
tags:
  - obsidian
  - obsidian dataview
  - obsidian random facts
image:
  path: /assets/images/posts/obsidian.webp
---
### Random Space Facts in Obsidian with DataviewJS

Add some excitement to your Obsidian vault by displaying a **random fact** each time you view your note. Using **DataviewJS**, you can create a dynamic block that shows a random space fact whenever you open your note.

![alt text](assets/images/posts/obsidian-random-facts.webp)

#### Here's the code for the Random Space Facts:

```yaml
```dataviewjs
// Space Facts Array
const spaceFacts = [
    "A day on Venus is longer than a year on Venus.",
    "There are more stars in the universe than grains of sand on all the Earth's beaches.",
    "Neutron stars are so dense that a teaspoon of their material would weigh about 6 billion tons.",
    "The largest volcano in the solar system, Olympus Mons, is on Mars.",
    "A solar flare can release as much energy as the Sun does in 24 hours.",
    "Saturn's moon Titan has lakes and rivers of liquid methane.",
    "Jupiter's Great Red Spot is a massive storm that's been raging for over 350 years.",
    "The first living creatures to orbit the Earth were fruit flies.",
    "A full NASA space suit costs about $12 million.",
    "The largest known star, UY Scuti, could fit 1,700 of our suns inside it.",
    "A day on Mercury is twice as long as its year.",
    "The Hubble Space Telescope has taken some of the most detailed images of deep space.",
    "The Milky Way galaxy is on a collision course with the Andromeda galaxy.",
    "Astronauts' height can increase by up to 2 inches in space due to the lack of gravity.",
    "Saturn's rings are made up of billions of ice and rock particles.",
    "There is a planet made of diamond, 55 Cancri e, located 40 light years from Earth.",
    "Black holes are regions of space where gravity is so strong that not even light can escape.",
    "The first human to walk on the Moon, Neil Armstrong, left behind a footprint that will last millions of years.",
    "The largest moon of Neptune, Triton, orbits the planet in the opposite direction of the planet's rotation.",
    "The Sun is about 109 times the size of Earth."
];

// Get a random space fact
const randomFact = spaceFacts[Math.floor(Math.random() * spaceFacts.length)];

// Display the random space fact
const container = this.container;
container.createEl("h1", { text: `🌌 Random Space Fact 🌠` });
container.createEl("p", { text: randomFact });
```
### Random Space Facts Script Explanation

This script displays a **random space fact** each time you open your Obsidian note, adding a fun and dynamic element to your vault. It will show one fact at a time, and you can refresh the page to get a new one.

#### How It Works:
1. **Create the Facts Array**: The script contains an array of space-related facts. 
2. **Random Fact Selection**: It selects a random fact from the array each time the note is viewed.
3. **Display the Fact**: The script creates two elements in your Obsidian note — a heading (`h1`) and a paragraph (`p`) — to display the randomly selected space fact.

#### Why Use This?
- **Ever-changing Content**: Each time you view the note, a new random space fact is displayed, keeping things interesting.
- **Educational and Fun**: A great way to add some learning and fun to your notes, all while exploring space-related trivia.
- **Customization**: You can easily replace the facts in the array or adapt the script to show facts about any other topic you prefer.

Give it a try and enjoy your dynamic space facts! 🚀🌟