---
description: Work Management is used to centrally manage and track Jobs running under an Agent, providing a clear view of each job's status, ownership, and progress changes.
---

# Work Management

## Introduction

<figure><img src="../.gitbook/assets/image (215).png" alt=""><figcaption></figcaption></figure>

When a user submits a request, the system breaks it down into executable work items and creates corresponding Tasks in the Job Manager. Each Task includes a clear Job description, current status (e.g., Pending, Running, Succeeded, Failed/Needs Intervention), creation and update times, related inputs and outputs, and necessary execution logs for traceability and verification.

## Task Status Overview

There are 8 status types in total:

<table><thead><tr><th width="224">Status Name</th><th>Description</th></tr></thead><tbody><tr><td>PENDING</td><td>Created, waiting to enter the queue / not yet dispatched</td></tr><tr><td>QUEUED</td><td>In the queue, waiting to be executed</td></tr><tr><td>RUNNING</td><td>Currently executing</td></tr><tr><td>SUCCEEDED</td><td>Completed successfully</td></tr><tr><td>FAILED</td><td>Execution failed</td></tr><tr><td>STOPPED</td><td>Stopped (aborted)</td></tr><tr><td>CANCELED</td><td>Canceled</td></tr><tr><td>PAUSED</td><td>Paused</td></tr></tbody></table>

## Job Page Overview

Click the Task name you want to view to open a popup and browse the Jobs under it.

<figure><img src="../.gitbook/assets/image (216).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (217).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="101">Item</th><th width="177">Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Redo</td><td>Re-execute the Job</td></tr><tr><td>2</td><td>Continue</td><td>Resume the Job's progress</td></tr><tr><td>3</td><td>Details</td><td>View detailed information</td></tr><tr><td>4</td><td>Pause</td><td>Pause the Job's progress</td></tr><tr><td>3</td><td>Cancel</td><td>Cancel this Job's task</td></tr></tbody></table>
