# Slack Joke Bot — n8n Automation

A simple n8n workflow that fetches a random joke from a public API and posts it directly to a Slack channel.

## What it does

1. **Trigger** — manually started (can be swapped for a Schedule Trigger)
2. **HTTP Request** — calls `https://v2.jokeapi.dev/joke/Any` to fetch a random joke
3. **Edit Fields** — combines the joke's `setup` and `delivery` fields into a single clean message
4. **Send a message (Slack)** — posts the combined message to a Slack channel via OAuth2

## Tech used

- [n8n](https://n8n.io) — workflow automation
- [JokeAPI](https://v2.jokeapi.dev) — free public joke API
- Slack OAuth2 integration

## Setup

1. Import `slack-joke-bot.json` into your n8n instance
2. Add your own Slack OAuth2 credentials
3. Replace `YOUR_CHANNEL_ID` in the Slack node with your actual channel ID
4. Execute the workflow

## Why I built this

Second automation in my n8n learning journey — a small project to practice the core chain of **API call → data transformation → delivery**, a pattern I reuse in almost every workflow since.
