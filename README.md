<img src="banner.svg" alt="Daniel Maymon Ramon - Backend & AI Engineer" width="100%">

Backend & AI engineer. I build agents, and then I build something that shows me what the agent actually did, because an LLM saying "done" doesn't mean much.

These days most of my time goes into agents running on a self-hosted OpenClaw server (one of them answers baby sleep questions in my family's Telegram group), and tools for reading their traces.

## Rank Air

[rank-air.com](https://www.rank-air.com/) ([code](https://github.com/Daniel1Maymon/israel-flights-etl)) - compares how airlines actually perform at Ben Gurion (delays, cancellations), with up to a year of history. It pulls the official flight data from data.gov.il every 15 minutes into Postgres, and serves it through FastAPI to a React dashboard.

You can also just ask it things, like "which airline should I fly to Paris and why?", in Hebrew or English. The LLM never touches the database directly: common questions run through queries I wrote and reviewed, and anything else goes through a read-only DB user plus a SQL validator that only lets a single SELECT through.

## Agents

- [run-investigation-agent](https://github.com/Daniel1Maymon/run-investigation-agent) - give it a run ID from another agent and it goes through the trace and tells you if the task really got done, and if not, where it broke. Python, FastAPI, OpenRouter.

## Seeing what agents did

- [openclaw-trace-viewer](https://github.com/Daniel1Maymon/openclaw-trace-viewer) - shows the full context that went into every model call in a run, plus the tool calls, failures and cost. It reads the files OpenClaw already writes, so nothing gets installed on the server.
- [claude-live-dashboard](https://github.com/Daniel1Maymon/claude-live-dashboard) - a terminal dashboard for all my running Claude Code sessions. Catches the one that's stuck calling the same tool over and over, or whose context quietly blew up.

## Other stuff

- [writing-assistant](https://github.com/Daniel1Maymon/writing-assistant) - my own Grammarly for macOS, in Swift. Spelling is checked locally with Harper, and an LLM catches sentences that are wrong even when every word is spelled right.
- [dev-dispatch](https://github.com/Daniel1Maymon/dev-dispatch) and [claude-usage-menubar](https://github.com/Daniel1Maymon/claude-usage-menubar) - small tools I use every day with Claude Code.
- [ApartmentHunterBot](https://github.com/Daniel1Maymon/ApartmentHunterBot) - scraped Facebook groups for apartments back when I was looking for one. Still my most starred repo.

Usually working in:

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white) ![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Swift](https://img.shields.io/badge/Swift-F05138?style=for-the-badge&logo=swift&logoColor=white)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/daniel-maymon-ramon/) [![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:daniel1maymon@gmail.com)
