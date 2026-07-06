---
name: google-chat
description: >
  Manage Google Chat operations: list spaces, send messages, and search chat history.
  Use for "message the team", "list my chat spaces", "search for X in chat", etc.
---

# Google Chat

## Tool Reference

| Task | Tool |
|------|------|
| List spaces | `list_spaces` |
| Get messages | `get_messages` |
| Search messages | `search_messages` |
| Send message | `send_message` |
| React to message | `create_reaction` |
| Download attachment | `download_chat_attachment` |

## Detailed Reference
For exact parameter names and types, see [references/chat.md](references/chat.md).

## Tips
- `send_message` supports threading via `thread_id`.
