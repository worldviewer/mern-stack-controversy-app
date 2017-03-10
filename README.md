# MERN Stack Wrapper for the Controversy App

The idea here is to use a MongoDB/Express/React/Node hackathon starter wrapper to add basic routing, database, authentication, account management, testing and deployment functionality to the existing react-worldviewer-prototype.

## The Big Picture

There are currently a few repositories related to this Controversies of Science project, so it might help to run through how they all relate to one another here, since this will be where we will bring them all together.

The [Controversies of Science](https://plus.google.com/collection/Yhn4Y) collection is a set of infographics and select reading materials that are designed to teach the patterns of scientific controversies.  The collection currently stands at almost 200 controversy cards which span 6 main categories:

- *ongoing* - Recent, ongoing controversies
- *historical* - Controversies possibly still at play, but more historical in nature
- *person* - Some people you should know about + character studies
- *reform* - Relevant to academic reform and redesigning scientific discourse
- *critique* - The best critical commentary ever published for modern science
- *thinking* - How to think like a scientist about controversies

The [react-worldviewer-prototype](https://github.com/worldviewer/react-worldviewer-prototype) repository is where I am currently experimenting with adding animation and interactivity to the Controversies of Science controversy cards infographics.  Although the goal is to experiment with new interactions and animations for each card in the collection, the initial goal is to identify how to accommodate all of those variations with a single data model and architecture.

Of particular concern with this repository is what happens on the canvas background for each graphic.  A pattern which will be consistent for all of these controversy cards will be that the background will be deep-zoomable.  This canvas is where I want to locate the crowdsourcing activities for each controversy, but it remains an open question what collaboration at this level should actually look like.

I'll also eventually be experimenting in this repository with a variety of slideshows and options for tracking user engagement with controversies.

The [controversy-api-mongodb](https://github.com/worldviewer/controversy-api-mongodb) repository houses the database and seed scraper script to populate the Controversies of Science API from the G+ collection.  At the moment, that data is being pulled into the react-worldviewer-prototype frontend from a Usergrid Apigee backend.  The intention is to port that over to MERN stack on AWS.

The repository you're looking at here is where I will concentrate those efforts.  I want to use this repo to figure out what technologies and architecture I should be going with.

## Repositories

My starting point is to consider some sort of aggregation/selection of these three hackathon starters, with an initial focus on the first ...

(1) Megaboilerplate Starter

    http://megaboilerplate.com/
    Node.js + Express.js (w/ PM2) + Bootstrap + Sass + React/Redux (w/ Redux DevTools) + Jade + Webpack + MongoDB + Auth via Email/Facebook/Google/Twitter/Github.

(2) Selections From

    https://github.com/reactGo/reactGo
    Your One-Stop solution for a full-stack app with ES6/ES2015 React.js featuring universal Redux, React Router, React Router Redux Hot reloading, CSS modules, Express 4.x, and multiple ORMs.

(3) Selections From

    https://github.com/sahat/hackathon-starter
    Hackathon Starter: A kickstarter for Node.js web applications

(4) Selections From

    https://github.com/MattMcFarland/reactathon
    boilerplate w/ React, Relay, React-Router, SSL, Express and Passport.
