---
description: Workflow Agent allows users to design how an Agent can complete complex tasks using the functional components provided by AI Studio, by building a workflow.
---

# Workflow Agent

## **Create Workflow Agent**

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (189).png" alt=""><figcaption></figcaption></figure>

1. Click the "+ Create" button near the upper right of the screen
2. In the dialog window, select the "Agent Type" as _Workflow_
3. Enter the name in the "Name" field, then click the button on the right to create multi-language labels. See [Multi-language Settings](gong-zuo-liu-cheng-agent.md#duo-guo-yu-yan-she-ding)
4. Enter the description in the "Description" field, then click the button on the right to create multi-language labels. See [Multi-language Settings](gong-zuo-liu-cheng-agent.md#duo-guo-yu-yan-she-ding)
5. Click the "Workflow Template" menu to select a workflow template
6. Click the "Save" button to finish. The system will automatically enter the Agent editing screen for the user to complete the configuration

### Multi-language Settings

<figure><img src="../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

1. Click the "globe button" on the screen for automatic translation. Users can also manually edit the content
2. After automatic translation is complete, click the "OK" button to save the content

> Note: The workflow template options in the Workflow menu depend on the configuration of the actual installation environment. The options shown in this documentation are for reference only.

## Workflow Agent Feature Interface

The homepage of the Workflow Agent can be divided into several main areas, as shown below:

<figure><img src="../.gitbook/assets/image (191).png" alt=""><figcaption></figcaption></figure>

1.  **Agent Feature Menu:** Provides links to Agent feature settings

    The feature menu area contains the following links. Click to navigate to the corresponding settings page:

<table><thead><tr><th width="250">Name</th><th>Description</th></tr></thead><tbody><tr><td>Basic Settings</td><td>Edit the Agent's homepage</td></tr><tr><td>Workflow Settings</td><td>Edit the Agent's workflow</td></tr><tr><td>Session Logs</td><td>View conversation records for this Agent</td></tr><tr><td>Member Management</td><td>Manage access permissions for this Agent</td></tr><tr><td>AI WEBAPP</td><td>Configure web embedding for this Agent</td></tr><tr><td>API Key</td><td>Credentials for third-party applications to securely call the API</td></tr></tbody></table>

2. **Basic Information**: Edit the Agent name, description, and enabled status
3. **Application Settings:** Provides Agent behavior settings based on the Agent type

<table><thead><tr><th width="250">Name</th><th>Description</th></tr></thead><tbody><tr><td>Welcome Page</td><td>Configure Agent question settings</td></tr><tr><td>Prompt Templates</td><td>Add existing prompt templates for later use</td></tr><tr><td>File Handling</td><td>Control how uploaded files are processed</td></tr></tbody></table>

4. **Tuning Preview:** Allows users to test whether Q&A results are as expected

## **Basic Settings**

All Agent types share the Basic Settings section on the homepage, which includes the enabled status toggle and a Settings button for updating the Agent name and description. Clicking the Settings button opens the following dialog window:

<figure><img src="../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

1. **Agent Status**: Users can edit the Agent's enabled status. Toggling the switch changes the status immediately.
2. **Basic Settings Editing**: Edit the most basic name, description, and international language translations.

### Agent Status Settings

<figure><img src="../.gitbook/assets/image (192).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (193).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (194).png" alt=""><figcaption></figcaption></figure>

1. Click the status bar to open the interface
2. Click the Publish button
3. Copy the URL in the workspace
4. Click the conversation button to open the workspace conversation
5. Click the Unpublish button to cancel publishing

## **Application Settings**

Provides Agent behavior settings based on the Agent type. The following describes the application settings for the _Workflow Agent_.

### **Prompt Templates**

Bind created or saved application templates (Prompt Templates) to the Agent. When using them, only the necessary information needs to be filled in, speeding up the Q&A process.

<figure><img src="../.gitbook/assets/image (195).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (197).png" alt=""><figcaption></figcaption></figure>

### **Welcome Page**

Users can configure default conversation content, allowing the Agent to provide clickable question prompts before the conversation begins, helping users start interacting more quickly.

<figure><img src="../.gitbook/assets/image (196).png" alt=""><figcaption></figcaption></figure>

## **Tuning Preview**

Users can test Agent behavior and response content in this area, and adjust the Agent's configuration based on the responses.

<figure><img src="../.gitbook/assets/image (198).png" alt=""><figcaption></figcaption></figure>

## Workflow Configuration

"Workflow Configuration" in the Agent Feature Menu is used to edit the Agent's workflow. Clicking it opens the editing screen for the workflow bound to this Agent.

> For screen descriptions and operations related to workflow editing, see [Edit Workflow](bian-ji-gong-zuo-liu-cheng.md)

## **Session Logs**

Session Logs provide all conversation records for this Agent. Administrators can filter records by title, user, and conversation time range.

The logs also retain the processing flow. When errors occur or performance is poor in a conversation, administrators can review the processing flow generated for each response to identify the cause.

<figure><img src="../.gitbook/assets/image (199).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (200).png" alt=""><figcaption></figcaption></figure>

## **Web App**

Agents can be embedded in web pages to provide Q&A services, as shown in the example below:

<figure><img src="../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

If users want to embed an Agent into a web page, they need to use this feature to generate the code for embedding in the web frontend.

### **Add AI WEBAPP**

<figure><img src="../.gitbook/assets/image (207).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (208).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (209).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (210).png" alt=""><figcaption></figcaption></figure>

1. Go to Web App in the "Agent Feature Menu" list
2. Click "+" to open the _Create_ Web App dialog window
3. Enter the name in the "Name" field, then click the button on the right to create multi-language labels. See [Multi-language Settings](gong-zuo-liu-cheng-agent.md#duo-guo-yu-yan-she-ding)
4. Enter the description in the "Description" field, then click the button on the right to create multi-language labels. See [Multi-language Settings](gong-zuo-liu-cheng-agent.md#duo-guo-yu-yan-she-ding)
5. Click "Save" to finish
6. The new Web App will appear in the list. Use the "Actions" menu to "Edit", "Set Expiration Date", or "Delete"
7. Click the Web App name to access the information page and view "Embed Code", configure _application language_, _request and token limits_, etc.

> Note: Each Agent can have multiple API keys and corresponding embed codes to independently manage expiration dates and usage limits for different Web App instances.

## API Key

An API Key is an access credential used for identity verification. It allows the system to identify the source of requests and apply the corresponding permissions and usage quotas when calling the Agent API. Keep your API Key secure and avoid leaking it. If you suspect the key has been compromised, it is recommended to replace it immediately and update all integration settings that use that key.

<figure><img src="../.gitbook/assets/image (211).png" alt=""><figcaption></figcaption></figure>

### Add API Key

<figure><img src="../.gitbook/assets/image (212).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (213).png" alt=""><figcaption></figcaption></figure>

1. Go to API Key in the "Agent Feature Menu" list
2. Click "+" to open the _Create_ API Key dialog window
3. Enter the name for the API Key
4. Choose whether to enable Rate Limit and set the value
5. Click the "Save" button

> Note: After saving, please copy your ID and API key immediately to avoid losing them.

### Copy Endpoint

An Endpoint is the service entry URL for the Agent API. The system will send API requests to this location to execute the corresponding functions. Select the correct Endpoint based on your use case (e.g., test environment or production environment) to avoid sending requests to the wrong environment or causing connection failures.

The copy button for the Endpoint is located next to the search box. Click the copy button to copy the URL. Please pay attention to the environment you are in when copying the URL.

<figure><img src="../.gitbook/assets/image (214).png" alt=""><figcaption></figcaption></figure>
