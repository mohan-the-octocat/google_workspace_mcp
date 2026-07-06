---
name: google-calendar
description: >
  Manage Google Calendar operations: list calendars, manage events, and check availability.
  Use for "schedule a meeting", "what's on my calendar today?", "check if X is free", etc.
---

# Google Calendar

## Tool Reference

| Task | Tool |
|------|------|
| List calendars | `list_calendars` |
| Get events | `get_events` |
| Create/update/delete event | `manage_event` |
| Check availability | `query_freebusy` |

## Detailed Reference
For exact parameter names and types, see [references/calendar.md](references/calendar.md).

## Tips
- `manage_event` supports Google Meet integration via the `add_google_meet` parameter.
- Use `query_freebusy` to check availability across multiple calendars before scheduling.
