# Lore plugin

Connects your agent to [Lore](https://mcp.lore.protoductai.com), a private knowledge inbox app for iPhone, through Lore's hosted MCP server at `https://mcp.lore.protoductai.com/mcp`.

This plugin works in Cursor and Grok Bot. It contains one MCP server and one skill (`get-started`). It has no commands, hooks or local code.

## Requirements

- A Lore account (the one you use in the Lore iPhone app).
- An active Lore Pro subscription. Without Pro, `help` and `get_access_status` still work, and every other tool returns a short message saying a subscription is required.

## Connect

1. Install the plugin from the marketplace.
2. When the agent first calls Lore, a sign-in page opens. Sign in with your Lore account and approve access. Lore uses OAuth 2.1 with PKCE and dynamic client registration, so there is no API key to paste.
3. To disconnect, remove the plugin.

## Try it

- "Show my latest Lore articles."
- "Write today's Lore article about how vaccines train the immune system, with three quiz questions."
- "Which Lore quiz topics am I weakest at?"

## Tools

| Tool | What it does | Changes data |
|---|---|---|
| `help` | Explain what Lore can do and whether the tools are usable now | No |
| `get_access_status` | Check your subscription status | No |
| `connection_test` | Confirm the connection and record the time in the app | Yes |
| `articles_list` | List your articles | No |
| `articles_get` | Open one article | No |
| `articles_search` | Search your published articles | No |
| `articles_upsert` | Create or update one article with cited sources | Yes |
| `articles_archive` | Archive an article, or restore it | Yes |
| `quizzes_list` | List your quiz questions | No |
| `quizzes_upsert` | Add or replace one multiple-choice question for an article | Yes |
| `quizzes_deactivate` | Stop using an outdated question, keeping its answer history | Yes |
| `tags_list` | List your tags | No |
| `tags_upsert` | Create or rename a tag | Yes |
| `assets_upload` | Store one image for an article | Yes |
| `deliveries_prepare` | Start today's delivery of articles | Yes |
| `deliveries_commit` | Publish the delivery to your iPhone and send one notification | Yes |
| `review_status` | Read recent quiz answers and the topics you miss most | No |

## Privacy

Lore only reads and writes your own articles, quizzes and tags. It does not access your email, calendar, files or chat history, and it cannot send messages to anyone. Publishing a delivery may send one private notification to your own iPhone.

- Privacy policy: https://mcp.lore.protoductai.com/privacy
- Terms: https://mcp.lore.protoductai.com/terms
- Support: https://mcp.lore.protoductai.com/support (support@protoductai.com)

## License

MIT. See [LICENSE](LICENSE). The license covers the files in this repository, not the Lore service.
