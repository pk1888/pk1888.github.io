---
title: "Obsidian Personalized Greeting"
date: 2024-12-01 13:58:00 +0800
categories: 
  - Obsidian
  - Dataview
tags:
  - obsidian
  - obsidian dataview
  - obsidian personalized greeting
image:
  path: /assets/images/posts/obsidian.webp
---

### Personalized Greeting in Obsidian with DataviewJS

Add a **personalized greeting** to your Obsidian vault that changes based on the time of day. With **DataviewJS**, you can create a greeting that includes your name and adjusts according to whether it's morning, afternoon, or evening.

#### Here's the code for the Personalized Greeting:

```yaml
```dataviewjs
// Set the user's name
const userName = "Paul"; // Change this to your name

// Get the current hour
const hour = new Date().getHours();

// Determine the greeting based on the time of day
let greeting = "";
if (hour < 12) {
    greeting = "Good morning";
} else if (hour < 18) {
    greeting = "Good afternoon";
} else {
    greeting = "Good evening";
}

// Display the personalized greeting
const container = this.container;
container.createEl("h1", { text: `${greeting}, ${userName}! 👋` });
container.createEl("p", { text: "Welcome to your Obsidian vault!" });
```

### Personalized Greeting Script Explanation

This script displays a **personalized greeting** when you open your Obsidian note, making your vault feel more interactive and welcoming. It can greet you by name and adjust the greeting based on the time of day (morning, afternoon, or evening).

#### How It Works:
1. **Set the User's Name**: The script greets you by your name. You can customize the `userName` variable to your own name.
2. **Time-Based Greeting**: The script checks the current time and adjusts the greeting based on the time of day.
3. **Display the Greeting**: The script creates two elements in your Obsidian note — a heading (`h1`) and a paragraph (`p`) — to display the personalized greeting.

#### Why Use This?
- **Personalized Experience**: Adds a friendly, customized greeting every time you open your note.
- **Time-Based Adjustments**: The greeting dynamically changes depending on the time of day, making your vault feel more alive.
- **Customization**: You can easily change the greeting or adjust the logic for different times of the day.

Give it a try and enjoy a warm, personalized greeting each time you open your vault! 👋✨