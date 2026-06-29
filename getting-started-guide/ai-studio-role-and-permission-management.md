---
description: The features and operations visible to users in AI Studio depend on the role assigned to their account.
---

# AI Studio Roles and Permissions

## **Role Types in AI Studio**

The system has three default role types:

* **AI Studio Administrator:** Can browse all feature menus on the platform and grant other users advanced operational permissions for Knowledge Base and Agent features.
* **AI Studio Collaborator:** Can browse the Knowledge Base, Capabilities, Analytics, Templates, and Agent feature menus on the platform to create document knowledge bases and Agents for different domains and scenarios.
* **AI Studio User:** A general user within the organization who can browse the Knowledge Base, Templates, and Agent feature menus on the platform.

### **Role Comparison**

<table data-full-width="false"><thead><tr><th>Module Level 1</th><th>Module Level 2</th><th>AI Studio Administrator</th><th>AI Studio Collaborator</th><th>AI Studio User</th></tr></thead><tbody><tr><td><strong>Workspace</strong></td><td></td><td>O</td><td>O</td><td>O</td></tr><tr><td><strong>Agent</strong></td><td></td><td>O</td><td>O</td><td>O</td></tr><tr><td><strong>Knowledge Base</strong></td><td></td><td>O</td><td>O</td><td>O</td></tr><tr><td><strong>Capabilities</strong></td><td>Skills</td><td>O</td><td>O</td><td>X</td></tr><tr><td></td><td>MCP</td><td>O</td><td>O</td><td>X</td></tr><tr><td><strong>Templates</strong></td><td>Workflow</td><td>O</td><td>O</td><td>O</td></tr><tr><td></td><td>Prompt</td><td>O</td><td>O</td><td>O</td></tr><tr><td><strong>Analytics</strong></td><td>Reports</td><td>O</td><td>O (own only)</td><td>O (own only)</td></tr><tr><td></td><td>Work Management</td><td>O</td><td>X</td><td>X</td></tr><tr><td></td><td>Audit Logs</td><td>O</td><td>X</td><td>X</td></tr><tr><td><strong>System Settings</strong></td><td>Models</td><td>O</td><td>X</td><td>X</td></tr><tr><td></td><td>Quota</td><td>O</td><td>X</td><td>X</td></tr><tr><td></td><td>Configuration</td><td>O</td><td>X</td><td>X</td></tr><tr><td></td><td>Secret Key Management</td><td>O</td><td>X</td><td>X</td></tr><tr><td></td><td>Label Management</td><td>O</td><td>X</td><td>X</td></tr></tbody></table>

> Note: The Reports section under Analytics is accessible to all roles, but only AI Studio Administrators can view usage records for all accounts.
