---
title: "Obsidian Random Quotes"
date: 2024-12-01 11:22:00 +0800
categories: 
  - Obsidian
  - Dataview
tags:
  - obsidian
  - obsidian dataview
  - obsidian random quotes
image:
  path: /assets/images/posts/obsidian.webp
---

### Random Quotes Display in Obsidian with DataviewJS

Bring a touch of inspiration to your Obsidian vault with a **Random Quotes Generator**. Using **DataviewJS**, you can display a new, randomly selected quote every time you refresh the note. It's a simple and fun way to keep yourself motivated or entertained while using your vault.

![alt text](assets/images/posts/obsidian-random-quotes.webp)

#### Here's the code for the Random Quotes Generator:

```yaml
```dataviewjs
// Array of Quotes
const quotes = [
  "The best way to predict the future is to invent it. – Alan Kay",
  "Code is like humor. When you have to explain it, it’s bad. – Cory House",
  "Simplicity is the soul of efficiency. – Austin Freeman"
];

// Generate a Random Quote
const randomQuote = quotes[Math.floor(Math.random() * quotes.length)];

// Display the Quote
dv.container.createEl("h1", { text: `💡 Daily Quote` });
dv.container.createEl("p", { text: randomQuote });
```

### Random Quotes Script Explanation

This script is a simple yet effective way to add some flair to your notes.

#### How It Works:
- **Set the Quotes**: The script uses an array to store a list of motivational or funny quotes.
- **Random Selection**: A random quote is selected from the array using JavaScript's `Math.random()` function.
- **Display the Quote**: The quote is displayed in your note with a title and text block.

#### Why Use This?
- **Dynamic Inspiration**: Every refresh brings a new quote to keep things interesting.
- **Fun Addition**: It adds personality to your notes.
- **Easy Customization**: You can update the array with your favorite quotes or even pull them dynamically from a file.

Give this a try and brighten up your Obsidian workspace with a bit of daily inspiration! 🌟