---
title: "Obsidian Countdowns"
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

```yaml
---
dataviewjs
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
---
```