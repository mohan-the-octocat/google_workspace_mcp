---
name: google-apps-script
description: >
  Manage and execute Google Apps Script projects.
  Use for "run this script", "create a new script project", "update the script code", etc.
---

# Google Apps Script

## Tool Reference

| Task | Tool |
|------|------|
| List projects | `list_script_projects` |
| Get project | `get_script_project` |
| Create project | `create_script_project` |
| Delete project | `delete_script_project` |
| Get file content | `get_script_content` |
| Update file content | `update_script_content` |
| Run function | `run_script_function` |
| Generate trigger code | `generate_trigger_code` |
| Manage deployments | `manage_deployment` / `list_deployments` |
| Versions | `create_version` / `get_version` / `list_versions` |
| Execution metrics | `get_script_metrics` |
| Process history | `list_script_processes` |

## Detailed Reference
For exact parameter names and types, see [references/apps-script.md](references/apps-script.md).

## Tips
- Use `run_script_function` to trigger custom logic already defined in Apps Script.
