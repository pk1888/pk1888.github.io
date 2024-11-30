---
title: "Obsidian - Countdowns"
date: 2024-10-30 00:00:00 +0800
categories: 
  - Obsidian
  - Dataview
tags:
  - obsidian
  - obsidian dataview
image:
  path: /assets/images/posts/obsidian.png
---

# Obsidian countdowns! 🎉 woop

Testing

---
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

// New Year Countdown
const newYear = moment(`${today.year() + 1}-01-01`, "YYYY-MM-DD");
const daysToNewYear = newYear.diff(today, 'days');
const hoursToNewYear = newYear.diff(today, 'hours') % 24;
const minutesToNewYear = newYear.diff(today, 'minutes') % 60;
const newYearContainer = this.container;
newYearContainer.createEl("h1", { text: `🎉 Countdown to New Year 🎆` });
newYearContainer.createEl("p", { text: `${daysToNewYear} days, ${hoursToNewYear} hours, and ${minutesToNewYear} minutes left!` });
---