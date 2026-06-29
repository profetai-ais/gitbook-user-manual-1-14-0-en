---
description: This page introduces how to operate Root Permissions and Object Permissions.
---

# Permission Operations

## **Root Permissions**

### **Where to Access**

The Root permission settings are located in the more options button at the top right of the module. Click it to open the permission management window.

<figure><img src="../.gitbook/assets/image (352).png" alt=""><figcaption></figcaption></figure>

### Page Navigation

<figure><img src="../.gitbook/assets/image (349).png" alt=""><figcaption></figcaption></figure>

| Item | Action Name    | Description                             |
| -- | ------- | ------------------------------ |
| 1  | Select User   | Search by name or account to add a user                   |
| 2  | Select Permissions    | Select the list permissions to configure                     |
| 3  | Added Users | View information and permission settings of added users; permissions can be adjusted or users removed |

### **Add Member**

<figure><img src="../.gitbook/assets/image (351).png" alt=""><figcaption></figcaption></figure>

1. Enter a keyword to search for the user to add
2. Set the permission level
3. Click Add to complete the setup; the permission settings take effect after the other party refreshes the page

### **Adjust Member Permissions**

<figure><img src="../.gitbook/assets/image (362).png" alt=""><figcaption></figcaption></figure>

1. Find the target user whose permissions you want to adjust
2. Click the dropdown menu on the right to adjust permissions

### **Remove Member**

<figure><img src="../.gitbook/assets/image (363).png" alt=""><figcaption></figcaption></figure>

1. Find the target user to remove
2. Click the dropdown menu on the right and select Remove

## Object Permissions

Object permissions in different features may use different permission modes. Common modes include role-based permissions and access permissions.

### **Where to Access**

Permission settings are located within the object inside the module. Click the target object, then select the permissions tab on the inner page to view the permission management page. The Agent module is used here as an example.

<figure><img src="../.gitbook/assets/image (353).png" alt=""><figcaption></figcaption></figure>

### Role Permissions

Role permissions differentiate the operations users can perform based on their role. Each object can have 2 to 3 permission roles set. The creator can grant access to other users through "Permissions." Users with higher permissions can typically manage object settings, adjust content, or maintain authorized members; users with lower permissions may only be able to view or use the object.

Common scenarios include:

* Can manage the object
* Can edit the object
* Can view or use the object

> Note: Actual role names and operable scope vary by feature design (for role definitions, refer to [Module Permission Roles](quan-xian-gong-neng-jie-shao.md)).

### Page Navigation

<figure><img src="../.gitbook/assets/image (355).png" alt=""><figcaption></figcaption></figure>

| Item | Action Name | Description                            |
| -- | ---- | ----------------------------- |
| 1  | Edit Table | Allows users to edit how the table is displayed                |
| 2  | Refresh   | Click to refresh the list                       |
| 3  | Content Filter | Advanced filtering for specified content                      |
| 4  | Batch Delete | After checking items, a delete button appears in the top left, allowing users to delete multiple items |
| 5  | Search Field | Search by name                         |
| 6  | Invite   | Invite an organization / member                     |
| 7  | Actions   | Transfer roles or delete the selected user               |

#### **Add Member**

<figure><img src="../.gitbook/assets/image (356).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (357).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (358).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (359).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (360).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (361).png" alt=""><figcaption></figcaption></figure>

1. Click "Add" to open the _Add Member_ dialog
2. The input field can search for organizations or users
3. Select the corresponding permissions
4. There are two ways to select an organization/user:
   * Click to search by organization
   * Enter a keyword to bring up matching organizations/users; click the level button on the right to confirm the role level
5. After selecting the target organization/user, click the tag to open the view menu to see all users within the organization level and role
6. Click the "Add" button to complete the invitation

#### **Adjust Member Permissions**

<figure><img src="../.gitbook/assets/image (364).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (365).png" alt=""><figcaption></figcaption></figure>

1. Find the target organization/user whose permissions you want to adjust and click the edit button
2. Adjust the permissions
3. Click Save to complete the setup

#### **Transfer Owner**

<figure><img src="../.gitbook/assets/image (366).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (367).png" alt=""><figcaption></figcaption></figure>

1. Find the target user to transfer ownership to and click the transfer permissions button
2. Confirm the transfer user's information
3. Click Transfer to complete the setup

> Note:&#x20;
>
> 1. The Transfer Owner feature only applies to user role; one cannot transfer ownership to an organization.
> 2. After transferring ownership, the object's owner and creator will automatically change to the new user, and the object permissions will remain as they were before the transfer.

#### **Remove Member**

<figure><img src="../.gitbook/assets/image (368).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (369).png" alt=""><figcaption></figcaption></figure>

1. Find the target organization/user to remove and click the remove button
2. Confirm whether to remove the target, then click the Remove button

### Access Permissions

Access permissions can be granted to organizations or individual users. If granted to an organization, all users within that organization will have access to that data. The Knowledge Base's Dataset is used here as an example.

{% hint style="info" %}
Objects with access permission settings in AI Studio currently include the **Knowledge Base's Dataset** and **MCP's MCP Tools.**
{% endhint %}

#### **Add Member**

<figure><img src="../.gitbook/assets/image (371).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (373).png" alt=""><figcaption></figcaption></figure>

1. Click the _Dataset Access Permissions_ item in the "Knowledge Settings Menu"
2. Click the button to batch add permissions to the dataset
3. In the "Dataset" area, select the file to configure permissions for
4. In the right area, click the "Organization" tab and check the organization levels to grant permissions to
5. In the right area, click the "User" tab to select users to grant permissions to
6. In the "User Menu," search for the user to add
7. After completing the organization and user changes, click the "ok" button to save the settings

#### **Remove Member**

<figure><img src="../.gitbook/assets/image (375).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (374).png" alt=""><figcaption></figcaption></figure>

1. Click the edit button for the dataset to remove from
2. Select the organization or user to remove and click the remove button
3. Click Save to complete the setup
