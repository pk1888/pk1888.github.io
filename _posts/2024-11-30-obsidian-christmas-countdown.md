---
title: "Obsidian Christmas Countdowns"
date: 2024-10-30 00:00:00 +0800
categories: 
  - Obsidian
  - Dataview
tags:
  - obsidian
  - obsidian dataview
  - obsidian countdown
image:
  path: /assets/images/posts/obsidian.webp
---

### Christmas Countdown in Obsidian with DataviewJS

As the holidays draw near, you can bring some festive spirit to your Obsidian vault with a **Christmas Countdown**. By using **DataviewJS** and `moment.js`, you can easily create a countdown timer that will display the number of days, hours, and minutes left until Christmas.

![alt text](assets/images/posts/obsidian-christmas-countdown.webp)

#### Here's the code for the Christmas Countdown:

```yaml
```dataviewjs
// Christmas Countdown
const today = moment();
const christmas = moment(`${today.year()}-12-25`, "YYYY-MM-DD");
if (today.isAfter(christmas)) christmas.add(1, 'year');
const daysToChristmas = christmas.diff(today, 'days');
const hoursToChristmas = christmas.diff(today, 'hours') % 24;
const minutesToChristmas = christmas.diff(today, 'minutes') % 60;
const christmasContainer = this.container;
christmasContainer.createEl("h1", { text: `🎄 Countdown to Christmas 🎅` });
christmasContainer.createEl("p", { text: `${daysToChristmas} days, ${hoursToChristmas} hours, and ${minutesToChristmas} minutes left!` });
```

### Christmas Countdown Script Explanation

This script calculates how much time is left until Christmas and displays it in a neat format. The countdown is updated in real time, and you can even adjust the code to show the countdown for other events, like New Year’s!

#### How It Works:
- **Set the Date**: The script sets the target date for Christmas, and if today is already past Christmas, it automatically shifts the countdown to next year.
- **Calculate Time Difference**: It calculates the days, hours, and minutes remaining.
- **Display the Countdown**: The script creates two elements in your Obsidian note — a heading (`h1`) and a paragraph (`p`) — to display the remaining time.

#### Why Use This?
- **Real-time Countdown**: The countdown dynamically adjusts based on the current date, ensuring it’s always accurate.
- **Fun Addition**: Adding little scripts like this one makes your notes more interactive and fun!
- **Customization**: You can tweak the script for other important events or even use different date formats.

Give it a try, and feel free to add a personal touch to your countdown! 🎉
