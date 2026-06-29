---
description: Administrators can create and adjust usage quota plans to manage the frequency and amount of system resources each user can consume.
---

# Quota

## Quota Plans

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="170">Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Name</td><td>The display name of the quota plan (e.g., <code>default</code>, <code>VVIP</code>, <code>Plan VIP</code>).</td></tr><tr><td>2</td><td>Usage Reset Cycle</td><td>The frequency at which the quota resets (e.g., daily, weekly, hourly).</td></tr><tr><td>3</td><td>Cost Limit (USD)</td><td>The maximum allowable spending per reset cycle (in USD). <code>-1</code> means unlimited.</td></tr><tr><td>4</td><td>Creator</td><td>The name of the administrator who created this plan.</td></tr><tr><td>5</td><td>Modified Date</td><td>The last modification time of the quota plan.</td></tr><tr><td>6</td><td>Description</td><td>Internal notes or descriptions of the quota plan's purpose.</td></tr><tr><td>7</td><td>Actions</td><td>Buttons for editing or deleting this plan.</td></tr></tbody></table>

## **Add Quota Plan**

Administrators can create new usage quota plans by configuring parameters such as name, description, cost limit, and reset cycle. These plans will control the frequency at which users consume paid resources (e.g., API tokens, model usage counts) according to the limits set here.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

1. Go to System Settings > Usage Quota Limits.
2. Select the Quota Plan tab.
3. Click the plus (+) button to open the Add/Update Quota Plan form.
4. Name: The display name for the plan.
5. Description: Optional internal notes.
6. Cost Limit (USD): The allowable amount per reset cycle (-1 means unlimited).
7. Usage Reset Cycle: Choose daily, weekly, or hourly.
8. Click OK to save the new quota plan.

## **Set Default Quota Plan**

The **Default Quota Plan** defines the baseline usage limits for all newly created users, unless a specific quota plan is manually assigned.

<figure><img src="../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

1. Go to the Set Default Quota Plan tab.
2. Click the Default User Quota Plan dropdown to view the list of available plans.
3. Select the desired plan from the list (e.g., `default`, `VVIP`, `ultra-low quota`).

> Note: Administrators can first create or update plans in the Quota Plan tab, and then set one as the default.

## **Quota Plan Binding Management**

The **Quota Plan Binding Management** feature allows administrators to manually assign a specific usage quota plan to a particular user, overriding the default settings.

<figure><img src="../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

1. Go to System Settings > User Quota Plan Binding Management.
2. Click "Create" to create a new binding.
3. On the left side (Dataset), select the quota plan to assign (e.g., `default`, `VVIP`, `Plan 1`).
4. On the right side (User), select one or more users from the dropdown list.
5. Click the "+" button to manually add users.
6. Click OK to confirm the assignment.

> Note: Once assigned, even if the default plan is later modified, the user will continue to follow the custom plan that has been bound to them.

## **Quota Adjustment Records**

The **Quota Adjustment Records** page logs all manual changes made to user quota usage, particularly operations from the **User Quota Plan Binding Management** tab.

<figure><img src="../.gitbook/assets/image (7) (1).png" alt=""><figcaption></figcaption></figure>

When an administrator clicks the **refresh icon** in the **User Quota Plan Binding Management** tab, the system will display a pop-up window prompting for a **Reason for Resetting Usage**. This field is required to complete the reset operation. Once confirmed, the updated budget and reason will be displayed on the User Quota Adjustment Records page.

<figure><img src="../.gitbook/assets/image (8) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="220">Field Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Username</td><td>The name of the user whose quota was manually adjusted.</td></tr><tr><td>2</td><td>Budget Before Adjustment (USD)</td><td>The user's budget before the adjustment (in USD).</td></tr><tr><td>3</td><td>Budget After Adjustment (USD)</td><td>The budget after the adjustment (in USD).</td></tr><tr><td>4</td><td>Reason for Usage Reset</td><td>Used to record the reason for the manual update or correction.</td></tr><tr><td>5</td><td>Created Date</td><td>The date the adjustment was performed.</td></tr></tbody></table>
