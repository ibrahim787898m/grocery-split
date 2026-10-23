# Grocery Split

A real-time shared expense tracker for splitting grocery bills between two people.

**Live:** [grocery-split.ibrahimmustafaopu.com](https://grocery-split.ibrahimmustafaopu.com) (sign-in required — it's a private app in real use)

<!-- TODO: add a screenshot of the dashboard here: ![Dashboard](screenshot.png) -->

## Why I built it

A friend and I kept losing track of who owed what for groceries. I wanted something we could both add to from our own phones and see update straight away. We still use it every week, and using it is how I find most of the bugs.

## What it does

- Two users, each signing in with a password
- Add, edit and delete expenses; changes appear on the other person's phone in real time
- Month-by-month view with totals and a dashboard
- Automatic split: shows who owes whom and how much
- Filter entries, rename users in settings, and clear a month

## How it's built

- Plain HTML, CSS and JavaScript in a single `index.html`
- Firebase Realtime Database (JS SDK v11) for storage and live sync
- Hosted on GitHub Pages with a custom domain

## What I learned — and what I haven't solved yet

The hard part wasn't the interface, it was the data. When two people write to the database at the same time, the shape of the data decides whether anything gets lost or double-counted. My first data model didn't account for that, and the app doesn't use transactions yet. Learning to design data for concurrent writers properly is the next thing I want to get right here.

## Possible next steps

- Use Firebase transactions for updates that both users can touch
- Split the single file into separate HTML, CSS and JS files
- Add a screenshot and a demo mode so visitors can try it without an account
