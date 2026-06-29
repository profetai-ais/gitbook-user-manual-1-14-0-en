---
description: The Chat Agent allows users to interact directly with large language models, suitable for tasks such as brainstorming, summarizing information, and generating formatted text content — without worrying about sensitive data leakage.
---

# Chat Agent

## **Create Agent**

<figure><img src="../.gitbook/assets/image (145).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

1. Click the "+ Create" button near the upper right of the screen
2. Select the "Agent Type" in the pop-up window
3. Enter the knowledge name in the "Name" field, then click the button on the right to create multilingual labels — see [Multi-language Settings](liao-tian-agent.md#duo-guo-yu-yan-she-ding)
4. Enter the knowledge description in the "Description" field, then click the button on the right to create multilingual labels — see [Multi-language Settings](liao-tian-agent.md#duo-guo-yu-yan-she-ding)
5. Click the "Tags" menu to select the tags to associate with this Agent
6. Click the "Model" menu to select the large language model for this Agent
7. Click the "Save" button to finish creating; the system will automatically navigate to the Agent editing screen for further configuration

### Multi-language Settings <a href="#duo-guo-yu-yan-she-ding" id="duo-guo-yu-yan-she-ding"></a>

<figure><img src="../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

1. Click the "Globe" button on the screen for automatic translation; users can also manually edit the content
2. After automatic translation is complete, click the "Confirm" button to save the content

> Note: The large language model options in the "Model" menu are based on the actual installed environment configuration. The options shown in the documentation are for reference only.

## Chat Agent Feature Interface

<figure><img src="../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

The Chat Agent homepage is divided into several sections, as shown below:

1. **Agent Feature Options**: The feature options area contains the following links, each opening a corresponding settings page

| Name        | Description                                       |
| --------- | ------------------- |
| Basic Settings      | Edit the Agent's main page        |
| Session Logs      | Provides conversation history for this Agent     |
| Member Management      | Manage access permissions for this Agent     |
| AI WEBAPP | Configure the web embed for this Agent     |
| API Key   | Provides credentials for third-party applications to securely call the API |

2. **Basic Information**: View the Agent name, creation and edit timestamps, personnel, and enabled status
3. **Application Settings:** Provides Agent behavior configuration based on Agent type

| Name         | Description                          |
| ---------- | --------------------------- |
| Inference Parameters       | Controls how responses are generated                   |
| Knowledge Base Configuration      | Select parameters and available knowledge sources                |
| Tools         | Enable and configure available tools                  |
| Skills         | Features that extend Agent capabilities            |
| Agent Collaboration   | Allows Agents to chain and collaborate with other Agents to execute tasks |
| Agent Welcome Page | Configure initial conversation content                    |
| Prompt Templates      | Provides reusable prompt templates for quick use         |
| File Handling     | Controls how uploaded files are processed                 |
| Guardrails         | Controls content output                      |

4. **Tuning Preview:** Allows users to test whether Q&A results meet expectations

## **Basic Settings**

<figure><img src="../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

All Agent types share the **Basic Settings** section on the homepage, which includes an **Enable Status** toggle switch and a **Settings** button for updating the Agent name and description. Clicking the Settings button opens the following dialog:

1. **Agent Status**: Users can edit the Agent's enabled status; toggling the switch changes the status immediately.
2. **Basic Settings Editing**: Allows editing of the most basic name, description, and international language translations.

### Agent Status Settings

<figure><img src="../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

1. Click the status field to open the interface
2. Click the Publish button
3. Copy the workspace URL
4. Click the conversation button to open the workspace conversation
5. Click the Unpublish button to cancel publishing

## **Application Settings**

### **Inference Parameters**

The settings include two tabs: "**Parameters**" and "**Instructions**".

#### **Parameters**

Users can control the Agent's response behavior by adjusting items in the "**Parameters**" tab.

<figure><img src="../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="98">Item</th><th width="112">Parameter</th><th width="238">Description</th><th>Range & Values</th></tr></thead><tbody><tr><td>1</td><td>Model</td><td>The default model selected when the Agent was created; can be changed here</td><td>n/a</td></tr><tr><td>2</td><td>Temperature</td><td>Controls the creativity of responses. Higher values produce more diverse and creative responses; lower values produce more precise and consistent responses</td><td>0–2</td></tr><tr><td>3</td><td>Top P</td><td>Controls randomness and diversity. Lower values produce more conservative and predictable text; higher values produce more diverse results</td><td>0–1</td></tr><tr><td>4</td><td>Max Tokens</td><td>Limits the maximum output length</td><td>Set as needed</td></tr><tr><td>5</td><td>Conversation Memory</td><td>Stores Q&A history to enhance coherence (may slow down response time)</td><td><code>0</code> means stateless responses; <code>5-10</code> balances coherence and performance. More memory means slower speed.</td></tr></tbody></table>

#### Instructions

Users can use the "Instructions" tab to define prompts that control the Agent's language, role, tone, and more.

<figure><img src="../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

* **Add prompts using templates**

Users can quickly add the required application templates from templates.

<figure><img src="../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

1. Add directly from a blank space; or, when prompts already exist, use the mouse to select the position to insert.
2. Click the "Templates" button to open the template list and select the desired template type.
3. The corresponding template will be generated; newly added templates appear highlighted, and can be further edited to suit your needs.
4. Click the "Save" button to finish editing.

* **Generate prompts from requirements**

The prompt generation feature supports "rewriting existing content" or "generating from scratch". The red input box above can optionally be filled in as the basis for rewriting; fill in the generation guidelines in the green input box below to produce results.

<figure><img src="../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

1. Select the dialog box below and enter your requirements for the prompt.
2. Press the Enter key on the keyboard or click the generate button on the right, and wait for the AI to automatically generate a template.
3. After automatic generation is complete, you can further edit it according to your needs.
4. Click the "Save" button to finish editing.

### Knowledge Base

#### Knowledge Base Sources

<figure><img src="../.gitbook/assets/image (187).png" alt=""><figcaption></figcaption></figure>

#### Knowledge Base Parameters

<figure><img src="../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

### **Tools**

Users can enable / disable the tools accessible to the Agent in the settings.

<figure><img src="../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>

#### **Session Memory**

<table><thead><tr><th width="250">Tool</th><th>Description</th></tr></thead><tbody><tr><td>KV Session Short-term Memory</td><td>Enables precise, key-based storage and retrieval of temporary data during a session. Useful for tracking dynamic variables such as <code>username</code> or <code>selected plan</code>.</td></tr><tr><td>graphiti - Add Memory Data</td><td>Stores episodic information (such as interactions or events) into a knowledge graph.</td></tr><tr><td>graphiti - Query Memory Nodes</td><td>Retrieves entity summaries or node-level memory representations.</td></tr><tr><td>graphiti - Query Memory Facts</td><td>Searches for relevant facts and structured relationships in the memory graph.</td></tr><tr><td>graphiti - Delete Entity Relationships</td><td>Deletes defined relationships between entities from the graph.</td></tr><tr><td>graphiti - Delete Event Segments</td><td>Deletes specific event segments from the memory graph.</td></tr><tr><td>graphiti - Get Entity Relationships</td><td>Retrieves structured relationships related to a specific entity.</td></tr><tr><td>graphiti - Get Event Segments</td><td>Returns recent memory episodes to provide context for conversations or decisions.</td></tr><tr><td>graphiti - Clear Memory Graph</td><td>Resets the entire graph-based memory system.</td></tr></tbody></table>

> Note: For more information about Graphiti, please refer to its official website.

#### **Academic Articles**

<table><thead><tr><th width="250">Tool</th><th>Usage Guide</th></tr></thead><tbody><tr><td>arXiv Paper Search</td><td>Allows users to search for academic papers from the arXiv database.</td></tr><tr><td>Google Scholar Search</td><td>Search academic articles and citations using Google Scholar.</td></tr></tbody></table>

#### **Web Search**

<table><thead><tr><th width="250">Tool</th><th>Usage Guide</th></tr></thead><tbody><tr><td>Serper - Web Content Extraction</td><td>Extracts readable content from a web page URL.</td></tr><tr><td>Serper - Google Search</td><td>Performs a Google search and returns summarized results.</td></tr><tr><td>Serper - Patent Search</td><td>Searches published patents and related documents.</td></tr><tr><td>Serper - Image Search</td><td>Searches for images based on a text query.</td></tr><tr><td>Serper - Paper Search</td><td>Queries academic papers using Google Scholar-style sources.</td></tr><tr><td>Serper - News Search</td><td>Searches for news based on a text query.</td></tr><tr><td>Serper - Map Search</td><td>Searches for map information based on a text query.</td></tr></tbody></table>

> Note: For more information about Serper, please refer to its official website.

#### **Code**

<table><thead><tr><th width="250">Tool</th><th>Usage Guide</th></tr></thead><tbody><tr><td>Execute Python Code</td><td>Executes Python scripts or logic to support tasks such as math, data parsing, or automation.</td></tr></tbody></table>

#### **Document Handling**

<table><thead><tr><th width="250">Tool</th><th>Usage Guide</th></tr></thead><tbody><tr><td>Preview Document</td><td>Displays uploaded documents in a readable format within the platform.</td></tr><tr><td>Document to Markdown</td><td>Converts documents to Markdown format.</td></tr></tbody></table>

#### **Other**

<table><thead><tr><th width="250">Tool</th><th>Usage Guide</th></tr></thead><tbody><tr><td>Get Current Time</td><td>Returns the current system time when the request is made.</td></tr><tr><td>Simple Math Expression Calculation</td><td>Performs simple arithmetic operations within prompts.</td></tr><tr><td>Dynamic Chain of Thought (Sequential Thinking)</td><td>Breaks down complex problems into step-by-step thinking, with the option to revise or branch. Suitable for planning, troubleshooting, and structured reasoning.</td></tr></tbody></table>

### Skills

<figure><img src="../.gitbook/assets/image (170).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (169).png" alt=""><figcaption></figcaption></figure>

By configuring different Skills, the Agent can support more features and task-handling scenarios, such as data access, tool operation, process execution, or task-specific extensions. Users can configure the corresponding skills based on their needs to enhance the Agent's flexibility and task-handling capabilities.

### Agent Collaboration

This feature allows users to establish collaborative relationships among multiple Agents, distributing tasks by role to improve process flexibility and overall task-handling efficiency.

<figure><img src="../.gitbook/assets/image (172).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (171).png" alt=""><figcaption></figcaption></figure>

### Guardrails

Guardrails are features for controlling content output. They can inspect and restrict content within workflows, helping to reduce risks related to personal data leakage, information security, and compliance, so that output content better conforms to usage norms and management requirements.

<figure><img src="../.gitbook/assets/image (173).png" alt=""><figcaption></figcaption></figure>

### **Conversation Panel**

The conversation panel contains Prompt Templates, Welcome Page, and Action Menu settings.

#### **Prompt Templates**

Users can bind existing or favorited application templates (prompt templates) to the Agent to accelerate Q&A by filling in required fields.

<figure><img src="../.gitbook/assets/image (167).png" alt=""><figcaption></figcaption></figure>

#### **Welcome Page**

**Quick Questions**

Users can set default conversation content, allowing the Agent to provide clickable question directions before the conversation starts, helping users begin interacting more quickly.

<figure><img src="../.gitbook/assets/image (329).png" alt=""><figcaption></figcaption></figure>

**Opening Message**

Set the Agent's initial greeting message. When a user selects this Agent and starts a conversation, the Agent will automatically send this message first as the conversation opener.

<figure><img src="../.gitbook/assets/image (330).png" alt=""><figcaption></figcaption></figure>

#### **Action Menu**

**File Handling**

The **File Handling** setting allows users to define how the Agent processes files uploaded in the workspace. This feature is especially useful when the Agent needs to interpret, convert, or extract content from files such as PDFs, DOCX documents, or images.

<figure><img src="../.gitbook/assets/image (331).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="109.5555419921875">Option</th><th width="101.111083984375">Visible to MCP Tools</th><th width="83.4444580078125">Visible to LLM</th><th>Description</th><th>Example Use Case</th></tr></thead><tbody><tr><td>None</td><td>X</td><td>X</td><td>The file is uploaded but not visible to either the LLM or MCP tools. It will not be opened or interpreted.</td><td>– –</td></tr><tr><td>LLM</td><td>O</td><td>X</td><td>The file is passed to MCP tools for processing, but not to the LLM.<br>Supported file types:<br>Documents: PDF, DOCX, DOC, PPTX, PPT<br>Images: JPG, JPEG, PNG, GIF, BMP</td><td>Useful when you want to extract data from a CSV or PDF without needing AI-generated commentary.</td></tr><tr><td>Tool Processing</td><td>X</td><td>O</td><td>The file is rendered as an image and made visible only to the LLM for reference.<br>Note: To enable this option, you also need to go to Tools > Document Processing and select File Preview.</td><td>Suitable for scanned documents or visual layouts where diagram relationships matter.</td></tr><tr><td>All</td><td>O</td><td>O</td><td>The file is both rendered for LLM reference and processed by MCP tools.<br>Note: To enable this option, you also need to go to Tools > Document Processing and select File Preview.</td><td>Best for invoices or tables that require both visual layout interpretation and structured data processing simultaneously.</td></tr></tbody></table>

**Canvas**

When enabled, the Canvas option is displayed in the conversation input menu.

When creating an Agent, the Canvas toggle is enabled by default.

<figure><img src="../.gitbook/assets/image (332).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (333).png" alt=""><figcaption></figcaption></figure>

## **Tuning Preview**

Use this section to test Agent responses and adjust settings accordingly.

> Please note: Files uploaded or generated in the Tuning Preview are retained for 30 minutes only.

<figure><img src="../.gitbook/assets/image (174).png" alt=""><figcaption></figcaption></figure>

### **Tuning Preview** File Upload Methods

* Click the plus sign (+) in the dialog box to upload files

<figure><img src="../.gitbook/assets/image (175).png" alt=""><figcaption></figcaption></figure>

* Drag-and-drop file upload is also supported

<figure><img src="../.gitbook/assets/image (176).png" alt=""><figcaption></figcaption></figure>

## Memory

The Memory feature helps users create reusable memory content for the Agent, enabling the Agent to reference pre-configured background information, usage contexts, and processing workflows when executing tasks or responding to questions.

Users can view the list of created memories on the Agent's Memory page, and quickly identify the purpose of each memory through its enabled status, name, description, and usage context. Memory can be used to store specific task workflows, decision rules, preconditions, operation steps, or notes, helping the Agent maintain consistent processing logic in subsequent interactions.

<figure><img src="../.gitbook/assets/image (177).png" alt=""><figcaption></figcaption></figure>

### Create Memory

<figure><img src="../.gitbook/assets/image (180).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (181).png" alt=""><figcaption></figcaption></figure>

1. Go to the Agent page. Click "Memory" in the left submenu.
2. Click the "Create" button in the upper right corner.
3. Fill in the basic memory information:
   * Name: Enter the memory name.
   * Description: Enter the memory description.
   * Applicable Context: Enter the usage context this memory applies to.
   * Content: Enter the detailed content; Markdown formatting can be used.
4. After confirming the content is correct, click "Create" to complete.

### View Memory Details

<figure><img src="../.gitbook/assets/image (179).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (178).png" alt=""><figcaption></figcaption></figure>

1. Go to the memory list.
2. Click the name of the memory you want to view.
3. The system will open a detail panel on the right.
4. Users can view the memory's name, enabled status, description, usage context, and full content. If the content is long, you can scroll up and down in the right panel to view it.

### Enable and Disable Memory

#### Memory Enable Rules

The Memory feature includes a global feature toggle and individual memory enable states.

<figure><img src="../.gitbook/assets/image (182).png" alt=""><figcaption></figcaption></figure>

If the toggle is on, it means this Agent can use the Memory feature. Users can still individually enable or disable different memories in the memory list.

If the toggle is off, it means this Agent does not use the Memory feature. Even if there are memories already created in the memory list, the Agent will not apply them.

#### Enable and Disable Individual Memories

<figure><img src="../.gitbook/assets/image (183).png" alt=""><figcaption></figcaption></figure>

In the memory list, the "Enable" column indicates whether an individual memory is enabled. When the global memory toggle is on, only individually enabled memories will be used as reference content when the Agent responds or processes tasks.

Users can disable memories they temporarily do not need, preserving the content without letting the Agent apply it; if needed again later, they can re-enable it.

## **Session Logs**

Session Logs store all conversation records for this Agent. Administrators can filter records by title, user, or date range. Records include processing workflows; when errors occur or responses are slow, administrators can review the processing details to diagnose issues.

<figure><img src="../.gitbook/assets/image (184).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (185).png" alt=""><figcaption></figcaption></figure>

## **Web App**

The Agent can be embedded into a web page to provide Q&A services, as shown below:

<figure><img src="../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

To embed the Agent into a website, use this feature to generate the front-end embed code.

### **Add Web App**

<figure><img src="../.gitbook/assets/image (81).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

1. Go to Web App in the "Agent Feature List"
2. Click "+" to open the _Create_ Web App dialog window
3. Enter the knowledge name in the "Name" field, then click the button on the right to create multilingual labels — see
4. Enter the knowledge description in the "Description" field, then click the button on the right to create multilingual labels — see
5. Click "Save" to finish
6. The new Web App will appear in the list. Use the "Actions" menu to "Edit", "Set Expiration Date", or "Delete"
7. Click the Web App name to access the information page and view the "Embed Code", set _Application Language_, _Request and Token Limits_, etc.

> Note: Each Agent can have multiple API keys and corresponding embed codes to independently manage the expiration dates and usage limits of different Web App instances.

## API Key

An API Key is an access credential used for identity verification, allowing the system to identify the request source and apply corresponding permissions and usage quotas when calling the Agent API. Please keep your API Key secure and prevent it from leaking; if you suspect the key has been compromised, it is recommended to replace it immediately and update all integration settings that use that key.

<figure><img src="../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

### Add API Key

<figure><img src="../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

1. Go to API Key in the "Agent Feature List"
2. Click "+" to open the _Create_ API Key dialog window
3. Enter the name of the API Key
4. Choose whether to enable Rate Limit and configure the value
5. If needed, set an expiration date for the API Key
6. Click the "Save" button

> Please note: After saving, copy your ID and API key immediately to avoid losing them.

### Copy Endpoint

The Endpoint is the service entry point (URL) for the Agent API. The system sends API requests to this location to execute the corresponding functions. Please select the correct Endpoint based on your use case (e.g., test environment or production environment) to avoid sending requests to the wrong environment or causing connection failures.

The copy button for the Endpoint is located next to the search box. Click the copy button to copy the URL. Please be aware of which environment you are in when copying the URL.

<figure><img src="../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>
