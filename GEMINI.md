# Google Workspace MCP Extension

This extension provides comprehensive control over Google Workspace services through natural language. It supports 12 different services with over 110 tools.

## Supported Services

| Service | Description |
|---------|-------------|
| **Gmail** | Search, read, send, draft, and manage labels/filters. |
| **Google Drive** | Search, read, create, copy, share, and manage permissions. |
| **Google Calendar** | List calendars, manage events, and check availability. |
| **Google Docs** | Rich document creation, editing, formatting, and markdown export. |
| **Google Sheets** | Read/write values, formatting, and conditional formatting. |
| **Google Slides** | Create presentations, extract content, and thumbnails. |
| **Google Forms** | Create forms, list responses, and manage settings. |
| **Google Tasks** | Manage task lists and tasks with hierarchy. |
| **Google Contacts** | Search, create, update, and manage contact groups. |
| **Google Chat** | List spaces, send messages, and search chat history. |
| **Apps Script** | Manage and execute Google Apps Script projects. |
| **Custom Search** | Web search via Google Programmable Search Engine. |

## Configuration

The extension requires OAuth credentials from the Google Cloud Console.

### Required Environment Variables

- `GOOGLE_OAUTH_CLIENT_ID`: Your Google OAuth client ID.
- `GOOGLE_OAUTH_CLIENT_SECRET`: Your Google OAuth client secret.

### Optional Environment Variables

- `USER_GOOGLE_EMAIL`: Default email for single-user mode.
- `GOOGLE_PSE_API_KEY`: API key for Google Custom Search.
- `GOOGLE_PSE_ENGINE_ID`: Engine ID for Google Custom Search.
- `OAUTHLIB_INSECURE_TRANSPORT`: Set to `1` for local development (HTTP).

## Skills

This extension includes granular skills for each major service. Activate a specific skill (e.g., `gmail`, `google-docs`) when focusing on a particular task to optimize context usage.

## Tool Tiers

The extension supports three tool tiers: `core`, `extended`, and `complete`.
- `core`: Essential operations (search, read, create, send).
- `extended`: Core + management (labels, folders, batch ops).
- `complete`: Full API access.

By default, all tools are enabled. You can filter tools by tier or service using command-line arguments if running as a standalone MCP server.
