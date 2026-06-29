---
description: This page is used to centrally manage the secret keys (API Keys) required by the system. Through this page, users can add, view, and delete secret keys to ensure that system services operate securely and correctly.
---

# Secret Key Management

## Page Navigation

After entering the "Key Management" page, the screen will display a list of currently created secret keys. Field descriptions are as follows:

<figure><img src="../.gitbook/assets/image (9) (1).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="210">Name</th><th>Description</th></tr></thead><tbody><tr><td>Type</td><td>Key Type (e.g., SERPER, LiteLLM), representing the type of service this key corresponds to</td></tr><tr><td>Name</td><td>Key Name, used to identify the purpose of this API Key</td></tr><tr><td>Key</td><td>The API Key value, displayed only in masked form for security</td></tr><tr><td>Tenant ID</td><td>Tenant ID</td></tr><tr><td>Expire Date</td><td>Key Expiration</td></tr><tr><td>Creator</td><td>Creator</td></tr><tr><td>Created Date</td><td>Created Date</td></tr><tr><td>Modified Date</td><td>Last Modified Date</td></tr><tr><td>Actions</td><td>Actions; currently provides delete (trash icon)</td></tr></tbody></table>

## Add Secret Key

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

1. Click "+" in the upper right corner to open the Add Secret Key configuration window, then complete the following settings in order:
2. Type: Select the key type.
3. Name: Enter an identifying name for this API Key. It is recommended to enter a specific purpose (e.g., `litellm api key`) for easier management later.
4. API Key: Enter the actual API key content.
   * The field is hidden by default.
   * Users can toggle show/hide via the eye icon on the right side.
5. Confirm and Submit: Once configuration is complete, click "Ok" to save the secret key; if users do not wish to save, click "Cancel" to cancel the operation.

## Delete Secret Key

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

1. Click the trash icon in the Actions column on the far right of the row.
2. Click Confirm to execute the deletion; the secret key will be immediately removed from the list.

### **Notes**

* **Deleted secret keys cannot be restored.**
* If the API Key is currently in use by the system or a workflow, deleting it may cause related features to malfunction.
* It is recommended to confirm that the key is no longer referenced by any service or workflow before deleting it.
