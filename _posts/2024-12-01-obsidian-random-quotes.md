---
title: "Obsidian New Year Countdown"
date: 2024-12-01 09:29:00 +0800
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

### New Year Countdown in Obsidian with DataviewJS

As we approach the end of the year, add some excitement to your Obsidian vault with a **New Year Countdown**. Using **DataviewJS** and `moment.js`, you can create a countdown timer that shows the remaining days, hours, and minutes until New Year’s Day.

![alt text](assets/images/posts/obsidian-newyear-countdown.webp)

#### Here's the code for the New Year Countdown:

```yaml
```dataviewjs
// New Year Countdown
const today = moment();
const newYear = moment(`${today.year() + 1}-01-01`, "YYYY-MM-DD");
const daysToNewYear = newYear.diff(today, 'days');
const hoursToNewYear = newYear.diff(today, 'hours') % 24;
const minutesToNewYear = newYear.diff(today, 'minutes') % 60;
const newYearContainer = this.container;
newYearContainer.createEl("h1", { text: `🎉 Countdown to New Year 🎆` });
newYearContainer.createEl("p", { text: `${daysToNewYear} days, ${hoursToNewYear} hours, and ${minutesToNewYear} minutes left!` });
```

### New Year Countdown Script Explanation

This script calculates how much time is left until the New Year and displays it in a neat format. The countdown updates in real time, keeping your notes dynamic and engaging.

#### How It Works:
1. **Set the Date**: The script sets the target date for New Year’s Day, which is always January 1 of the next year.
2. **Calculate Time Difference**: It calculates the days, hours, and minutes remaining.
3. **Display the Countdown**: The script creates two elements in your Obsidian note — a heading (`h1`) and a paragraph (`p`) — to display the remaining time.

#### Why Use This?
- **Real-time Countdown**: The countdown dynamically adjusts based on the current date, ensuring accuracy.
- **Fun Addition**: It’s a fun way to add an interactive element to your notes.
- **Customization**: You can adapt the script to count down to other special dates or milestones.

Give it a try, and start the countdown to a fantastic New Year! 🎇 