# Hybrid

My definition of hybrid is the use of Native navigation chrome/controls/header/side-menu, but present the screen with a web view and leverage HTML/JavaScript/CSS. I am a big fan of hybrid approaches with a few guiding principles. But first, a little history. 

Several years ago, I was responsible for estimating the time and cost to deliver IT projects. This was a time when the team had to support web, feature-web (no JavaScript - _think Nokia, Ericsson feature phone web browsers_), native apps on Blackberry, Windows Phone, Android, and iOS (iPhone and iPad). Estimates for web projects that needed 500 hours to deliver, quickly became exponentially more complex and costly. For the sake of sanity, I would always argue for web-first and quickly became a fan of [responsive web design](https://alistapart.com/article/responsive-web-design). 

Thankfully, the IT world has reduced it's complexity to the 3 pillars - web, Android, and iOS. 

My guiding principle for leveraging hybrid is based on the following: 

* **Not a high usage feature:** When app users infrequently use a feature, then use the web. If using RWD principles, then we can have 1 solution work across all 3 pillars.
* **Speed to market:** Building 1 solution in web should take less resources and time to deliver. 
* **A/B Feature testing:** It is laborious to bake in A/B experiences into a native app. This requires a significant amount of coordination, controls, development, testing, and code clean up after a decision is made. We can build A/B experiences in HTML/JS/CSS and build the winner in native if warranted. 

Conversely, we need to stick with native screens for high usage, front-door, key feature experiences. HTML/JS/CSS performance continues to improve due to solid hardware and software maturity but native screen experiences will always be several steps ahead, providing crisp, creative, and high responsive experiences. 

[Previous](03_uidesign.md) | [Next](05_healthcheck.md)