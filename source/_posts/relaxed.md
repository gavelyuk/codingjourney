---
title: ReLaXed SWOT and first touch
date: 2018-06-09 12:56:16
tags: relaxed analisis comparation benefits
---
Based on chrome puppeteer, ReLaXed creates PDF documents interactively using HTML or Pug Pug (a shorthand for HTML). It allows complex layouts to be defined with CSS and JavaScript, while writing the content in a friendly, minimal syntax close to Markdown or LaTeX.

Main advantages of use ReLaXed to use PUG&SCSS templates for candy like pages and hacks with Puppeteer to create page on client side to decrease network usage. Relaxed gives you to use Markwown or LaTeX for clear content and abilities to define Page Footer and Header and reuse it but looks like the last one still not working properly.
It mean main libraries is build in browser and server generated only styles and content and user compile PDF page accordingly to view area of the screen and addition parameters.
All files: styles and content according KISS stored in most compact, easy and common format and all graphics goes to SVG by charts.js, Vega-Lite a concise JSON graphic, Mermaid flowcharts, Flowchart.js plots.
https://github.com/RelaxedJS/ReLaXed

### ReLaXed swot
|Strengths	| Opportunities|
|-|-|
|Lightweight      |Small network usage footprint|
|Extendable       |Stable firefox, safari, ie, edge versions|
|Free|Become kind of standard|
|Optimized||
|Simple (Markdown and LaTeX)	|_|

|Weaknesses	| Treats|
|-|-|
|Still in Development|Difficulties with mobile segment|
|Development as extend functionality|Small amount of themes|
|Learn structure|Bugs|
|Properly working only in Chrome|Only 4 key persons|
|Difficult to host on EC2 [Read more HERE](https://mockingbot.com/posts/run-puppeteer-chrome-headless-on-ec2-amazon-linux)|_|


#### Stranghts&Opportunities:
User side creation of rendered PDF’s (server generates html) it means significant reduce on the traffic and loading times.
Possible to extend by development (plugins is still not available) to reuse any part of code.
Firefox looks like able to handle client side renderer as well as Chrome, so remain IE and EDGE and of course mobile browsers.
Simple for data storage, understandable for average user.

#### Weaknesses&Treats:
For hosting good understanding require how to use ReLaXed, it is not only npm i -g relaxedjs extra libraries is required, as well as experienced administrator to find out which libraries is missing, etc.
Luck of plugins and themes, so it mean – development required, as company manager you must accept fact it can be as with first Angular, can be critical changes in the next versions and it can touch this segment.
Still a lot of bugs and luck of good polished documentation same as individuals able to learn and share their knowledge, difficult for average user to understand what is framework is and main framework benefits and application.

### Competitors:


1.	jsPDF
https://parall.ax/products/jspdf - creates pdf files from JavaScript source.
 * Simple to create, small content footprint.
 * Required JavaScript knowledge users, 2Mbytes library.


2.	PDFjs
 Portable Document Format (PDF) viewer that is built with HTML5 , used as client-server , library by Mozilla.
 * Simple to create, big content footprint.
 * Default build in Firefox viewer .


3.	Puppeteer
Puppeteer Chrome ( high-level API to control headless Chrome or Chromium over the DevTools Protocol) https://github.com/GoogleChrome/puppeteer
Puppeteer supported in chrome headless mode, in headless mode it means no user interface is available, also in this mode plugins and extensions not available. It is still possible to switch non headless mode, but plugins and extensions will not works.
•	Generate screenshots and PDFs of pages.
•	Crawl a SPA and generate pre-rendered content (i.e. "SSR").
•	Automate form submission, UI testing, keyboard input, etc.
•	Create an up-to-date, automated testing environment. Run your tests directly in the latest version of Chrome using the latest JavaScript and browser features.
•	Capture a timeline trace of your site to help diagnose performance issues.
Give it a spin: https://try-puppeteer.appspot.com/
 * Simple to create, any page to pdf.
 * Default build in Chrome  and Chromium as a part of development tools .


4.	Puppeteer Firefox
(somehow linked to Puppeteer Chrome )
https://github.com/GoogleChrome/puppeteer


5.	Puppeteer-FX
(independent developments without support PDF, probably in the future).
https://github.com/autonome/puppeteer-fx
 * npm module alternative to Puppeteer Chrome but design for Firefox.
 * Luck of functionality, luck of documentation .


6.	SeleniumHQ
(similar to Selenium 1.0 + WebDriver = Selenium 2.0) - libraries that enable and support the automation of web browsers .
https://github.com/SeleniumHQ
 * Independent cross platform and cross browser libraries.


7.	PhantomJS
development is suspended until further notice.
PhantomJS is a headless web browser scriptable with JavaScript. It runs on Windows, macOS, Linux, and FreeBSD.
 * Independent cross platform and cross browser libraries.
 * Deprecated project .

### First start with ReLaXed:
