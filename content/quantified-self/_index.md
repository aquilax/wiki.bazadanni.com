---
title: "Quantified self tools"
date: 2019-04-06T05:22:26+01:00
route: "quantified-self"
---

# Useful quantified self tools

## Money

### Accounting

[Plain Text Accounting](https://plaintextaccounting.org/) does a great job of outlining the tools available for handing accounting through plain text files. I personally have been using [ledger](https://www.ledger-cli.org/) for the last five years and am quite happy with it.

## Nutrition

### Calorie counting

[hranoprovod-cli](https://github.com/aquilax/hranoprovod-cli/) is a tool, inspired by Ledger, which I am using since `2011/07/17`. It uses two text files, one with "recipes" and one with food log. Given that those are properly maintained, one can generate different reports for random period with console and optional cvs output.

## Health

### Merki

[merki](https://github.com/aquilax/merki) is small command-line tool I wrote to keep track of health measurements. It's very simple to use and keeps all the data in tab separated timestamped text file.

## Life

### Biograph

[Biograh](https://github.com/aquilax/biograph) is inventory tool for one's life. It's similar to [devotees/biograph](https://github.com/devotees/biograph) but with text output. I use it to track places I've lived, travels I've done, stuff I've bought a.s.o.

## General

### Dashboard

My approach to dashboard is highly pragmatic. Most of the tools I use can produce some form of parse-able text and the data is kept locally in a git repository. A dead simple php script [me-report](https://github.com/aquilax/me-report) runs every hour against a template and executes all the pre-defined commands in the template, replacing them with the output of the command.

That output is caught by a js script on the page which turns the data into charts, using [charts.js](https://www.chartjs.org/)

The sections I have in my current report are:

* QOTD - using linux's [fortune](https://en.wikipedia.org/wiki/Fortune_(Unix)) utility with custom quotes database
* Diary - embedding the [vimwiki](https://github.com/vimwiki/vimwiki)'s diary entry for yesterday;
* Pending tasks in TaskWarrior - summary of the top priority tasks in [taskwarrior](https://taskwarrior.org/)
* Nutrition - all nutrition data comes from [hranoprovod-cli](https://github.com/aquilax/hranoprovod-cli/)
  * Yesterday - full nutrition report for yesterday
  * Today  - full nutrition report for yesterday
  * Yesterday kcal - kcal by food sorted desc for yesterday
  * Today kcal - kcal by food sorted desc for today
  * Yesterday carb - g carbs by food sorted desc for yesterday
  * Today carb - g carbs by food sorted desc for today
* Nutrition sorted (7 days)
  * Calories - kcal by food sorted desc for the last 7 days
  * Carbs - g by food sorted desc for the last 7 days
  * Fat - g by food sorted desc for the last 7 days
  * Protein - g by food sorted desc for the last 7 days
* Nutrition tree (7 days)
  * Calories - kcal grouped by food group
  * Carbs - g grouped by food group
  * Fat - g grouped by food group
  * Protein - g grouped by food group
* Nutrition charts
  * Calories - chart for last 3 months kcal per day
  * Carbohydrates - chart for last 3 months g per day
  * Fat - chart for last 3 months g per day
* Health - most health reports come from the merki tool
  * Latest health readings - latest 10 entries in the merki log
  * Weight chart - weight chart from hranoprovod-cli kg for last three months by day
  * Steps chart - number of steps chart from hranoprovod-cli for last three months by day (importing data from Google Fit, which get synced with MiBand gen3)
  * Pushups chart - number of pushups by day for the last three months
  * Pulse graph - average pulse measurements per day for the last three months
  * Blood pressure, high - average blood pressure high per day for the last three months
  * Temperature graph - average body temperature per day for the last three months
  * Latest medicines taken - last ten entries for medicines taken
  * Latest health measurements - report of all latest measurements values by type of measurement

* Finance - data comes from ledger
  * Top expenses for the last 30 days period
  * Top expenses for the previous 30 days period
  * Top level accounts for the last 30 days
  * Top level accounts for the previous 30 days
  * Transaction totals for last two weeks
  * Weekly expenses
  * Weekly expenses - Goods
  * Monthly expenses
  * Monthly expenses - Goods
  * Monthly expenses - Services
  * Monthly expenses - Transport
  * Monthly taxes
  * Yearly expenses
  * Yearly taxes
* Capital

* Latest website visits - Report from [TopSiteCounter](http://topsitecounter.appspot.com/)
* Bookmarks - Latest 30 bookmarked websites from Chrome
* Analytics - Report for difference between Google Analytics reports between the latest two dates. Doing this semi-automatically.
* Biograph - Report from biograph for the state of my life as of today
