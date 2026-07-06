---
name: google-drive
description: >
  Manage Google Drive operations: search, read, create, copy, share, and manage permissions.
  Use for "find a file", "upload a document", "create a folder", "share this file with X", etc.
---

# Google Drive

## Tool Reference

| Task | Tool |
|------|------|
| Search files/folders | `search_drive_files` |
| List items in folder | `list_drive_items` |
| Read file content | `get_drive_file_content` |
| Download file | `get_drive_file_download_url` |
| Create file | `create_drive_file` |
| Create folder | `create_drive_folder` |
| Copy file | `copy_drive_file` |
| Update file metadata | `update_drive_file` |
| Share / set permissions | `set_drive_file_permissions` |
| Manage access (add/remove) | `manage_drive_access` |
| Check permissions | `get_drive_file_permissions` |
| Get shareable link | `get_drive_shareable_link` |
| Check public access | `check_drive_file_public_access` |
| Import file to Google Doc | `import_to_google_doc` |

## Detailed Reference
For exact parameter names and types, see [references/drive.md](references/drive.md).

## Common Workflows

### Find and share a file
1. `search_drive_files` -- find the file
2. `manage_drive_access` -- share it
3. `get_drive_shareable_link` -- get the link

## Tips
- `create_drive_file` can create files from local content or remote URLs.
- `get_drive_file_content` can convert Docs, Sheets, and Slides to text/markdown or CSV.
