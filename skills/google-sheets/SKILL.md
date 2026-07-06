---
name: google-sheets
description: >
  Manage Google Sheets operations: read/write values, formatting, and conditional formatting.
  Use for "update the spreadsheet", "read data from the sheet", "format these cells", etc.
---

# Google Sheets

## Tool Reference

| Task | Tool |
|------|------|
| Read cell values | `read_sheet_values` |
| Write/append/clear values | `modify_sheet_values` |
| Format cells | `format_sheet_range` |
| Conditional formatting | `manage_conditional_formatting` |
| Get spreadsheet info | `get_spreadsheet_info` |
| Create spreadsheet | `create_spreadsheet` |
| Create sheet (tab) | `create_sheet` |
| Move rows between sheets | `move_sheet_rows` |
| List spreadsheets | `list_spreadsheets` |
| Comments | `manage_spreadsheet_comment` / `list_spreadsheet_comments` |

## Detailed Reference
For exact parameter names and types, see [references/sheets.md](references/sheets.md).

## Common Workflows

### Read and update a spreadsheet
1. `get_spreadsheet_info` -- get sheet names
2. `read_sheet_values` -- read current data
3. `modify_sheet_values` -- write updated data
4. `read_sheet_values` -- verify the update

## Tips
- `read_sheet_values` supports A1 notation (e.g., `Sheet1!A1:B10`).
- `modify_sheet_values` can append data to the end of a sheet.
