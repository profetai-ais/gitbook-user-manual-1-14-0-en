# API Key

## Introduction

API Keys allow users to create dedicated API keys for external systems to call the open APIs supported by AI Studio. With an API Key, external programs, integration services, or third-party tools can make API calls under the user identity bound to the key without needing to log in with a username and password. Users can create new API Keys here and open the API documentation to view available API specifications.

Each API Key is bound to the user who created it. The system determines the accessible API scope based on that user's permissions.

<figure><img src="../.gitbook/assets/image (321).png" alt=""><figcaption></figcaption></figure>

## API Key Settings

After opening the API Key window, click the Generate button to create a key.

<figure><img src="../.gitbook/assets/image (336).png" alt=""><figcaption></figcaption></figure>

> Note: After an API Key is created, the full key content is only displayed once. For security reasons, the system will not display the full key again and cannot help retrieve the original key. If the key is lost, delete the original and create a new one.
> Each user can create a maximum of 1 API Key. To generate a new API Key, delete the existing one first before regenerating.

### Manage API Keys

After creating an API Key, users can view all keys they have created. To protect key security, the list only displays the masked key format, for example:

```
gak_abc*******xyz
```

After disabling or deleting an API Key, external systems can no longer use that key for API calls. If a key has an expiration date set, the system will automatically invalidate it after it expires.

> Note: Do not expose API Keys in public environments, such as front-end code, public Git repositories, or unprotected documents. If you suspect an API Key has been compromised, immediately disable or delete the key and create a new one.

## API Documentation

In the API Documentation section, users can click to open the API docs. The API documentation displays the available API specifications and allows you to view API paths, parameters, and test requests via the Swagger UI.

## Usage History

After switching to the Usage History tab, users can view the usage records for the API Key. Usage history helps users track calls from external systems and confirm whether any abnormal requests occurred. Users can also query API call records within a specific period by date range.
