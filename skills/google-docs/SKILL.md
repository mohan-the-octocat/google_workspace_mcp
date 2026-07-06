---
name: google-docs
description: >
  Manage Google Docs operations: rich document creation, editing, formatting, and markdown export.
  Use for "create a new doc", "edit the proposal", "add a table to the doc", "export as markdown", etc.
---

# Google Docs

## Tool Reference

| Task | Tool |
|------|------|
| Read doc as Markdown | `get_doc_as_markdown` |
| Read doc content (raw) | `get_doc_content` |
| Create new doc | `create_doc` |
| Modify text / apply styles | `modify_doc_text` |
| Insert elements (tables, lists, breaks) | `insert_doc_elements` |
| Insert image | `insert_doc_image` |
| Create table with data | `create_table_with_data` |
| Update paragraph styles | `update_paragraph_style` |
| Find and replace | `find_and_replace_doc` |
| Inspect structure | `inspect_doc_structure` |
| Batch update (multiple ops) | `batch_update_doc` |
| Headers/footers | `update_doc_headers_footers` |
| Manage tabs | `manage_doc_tab` |
| Export to PDF | `export_doc_to_pdf` |
| List docs in folder | `list_docs_in_folder` |
| Search docs | `search_docs` |
| Comments | `manage_document_comment` / `list_document_comments` |
| Debug table structure | `debug_table_structure` |

## Detailed Reference
- **Parameters**: For exact parameter names and types, see [references/docs.md](references/docs.md).
- **Layout & Workflow**: For advanced layout patterns and formatting workflows, see [references/docs-layout-workflow.md](references/docs-layout-workflow.md).

## Common Workflows

### Create a formatted document
1. `create_doc` -- create the doc
2. `modify_doc_text` -- add text with formatting
3. `insert_doc_elements` -- add tables, lists, page breaks
4. `update_paragraph_style` -- apply heading styles
5. `get_doc_as_markdown` -- verify the result

### Edit a Google Doc
1. `get_doc_as_markdown` -- read current content
2. `inspect_doc_structure` -- find insertion points and indices
3. `modify_doc_text` / `insert_doc_elements` -- make changes
4. `get_doc_as_markdown` -- verify the result

## Tips
- Use `get_doc_as_markdown` for a high-level view of the document.
- Use `inspect_doc_structure` to find precise indices for insertions and formatting.
