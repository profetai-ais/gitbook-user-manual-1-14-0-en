---
description: AI Studio provides a two-level permission control system, helping users flexibly configure "who can access a specific feature list" and "who can operate individual items within it."
---

# AI Studio Permission Architecture

## Permission Architecture

<figure><img src="../.gitbook/assets/image (397).png" alt=""><figcaption></figcaption></figure>

### Feature Level (Root)&#x20;

Used to manage the access and administrative permissions for "a category of features," such as Agent List, Knowledge Base List, Template List, etc. This level determines whether users can enter the feature, create new items, or manage the member list for that feature.

The view permissions for Root are determined by the AI Studio role permission configuration. For AI Studio role permission details, refer to [AI Studio Roles and Permissions](ai-studio-jue-se-yu-quan-xian-shuo-ming.md).

### Item Level (Object)&#x20;

Used to manage permissions for "each individual item" within a feature, such as a specific Agent, a specific Knowledge Base, or a specific Template. This level allows users to set member roles for individual items, deciding who can edit, who can only use, and who can manage members.

The view permissions for Object are determined by the Root role permission configuration. For Root role permission details, refer to the individual **list role permissions** in [Module Permission Roles](quan-xian-gong-neng-jie-shao.md).

> Note: By default, only roles with administrative permissions can access the corresponding feature and perform management operations. If users cannot see certain features or cannot perform operations, please confirm with the administrator whether account permissions at the "Feature Level" and "Item Level" have been granted.

## How Permissions Are Determined

<figure><img src="../.gitbook/assets/image (398).png" alt=""><figcaption></figcaption></figure>

The system first evaluates the user's Root permissions for that feature, then decides based on the user's Root role whether further evaluation of Object permissions is needed.

* If the user is the **List Administrator** of that feature, they can manage objects within that feature and perform add, edit, and delete operations even without individual Object permissions.
* If the user is a **List Collaborator** or **List User** of that feature, the accessible and operable object scope is still determined by Object permissions.
* If the user has no Root permissions for that feature, they cannot access the feature page or operate any objects within it.

### Notes

The content a user can view and operate will vary based on Root and Object permission settings. If a user cannot see a specific feature or object, confirm whether that user has the Root permissions for the corresponding feature and whether the corresponding Object permissions have been granted for that object.

If a user needs to manage all objects within an entire feature, they can be set as the Root Admin for that feature. If only specific object access is needed, it can be configured through Object permissions.

After adjusting permissions, some pages may need to be refreshed or re-entered before the latest permission results are displayed.



## Root Permissions

<figure><img src="../.gitbook/assets/image (347).png" alt=""><figcaption></figcaption></figure>

Root permissions are the outermost control permissions of the entire module, used to control the overall scope of operations a user has within a feature. Root permissions are typically divided into the following roles:

* **List Administrator**
* **List Collaborator**
* **List User**

The scope of operations available to different Root roles varies depending on the feature design.

If a user has Root permissions for a feature, they can access that feature's page or use the main operations provided by that feature — for example, accessing Agent, Knowledge Base, Templates, or other feature modules.

Among these, the **List Administrator** has the highest administrative permissions for that feature. When a user is the List Administrator for a feature, they can perform add, edit, and delete management operations on objects within that feature even without specific Object permissions.

## **Object Permissions**

<figure><img src="../.gitbook/assets/image (348).png" alt=""><figcaption></figcaption></figure>

Object permissions control which individual objects a user can access and operate within a feature.

A single feature may contain multiple objects, such as different Agents, Knowledge Bases, Templates, or other items. When a user is not the List Administrator for that feature, the system uses each object's Object permissions to determine whether the user can view, use, edit, or manage that object.

## AI Studio and Root Permission Sync

Upon login, the system automatically adds list permissions matching the user's current AI Studio account permissions.

For example: if an account is an **AI Studio Collaborator**, upon login it automatically receives **List Collaborator** permissions for Agent, Knowledge Base, Capabilities (Skills, MCP), Templates (Workflow, Prompt), and Analytics (Reports).

This feature **only triggers a sync at login for parts that currently have no permissions** and **does not affect existing list permissions**. If the account's permissions in AI Studio change, the automatic permission sync will not be triggered.
