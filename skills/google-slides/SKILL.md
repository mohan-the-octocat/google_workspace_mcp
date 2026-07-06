---
name: google-slides
description: >
  Manage Google Slides operations: create presentations, extract content, and thumbnails.
  Use for "create a slide deck", "get text from slide 3", "generate a thumbnail of the slide", etc.
---

# Google Slides

## Tool Reference

| Task | Tool |
|------|------|
| Get presentation | `get_presentation` |
| Get specific slide | `get_page` |
| Get slide thumbnail | `get_page_thumbnail` |
| Create presentation | `create_presentation` |
| Batch update | `batch_update_presentation` |
| Comments | `manage_presentation_comment` / `list_presentation_comments` |

## Detailed Reference
For exact parameter names and types, see [references/slides.md](references/slides.md).

## Tips
- `batch_update_presentation` is powerful for creating complex slide layouts programmatically.
