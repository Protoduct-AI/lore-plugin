---
name: get-started
description: Use when the user wants to start using Lore, asks what Lore can do, or wants articles and quizzes written into or read from their Lore inbox. Explains the tools and suggests first requests.
---

# Get started with Lore

Lore is the user's private knowledge inbox, the same one they read in the Lore iPhone app. The agent researches and writes; Lore keeps and shows it, and quizzes the user so it sticks.

1. The user connects Lore and signs in with their Lore account. An active Lore Pro subscription is required. Without it, only `help` and `get_access_status` work.
2. Suggest a first request:
   - "Show my latest Lore articles."
   - "Write today's Lore article about how vaccines train the immune system, with three quiz questions."
   - "Which Lore quiz topics am I weakest at?"
3. Lore can list, search and open articles, write new articles with sources, add quiz questions, organize tags, archive articles, check weak topics, and publish a day's delivery to the user's iPhone.

Rules:
- Cite at least one real source in every article. Do not invent sources.
- Call `deliveries_commit` only once per delivery and only when the user wants it published; it sends one notification to their iPhone.
- Before archiving an article or deactivating a question, name it and get the user's confirmation.
- Lore only reads and writes the user's own articles, quizzes and tags. It does not read their email, calendar or files.
- If a tool says a subscription is required, tell the user that plainly. Do not suggest purchases or link to plans.
