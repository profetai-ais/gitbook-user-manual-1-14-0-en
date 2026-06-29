# Audit Logs

## Introduction

Audit Logs record the operation history of important objects in the system, helping administrators track user actions such as creating, editing, and deleting items on the platform. Through Audit Logs, users can view the operation time, operator, object type, object name, and change details, making it convenient for system management, issue tracking, and data auditing.

<figure><img src="../.gitbook/assets/image (376).png" alt=""><figcaption></figcaption></figure>

## Field Descriptions

| Field | Description |
| ---- | ------------------------------------------ |
| Operation Type | Displays the type of object operated on, such as Agent, Dataset, Skill, Workflow Template, Prompt Template, etc. |
| Operation Name | Displays the name of the object operated on. Click the name to view detailed change content for that record. |
| Action | Displays the action type, such as CREATE, UPDATE, DELETE. |
| Operator | Displays the user who performed the operation. |
| Created Date | Displays the time the operation record was created. |

## Viewing Audit Log Content

<figure><img src="../.gitbook/assets/image (377).png" alt=""><figcaption></figcaption></figure>

Users can click an operation name in the list to open the Audit Log preview window and view the detailed content of that operation.

In the **Before** and **After** sections, the system displays the data differences caused by the operation. Users can use this to confirm the state of an object before and after the operation.

Different operation types display different change content. For example, a **Create** operation typically shows the newly added data; an **Update** operation shows the differences before and after modification; a **Delete** operation can be used to trace information about the deleted object.

## Search and Filter

<figure><img src="../.gitbook/assets/image (378).png" alt=""><figcaption></figcaption></figure>

Users can type a name in the search bar at the top of the page to quickly find operation records for a specific object.

The filter feature can also be used to narrow the query range, such as filtering by object type, action type, operator, or time range. Filter conditions help users quickly locate operation records for a specific period or specific user.

## Export Audit Logs

To save or further analyze audit records, users can click the **Export** button in the top-right corner to open the Export Audit Log window.

<figure><img src="../.gitbook/assets/image (392).png" alt=""><figcaption></figcaption></figure>

The following conditions can be configured before exporting:

| Field | Description |
| ------------ | ---------- |
| Operation Type | Select the object types to export |
| Action | Select the action types to export |
| Operation Name | Enter the specific object name |
| Operator | Select the user who performed the operation |
| Start Time ~ End Time | Set the time range to export |

After configuring the conditions, choose one of the following export formats:

* **Export CSV**: Exports as a CSV file, suitable for viewing or organizing with spreadsheet tools.
* **Export JSON**: Exports as a JSON file, suitable for system integration, data exchange, or technical analysis.

## Notes

Audit Logs are primarily used for tracking system operation records. The range of viewable records varies by user permissions.

If a specific record cannot be found, verify that the search criteria, filter conditions, and time range are correct. After adjusting the conditions, you can re-query or export audit records that match the criteria.
