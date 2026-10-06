# Lab 3: Unearthed Part 3 Exemplar

## Overview

In the third part of this lab, students will dip into React once again, creating a backend that can respond to API requests, as well as familiarizing themselves with the way React apps send API requests via `useEffect()` and the `async`/`await` design pattern.

This repository is the state of the project at the end of the Unit 3 lab. It is also the starting point students download for the Unit 4 lab, so the files here match what the Unit 1–3 lab steps produce.

## Project Screenshot

![screenshot of completed project](readme_screenshot.gif)

## Setup

### Dependencies

* [Vite](https://vitejs.dev/guide/)
* [React](https://www.npmjs.com/package/react)
* [React DOM](https://www.npmjs.com/package/react-dom)
* [React Router](https://www.npmjs.com/package/react-router)
* [Express](https://expressjs.com/)
* [PostgreSQL](https://www.npmjs.com/package/pg)
* [Nodemon](https://www.npmjs.com/package/nodemon)
* [CORS](https://www.npmjs.com/package/cors)
* [dotenv](https://www.npmjs.com/package/dotenv)

---

### Install Dependencies

Before installing dependencies, you will need `node` and `npm` installed globally on your machine by installing [NodeJS](https://nodejs.org/en/download/) onto your machine.

To install the client-side dependencies, run the following command in the `client` directory:

```sh
npm install
```

To install the server-side dependencies, run the following command in the `server` directory:

```sh
npm install
```

---

### Connect a Database

The server reads its Postgres credentials from `server/.env`, which is not committed. Create one from the template:

```sh
cp server/.env.example server/.env
```

Then fill in the five values from your own Render Postgres instance, found under **Connections** on the database's page in the Render dashboard. `PGHOST` is the Hostname plus your instance's region suffix, so check which region yours is in rather than assuming `oregon-postgres.render.com`.

---

### Run UnEarthed Part 3

In the `server` directory, run the following in your terminal. This drops and re-seeds the `gifts` table, then starts the API on port 3001:

```sh
npm start
```

In the `client` directory, run the following in your terminal:

```sh
npm run dev
```

Visit the web application in the browser:

```html
http://localhost:5173/
```

The client's `vite.config.js` proxies `/gifts` to the server on port 3001, so both have to be running for gifts to appear.

---

*Last Updated: October 2026*
