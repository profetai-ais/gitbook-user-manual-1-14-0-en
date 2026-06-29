# Scheduling

## Introduction

<figure><img src="../.gitbook/assets/image (385).png" alt=""><figcaption></figcaption></figure>

Schedule allows users to create scheduled tasks, enabling a designated Agent to automatically execute instructions at a set time or on a recurring cycle. Users can use Schedule to run routine tasks on a regular basis, such as daily summaries, timed notifications, data queries, report generation, or automated workflows.

With schedule settings, users do not need to manually open an Agent conversation — the Agent can automatically execute tasks at a specified time, and the results and records of each execution are retained.

## Create Schedule

### Create from Schedule Management Page

<figure><img src="../.gitbook/assets/image (381).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (382).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (384).png" alt=""><figcaption></figcaption></figure>

1. Switch to the Schedule tab
2. Click **Add** in the top-right corner to open the Add Schedule window and create a new scheduled task
3. Enter a schedule name
4. Select the Agent to trigger the schedule — once selected, this cannot be changed
5. Select the schedule execution mode
   * Independent Mode: Each schedule execution is treated as an independent task, suitable for single-execution scenarios that do not require accumulated context
   * Context Mode: The schedule continues and accumulates the execution context, suitable for scenarios that require continuous tracking, information accumulation, or continuation of task status
6. Enter the task content for the Agent to complete each time it runs. Instructions should clearly describe the task goal, output format, and conditions to note, in order to improve the stability of schedule execution results
7. Enter the time range — the system will calculate the schedule execution time based on the selected timezone
8. Select the schedule time cycle. Schedules support the following three cycle modes:
   * Recurring: Used to set a schedule that repeats at a fixed interval. For example, setting it to **every 30 minutes** means the schedule will automatically execute every 30 minutes starting from the **start time**
   * Specific Time: Used to set a specific date and time for the schedule to execute. Users need to select the execution date and time. This mode is suitable for tasks that only need to run once at a specific time, or tasks triggered at a designated time by system settings
   * Custom: Used to set more complex schedule rules. Users can enter a natural language description and let the system help generate a Cron expression, or directly enter a Cron expression
9. Select execution limits. At least one usage limit must be enabled. When any enabled usage limit reaches its configured threshold, the schedule will be automatically disabled. Schedules support the following stop conditions:
   * Date: Set an end date. The schedule will stop executing after the specified date is reached
   * Count: Set a maximum execution count. The schedule will stop executing after the specified number of times is reached
   * Token: Set a maximum Token usage. The schedule will stop executing after the specified Token count is reached
10. Configure notification recipients. Users can set whether to notify designated users after the schedule completes. Schedules currently support Email notification and Webhook modes:
    * Email notification: The system will notify the designated recipients via email
    * Webhook: Users can set an external URL. After the schedule completes, the system can send the results via POST to the designated external service
11. After configuration is complete, click **Add** to finish

### Create from Agent Settings Page

<figure><img src="../.gitbook/assets/image (386).png" alt=""><figcaption></figcaption></figure>

The entry point is located in the Schedule Management section of the Agent settings page. The process for adding a schedule can refer to [Create from Schedule Management Page](pai-cheng.md#cong-pai-cheng-guan-li-ye-mian-jian-li). The only difference is that on the Agent settings page, users cannot configure a different Agent.



## View Logs

On the schedule detail page, click **Logs** to view the execution records for that schedule.

<figure><img src="../.gitbook/assets/image (380).png" alt=""><figcaption></figcaption></figure>

The log list displays the title and status of each execution. Users can click a record to view the detailed content of that execution.

Execution results are presented in conversation form, including the Agent's reply, execution cost, and related operations. Users can copy the execution results or return to the log list to view other records.

Logs help users confirm whether the schedule executed successfully, whether the Agent's response met expectations, and whether the results of each execution require further processing.



## Notes

Schedules execute automatically according to the configured timezone and cycle. Before creating a schedule, please confirm that the time range, start time, cycle, and execution limit conditions are correct.

If a schedule execution fails, users can check the error records and execution results in the logs. If the schedule does not execute as expected, please confirm whether the schedule is enabled, whether the stop conditions have reached their threshold, and whether the Agent is still functioning normally.

If the scheduled task calls external services or sends notifications, please confirm that the Webhook URL, notification method, and recipient settings are correct.
