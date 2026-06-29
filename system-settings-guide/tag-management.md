# Label Management

## Introduction

The Label Management feature helps users classify and manage items in the system through labels. Users can add different labels to each item for quick identification, filtering, and searching in lists. Users can centrally view, create, edit, or delete labels here, and confirm which functional module each label belongs to.

<figure><img src="../.gitbook/assets/image (402).png" alt=""><figcaption></figcaption></figure>

## Create Label

<figure><img src="../.gitbook/assets/image (404).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (405).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (406).png" alt=""><figcaption></figcaption></figure>

1. Go to the "Label Management" page under "System Settings."
2. Select the module to add a label.
3. Click the "Add" button in the upper right corner.
4. Enter the label name. Users can also click the button on the right to create a multilingual label. Please refer to [Multi-language Settings](biao-qian-guan-li.md#duo-guo-yu-yan-she-ding).
5. After confirming the content is correct, click Save or Create. Once created, the label will appear in the Label Management list.

### Multi-language Settings

<figure><img src="../.gitbook/assets/image (407).png" alt=""><figcaption></figcaption></figure>

1. Click the globe button on the screen for automatic translation. Users can also manually edit the content.
2. After automatic translation is complete, click the "OK/Confirm" button to save the content.

> Note: The large language model options in the "Model" dropdown should be based on the configuration of the actual installed environment. The options shown in the documentation are for reference only.

### Notes

* Labels are primarily used for classifying, filtering, and managing items. It is recommended that users confirm naming conventions before creating labels to avoid creating labels with similar meanings but different names within the same module, which can make subsequent management difficult.
* Duplicate label names cannot be created within the same functional module; the same label name can be used across different functional modules. For example, Agent and Knowledge Base can each have labels with the same name, but they will belong to different functional modules.
* Label names support multiple languages, and searches are performed according to the current system language. If the user switches languages, the display or search results may differ depending on the language setting.

## Delete Label

When a user deletes a label that is already in use by other data, the system will display a deletion confirmation window and provide two handling options:

* **Replace with Another Label**

If "Replace with Another Label" is selected, the user must specify a new label as the replacement target. Once confirmed, all data that originally referenced this label will be updated to reference the new label. This action cannot be undone after completion.

* **Do Not Replace, Delete All Associations**

If "Do Not Replace, Delete All Associations" is selected, the system will remove all associations between the data and this label. The original data itself will not be deleted, but the label will no longer be retained on the data. This action cannot be undone after completion.

<figure><img src="../.gitbook/assets/image (408).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (409).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (410).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (411).png" alt=""><figcaption></figcaption></figure>

1. Go to the "Label Management" page.
2. Find the label to be deleted and click the delete icon on the right side of that row.
3. Choose a handling method:
   * Select "Replace with Another Label" and specify the new label to replace with.
   * Or select "Do Not Replace, Delete All Associations."
4. Click "Continue."
5. The system will display a confirmation window again based on users' selection. After confirming the content is correct, click "Replace" or "Delete" to complete the operation.

### Notes

* After deleting a label or replacing label associations, the action cannot be undone. Before proceeding, please confirm whether the label is still in use by other data, and whether it needs to be replaced with another label first.
* If "Replace with Another Label" is selected, all data referencing the original label will be updated to reference the new label. If "Do Not Replace, Delete All Associations" is selected, all data referencing the original label will have that label association removed.
* Deleting a label only removes the label itself or its associations, and will not delete the functional modules or other data that the label was applied to.
