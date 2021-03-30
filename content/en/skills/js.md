+++
title = "JavaScript/TypeScript"
subtitle = "Experience: 2 years"
tags = ['Languages']
date = 2020-03-20

# For description meta tag
description = "Frontend matters."

# Comment next line and the default banner wil be used.
banner = 'img/js.svg'

+++

Familiarity with JavaScript is inevitable when working with the web: you always need to keep in mind who and how on the front end will request data from your APIs. In addition, some part of the business logic sometimes leaks to the client and you need to consider this JS code as well during back-end services refactoring.

# TypeScript

I used TypeScript primarily because it allows linters (including ones on CI) and language servers to have better understanding of code and to give more contextual output when types involved. Python-like imports and classes were small bonuses as well: they are much more convenient when working in parallel with a back-end in Python, than that Lua-style which was predominant in JS before the widespread adoption of ES2015.

# GraphQL

As mentioned in the [Python](/skills/python) section, some of the services in the e-commerce platform project were developed using the GraphQL API. The "schema first" approach allowed the front-end team to define the desired API independently of the back-end team, which increased the speed of development and the quality of the API. Nevertheless, as new services appeared within the cluster, more and more independent APIs were formed, and these APIs had to be somehow combined.

Unfortunately, Python world doesn't yet have solutions for automating the creation of GraphQL gateways, so I had to use JS: [Apollo Federation](https://www.apollographql.com/docs/federation/). Not that everything happened completely automatically (you need to write additional annotations in the diagrams anyway), but the goal was achieved quite easily.

# React

I developed a small front-end for a UAV diagnostic system using React. All in all, nothing particularly outstanding: a dashboard made up of a bunch of components with graphs and telemetry that you can add, remove, and move around. But it was easy to expand and everything worked from the browser.

___
# Illustration

- Semi-transparent tesseract: the [webpack](https://webpack.js.org/) logo, if it was projected onto a plane at such an angle when all its cubes would have the same form.

- Atom in the center of the tesseract projection: [React](https://reactjs.org/).

- Background: old [JavaScript](https://www.javascript.com/) and [TypeScript](https://www.typescriptlang.org/) logos.
