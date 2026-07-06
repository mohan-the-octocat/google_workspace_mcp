---
name: gmail
description: >
  Manage Gmail operations: search, read, send, draft, and manage labels/filters.
  Use for "check my email", "send an email", "find a message from X", "archive old emails", etc.
---

# Gmail

## Tool Reference

| Task | Tool |
|------|------|
| Search/find emails | `search_gmail_messages` |
| Read one email | `get_gmail_message_content` |
| Read multiple emails | `get_gmail_messages_content_batch` |
| Read a thread | `get_gmail_thread_content` |
| Read multiple threads | `get_gmail_threads_content_batch` |
| Send email (new or reply) | `send_gmail_message` |
| Create draft | `draft_gmail_message` |
| Download attachment | `get_gmail_attachment_content` |
| Add/remove labels (one) | `modify_gmail_message_labels` |
| Add/remove labels (batch) | `batch_modify_gmail_message_labels` |
| Manage labels | `manage_gmail_label` |
| List labels | `list_gmail_labels` |
| Manage filters | `manage_gmail_filter` |
| List filters | `list_filters` |

## Detailed Reference
For exact parameter names and types, see [references/gmail.md](references/gmail.md).

## Common Workflows

### Reply to an email
1. `search_gmail_messages` -- find the email
2. `get_gmail_message_content` -- read it (get `message_id` and `thread_id`)
3. `send_gmail_message` -- reply using `in_reply_to` and `thread_id`

### Process email attachments
1. `search_gmail_messages` -- find the email
2. `get_gmail_message_content` -- get attachment metadata
3. `get_gmail_attachment_content` -- download the attachment

## Tips
- Use Gmail operators in the `query` parameter (e.g., `from:boss is:unread`).
- `send_gmail_message` supports both plain text and HTML bodies.
