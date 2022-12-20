# Introduction

**What is an REST API?**

A REST API (also known as RESTful API) is an application programming interface (API or web API) that conforms to the constraints of REST architectural style and allows for interaction with RESTful web services. REST stands for representational state transfer and was created by computer scientist Roy Fielding.

*Analogy*: Imagine, if you will, that you are a frontend developer, and you get a project to make a calendar app for a client. Another company has already gotten started on the backend development, so you contact them to find out what HTTP requests you need to make in order to fetch, create, and delete calendar entries. They give you a list:

- To get calendar entries, send HTTP POST to `/calendar/entries/get`.
- To create a calendar entry, send HTTP POST to `/calendar/entries/create`, and include the entry details in JSON.
- To delete a calendar entry, send HTTP POST to `/calendar/entries/delete`, and send a JSON object with a single `id` key.

Fair enough. You build the frontend, you test extensively, everything works, everyone’s happy. Then, a few months later, you get a project to make a calendar app for a different client. Once again, the client had another company do the backend development, and they give you this API:

- To get calendar entries, send HTTP GET to `/calendar/loadentries`.
- To create a calendar entry, send HTTP POST to `/calendar/newentry`, and include the entry details as an XML document.
- To delete a calendar entry, send HTTP POST to `/calendar/deleteentry?id=<entry_id>`.

Basically, nothing you built for the previous app can be reused, as far as backend communication goes. **Now imagine this chaos on an industry-wide scale.**

The **greatest advantage of REST** is that of any other standard: 
- it reduces the time and effort needed to develop an API, and increases the reusability of code between apps. 
- the unified format of URI’s also opened up the door for all sorts of automation.
- the URI + method combinations are fairly intuitive, and the URI patterns are open-ended, allowing backend developers to add custom actions for various types of content if necessary.

# Prerequisites

- You need a good understanding of what APIs are in general. Then, the above introduction to REST APIs with a short analogy is fair enough as you will understand more about the architecture movinf forward.
- You will need a code editor (`VS Code` preferably) and a browser (chrome, firefox etc.) for the awesome upcoming activities.
- Install [NodeJS](https://nodejs.org/en/download/) on your system. I am using Node `v16.17.1` and npm `8.15.0`. You can check the version installed on your system by running these commands in your terminal:
    ```
    node -v
    npm -v
    ```