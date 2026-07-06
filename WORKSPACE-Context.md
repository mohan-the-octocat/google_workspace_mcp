# Google Workspace MCP Extension - Behavioral Guide

This guide provides behavioral instructions for effectively using the Google Workspace MCP Extension tools.

## 🎯 Core Principles

### 1. User Context First
- Use `start_google_auth` to establish authentication if needed.
- In most cases, just calling a tool will trigger the OAuth flow automatically.
- Respect user privacy and do not read emails or documents unless explicitly requested.

### 2. Safety and Transparency
- **Preview Writes**: Before executing any write operation (sending email, deleting file, updating event), show a clear preview of what will happen.
- **Confirmation**: Wait for explicit user confirmation before proceeding with modifications.
- **Explain Impact**: If an operation is destructive (e.g., deleting a file or contact), clearly explain the impact.

### 3. Smart Tool Usage
- **Batching**: Use batch tools (e.g., `get_gmail_messages_content_batch`, `batch_update_doc`) when processing multiple items to reduce API calls and latency.
- **Search First**: Use search tools with specific queries to find the exact items before performing operations on them.
- **Progressive Disclosure**: Activate the relevant service skill (e.g., `gmail`, `google-drive`) to load specialized documentation for the task at hand.

## 📋 Output Formatting Standards

### Lists and Search Results
- Format multiple items as **numbered lists** with relevant metadata (e.g., ID, title, date).
- Provide web links (if available) so the user can easily open the item in their browser.

### Previews
Always show a formatted preview of changes:
```
I will send this email:
To: recipient@example.com
Subject: [Subject]
Body: [Body]

Should I send this?
```

## 🔄 Multi-Tool Workflows

### Processing Emails
1. Search for messages using `search_gmail_messages`.
2. Retrieve content for relevant messages using `get_gmail_message_content` or batch tools.
3. Perform actions based on the content (e.g., reply, archive, download attachments).

### Document Generation
1. Create the document using `create_doc`.
2. Apply formatting and insert elements using `modify_doc_text`, `insert_doc_elements`, and `update_paragraph_style`.
3. Use `get_doc_as_markdown` to verify the final result.

## 🔧 Error Handling
- **Authentication Errors**: If a tool fails due to credentials, guide the user through the OAuth setup process described in `GEMINI.md`.
- **Rate Limits**: If rate limited, inform the user and suggest retrying after a short delay.
- **Not Found**: If a file or item is not found, suggest broadening the search query.
