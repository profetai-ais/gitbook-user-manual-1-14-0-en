# Manage Knowledge Base

## Introduction

> Note: By default, only AI Studio administrators, AI Studio collaborators, knowledge base administrators, knowledge base collaborators, and knowledge base members can use the knowledge base feature. If account is unable to use the knowledge base, please confirm account permissions with an administrator.

The way datasets within knowledge are organized is shown in the diagram below:

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

## **Create New Knowledge**

### **Manually Create Knowledge**

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

1. Click the "Knowledge Base" item in the left menu
2. Click the "+" button near the top-right of the screen
3. Enter the knowledge name in the "Name" field, then click the button on the right to create multilingual labels. See [Multi-language Settings](guan-li-zhi-shi-ku.md#duo-guo-yu-yan-she-ding)
4. Enter the knowledge description in the "Description" field, then click the button on the right to create multilingual labels. See [Multi-language Settings](guan-li-zhi-shi-ku.md#duo-guo-yu-yan-she-ding)
5. Click the "Index Model" menu to select the model used to convert text into semantic vectors for this knowledge base
6. Click the "Save" button to complete the addition

### Multi-language Settings

<figure><img src="../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

1. Click the "globe button" on the screen for automatic translation; users can also manually edit the content
2. After automatic translation is complete, click the "Save" button to save the content

### **Import Knowledge**

<figure><img src="../.gitbook/assets/image (387).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (390).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (391).png" alt=""><figcaption></figcaption></figure>

1. Go to the Knowledge Base tab
2. Click the More button in the top-right corner, and select Import File
3. After selecting a model in the embedding model field, click the test button to verify whether the model is functioning properly
   1. This is the model used to build the knowledge base index. After importing knowledge, the system will use this model to re-index the knowledge base content for subsequent retrieval and Agent responses
4. If the test is successful, the system will display a success message. If the test fails, please select another available model, or verify that the model has been correctly configured, that account have the necessary usage permissions, and that the model service can be reached. After confirming, click the close button to close the window
5. Select the file to import
6. Click the import button to complete the import

> Note: Users must test the model first. The import operation can only proceed after the test is successful.

## Permissions

For list permission descriptions, please refer to [Module Permission Role Introduction - Knowledge Base List Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#zhi-shi-ku-qing-dan).

For permission configuration instructions, please refer to [Permission Operation Feature Introduction - Root Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#root-quan-xian).

### Knowledge Permissions

For role permission descriptions, please refer to [Module Permission Role Introduction - Knowledge Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#zhi-shi).

For permission configuration instructions, please refer to [Permission Operation Feature Introduction - Object Role Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#jue-se-quan-xian).

### Dataset Permissions

For role permission descriptions, please refer to [Module Permission Role Introduction - Dataset Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#shu-ju-ji).

For permission configuration instructions, please refer to [Permission Operation Feature Introduction - Object Access Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#cun-qu-quan-xian).
