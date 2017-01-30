# Build a Client Project

[Teachers' Project Briefs](https://docs.google.com/a/devbootcamp.com/document/d/1Kmw125hcNvyA_v4e35__TADi5NP88ELdhVfzPSlyAIc/edit?usp=sharing)

###  Stock Portfolio Manager

Tina the Trader is a celebrated 32 year old stock trader on Wall Street. She is well known in the industry as being a visionary in her trading decisions as she has generated billions of dollars in trading revenue for the companies she’s worked for, and tens of millions of dollars for her own personal portfolio. She is also notorious for being impossibly impatient and incredibly demanding. She is **_sick and tired_** of the current software she uses to manage her stock positions and would like to build her own platform. Through a huge stroke of luck, she has chosen YOU to build out this vision as per her high expectations. She is ready to pay you a __TON__ of cash for this project as long as the platform meets all of her criteria.

At a high level, this application should serve as a visual dashboard that displays all of Tina’s current stock trading positions using the most up to date stock prices. Also, it should track her total Profit and Loss (P&L) on all her positions.

__Core Goals:__
+ Has user authentication with password stored securely (bcrypt)
+ Displays all current stock positions in a Portfolio
+ Displays Current Value, Cost Basis and Total P&L for each Position
+ Displays Current Value, Cost Basis and Total P&L for total Portfolio
+ Connects with an API to retrieve most up-to-date stock pricing


__Stretch Goals:__
+ Trading: Users can add new stock positions at the most up to date price
+ Track selling: Users can track realized gains/losses (stock that they have actually sold)
+ Graphs and UI: Users can view current value of their portfolio divided up by sector in a chart
+ Graphs and UI: Users can view historical performance of positions and/or total portfolio in a chart
+ Analytics: Users can view amounts for unrealized gains/losses per stock or group of stocks
+ Analytics: Users can utilize various [prediction algorithms](https://blog.quantopian.com/common-types-of-trading-algorithms/) to determine if they should buy/sell/hold a specific stock
+ Analytics: Users can track the accuracy of the prediction algorithms they have utilized in the past (e.g. if algorithm X said to buy stock ABC on January 2, and now it’s February 2, did the algorithm succeed at predicting future performance?)
+ API integration: Users can view the recommendations of reputed ratings firms for a specific stock (e.g. Morningstar)

__Stock Trading Basics__
+ A Stock Portfolio consists of multiple Trading Positions
+ Each Trading Position will have the # of Shares, the Buy Price and the Current Price
+ The Current Value of a Trading Position is: # of Shares x Current Price
+ The Cost Basis of a Trading Position is: # of Shares x Buy Price
+ The Total P&L is: Current Value - Cost Basis
+ [Example online portfolio implementation](https://www.google.com/finance/portfolio)

__Groups__

Nick | Tony | John

Jefferson | Raji

Kevin | Kane

---

### Learning Competencies

- Interfacing with clients to determine the specification for building an application, in the form of user stories.
- Using a formal Agile group process to complete a successful development project.

### Summary

Let's put all of our knowledge thus far to the test and build someone a real web application!

The goal is for this challenge to simulate (albeit in a compressed form) the process of interacting with clients, building prototypes for them, and iterating based upon their feedback - all while working together as a team and following development and deployment best practices.

Your instructors will act as your clients throughout this project, helping you drive discovery of their requirements. The instructors will not be "difficult clients" - their goal is to help you find the right questions to ask and will respond as such. This is a low-stakes environment to practice these vital skills.

While you may have the temptation to try to throw a lot of AJAX into this application or turn it into a "single-page application," resist this temptation. There will be plenty of time for exploring JavaScript features later. Focus on defining clear routes, creating clean templates, and testing a "classic" CGI application.

Use the "DBC Rails"-preferred stack:

- Practice TDD using RSpec with `factory_girl` and `capybara`
- [Remove `turbolinks`][die-turbolinks] and `coffee-rails`

Remember, to create a new Rails application with certain features enabled / disabled, you can use [command-line switches][cls].  A good start would be `rails --help`.

### Strategy

Before you dive to deeply into the code, be clear with your team on three things:

1. Decide on your MVP
2. Break your MVP down into deliverable features

### Testing

Your app must be fully tested.  If you want to stretch yourself by TDDing your way, go for it, but timebox yourself. The goal of this is to actually build a functional and well tested app.

Additionally, since testing is such a heavy focus for this application, you should integrate [Continuous Integration][CI].  Two popular providers of CI services are [TravisCI][] and [CircleCI][].

As a bonus feature, try integrating the callback hooks between CI and [Trello][] and [Slack][] to post your CI status directly into your cards and chat..

### Pro Developer Technologies

* Track your work and user stories and their progress by means of [Trello][], [Pivotal Tracker][] or a physical card wall.
* Add continuous integration (CI) to your repo.
* Keep your team communication up and add a chat application.  Many teams, especially those that work remotely, find it helpful to use a chat environment like Slack.  Integrate this with GitHub and CI and hygeinic git behavior, you can work as well separated by miles as you might while standing in the same room together.

### Checkpoints

* Your team should produce a repo inside of your cohort's organization in GitHub
* Your first commit should be a `README.md` containing:
 * Your team name
 * Your team members' names
 * The user stories that define your MVP
* You will be demoing your MVP
 * Show us your app doing the essential work of your app
 * Show us your tests
 * Show us `git log --graph`, this should be clean
* You will be demoing your final project


[die-turbolinks]: http://blog.steveklabnik.com/posts/2013-06-25-removing-turbolinks-from-rails-4
[CI]: http://en.wikipedia.org/wiki/Continuous_integration
[TravisCI]: https://travis-ci.org/recent
[CircleCI]: https://circleci.com/
[Pivotal Tracker]: https://pivotaltracker.com
[Trello]: https://trello.com/
[Slack]: https://slack.com/
[cls]: http://en.wikipedia.org/wiki/Command-line_interface
