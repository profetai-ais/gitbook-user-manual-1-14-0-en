# Prompt Template Management

## Introduction

Prompt templates simplify the way users ask questions. Frequently asked questions or methods for retrieving information can be templatized, allowing users to get high-quality responses by providing only the key information, without writing prompts themselves. Enterprises can use this feature to improve response consistency and ensure that generative AI responses meet company policy requirements.

> Note: By default, only AI Studio administrators can modify these settings.

## **Add Prompt Template**

<figure><img src="../.gitbook/assets/image (261).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (262).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (263).png" alt=""><figcaption></figcaption></figure>

1. Click "Add" to display the create prompt template window
2. Select the prompt template type
3. In the "Name" field, enter the name, then click the button on the right to create multi-language labels. See [Multi-language Settings](ti-shi-mu-ban-guan-li.md#duo-guo-yu-yan-she-ding)
4. In the "Description" field, enter the description, then click the button on the right to create multi-language labels. See [Multi-language Settings](ti-shi-mu-ban-guan-li.md#duo-guo-yu-yan-she-ding)
5. Create "Fields"
6. Configure the prompt in the "Prompt Settings" tab
7. Click "OK" to complete the addition

### Multi-language Settings

<figure><img src="../.gitbook/assets/image (259).png" alt=""><figcaption></figcaption></figure>

1. Click the "globe" button on the screen for automatic translation. Users can also manually edit the content.
2. After automatic translation is complete, click the "OK" button to save the content.

> Note: The large language model options in the "Model" menu depend on the configuration of your actual installation environment. The options shown in this documentation are for reference only.

### **Prompt Template Types**

* **Chat Prompt:** A template for use in all scenarios. After editing, it can be saved and used under "App Templates" on the "Explore" page.
* **Agent Prompt:** A prompt template bound exclusively to an assistant. It will not appear on the "Explore" page for users to save.

### **Field Descriptions**

<figure><img src="../.gitbook/assets/image (264).png" alt=""><figcaption></figcaption></figure>

_Fields_ can be thought of as variables within a prompt, allowing users to provide the necessary information for the prompt based on their actual scenario. Fields come in the following types:

* **Text:** A single-line input field. Text length can be configured.
* **Multi-line Text:** A multi-line input field. Text length can be configured.
* **List:** Creates options that users can select from.
* **Number:** A numeric input field. Maximum and minimum values can be configured.
* **File Upload:** Creates a field that allows users to upload files.

## Permissions

For list permission descriptions, refer to [Module Permission Role Introduction - Prompt Template List Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#ti-shi-ci-mu-ban-qing-dan).

For permission configuration instructions, refer to [Permission Operation Feature Introduction - Root Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#root-quan-xian).

### Workflow Template Permissions

For role permission descriptions, refer to [Module Permission Role Introduction - Prompt Template Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#ti-shi-ci-mu-ban).

For permission configuration instructions, refer to [Permission Operation Feature Introduction - Object Role Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#jue-se-quan-xian).
