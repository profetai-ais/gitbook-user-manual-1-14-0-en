# Workflow Nodes

## Introduction

The workflow system provides a diverse set of node designs for building flexible, intelligent, and modular assistants. Each node plays a different role in enhancing system logic, user interaction, and backend integration.

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="160">Node Name</th><th>Purpose in Workflow</th></tr></thead><tbody><tr><td>1</td><td>Knowledge Retrieval</td><td>Retrieves relevant information from an internal knowledge base or document database.</td></tr><tr><td>2</td><td>LLM</td><td>Executes prompts using a language model (e.g., GPT-5.2 Thinking / GPT-5.2 Instant / Gemini 3) to generate or reason over results based on the current input.</td></tr><tr><td>3</td><td>Response</td><td>Defines what the user actually sees -- outputs and displays the assistant's reply.</td></tr><tr><td>4</td><td>Annotation</td><td>Adds internal comments or annotations on the canvas -- not connected to actual logic.</td></tr><tr><td>5</td><td>Variable Node</td><td>Captures, stores, or transforms values from a previous step for use by subsequent nodes.</td></tr><tr><td>6</td><td>Guardrail</td><td>Inspects and restricts content within the flow, helping reduce risks related to personal data leakage, information security, and compliance, so that outputs better conform to usage policies and governance requirements.</td></tr><tr><td>7</td><td>Classification</td><td>Automatically labels input or routes it based on pre-defined logic or model-based classification.</td></tr><tr><td>8</td><td>Fork</td><td>Describes the flow and order of data between nodes so that tasks can be executed automatically.</td></tr><tr><td>9</td><td>Merge</td><td>Converges the outputs of different branches into a single node, handing them off together to subsequent nodes for processing.</td></tr></tbody></table>

### **Knowledge Retrieval**

Retrieves relevant information from an internal knowledge base or document database.

<div align="center" data-with-frame="true"><figure><img src="../.gitbook/assets/image (29).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Knowledge Retrieval</td><td>The content of the Input (type "/" and select query as the user's question)</td></tr><tr><td>2</td><td>Knowledge Base Reference</td><td>Select the required knowledge base</td></tr><tr><td>3</td><td>Retrieval Parameters</td><td>Refer to "Test Knowledge Base - Retrieval Parameter Settings"</td></tr></tbody></table>

### **LLM**

Executes prompts using a language model (e.g., GPT-5.2 Thinking / GPT-5.2 Instant / Gemini 3) to generate or reason over results based on the current input.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (30).png" alt="" width="188"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>LLM Name</td><td>Enter a node name for easy identification</td></tr><tr><td>2</td><td>LLM Parameter Adjustment</td><td>Refer to <a href="liao-tian-agent.md#can-shu">Parameters</a></td></tr><tr><td>3</td><td>Model</td><td>Switch the language model used by this node (same as the model setting in item 2)</td></tr><tr><td>4</td><td>Context</td><td>The content of the Input (type "/" and select query as the user's question)</td></tr><tr><td>5</td><td>Use Node Files</td><td>Specifies which files the LLM is allowed to retrieve from preceding nodes</td></tr><tr><td>6</td><td>File Handling</td><td>Refer to <a href="https://www.notion.so/3509f9da96be81ef9413d427bc2132c7?pvs=21">File Handling</a></td></tr><tr><td>7</td><td>Enable Knowledge Base</td><td>Refer to <a href="https://www.notion.so/3509f9da96be81d7b1bbe69f43f236d4?pvs=21">Knowledge Base Source</a></td></tr><tr><td>8</td><td>Agent Collaboration</td><td>Refer to <a href="liao-tian-agent.md#agent-xie-zuo">Agent Collaboration</a></td></tr><tr><td>9</td><td>Skills</td><td>Refer to <a href="liao-tian-agent.md#ji-neng">Skills</a></td></tr><tr><td>10</td><td>Reference Memory</td><td>When enabled, the LLM will reference memories stored in the memory bank when generating replies. For how memories are stored, refer to <a href="../ge-ren-she-ding/agent-memory.md"> Agent Memory</a></td></tr><tr><td>11</td><td>Conversation Memory</td><td>Refer to Conversation Memory under <a href="liao-tian-agent.md#can-shu">Parameters</a></td></tr><tr><td>12</td><td>Tools</td><td>Refer to <a href="liao-tian-agent.md#gong-ju">Tools</a></td></tr></tbody></table>

### **Response**

The Response Node defines the **final output of the Agent**, responsible for returning the processed results from the flow to the user or as the output response for downstream systems.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (31).png" alt="" width="246"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Node Name</td><td>Enter a node name for easy identification</td></tr><tr><td>2</td><td>Notes</td><td>Optionally describe the purpose of this node</td></tr><tr><td>3</td><td>Configure Variable</td><td>Type / to configure a variable</td></tr></tbody></table>

### **Annotation**

Adds internal comments or annotations on the canvas -- not connected to actual logic.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (32).png" alt="" width="249"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Node Name</td><td>Enter a node name for easy identification</td></tr><tr><td>2</td><td>Notes</td><td>Enter notes for future reference</td></tr></tbody></table>

### **Variable Node**

Captures, stores, or transforms values from a previous step for use by subsequent nodes.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (33).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="200">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Variable (Global Variable Name)</td><td>Used to select or specify the <strong>global variable key</strong> to write to (e.g., <code>global.age</code>), so that subsequent flow nodes can read and reference it by a consistent name.</td></tr><tr><td>2</td><td>Variable Content (Variable Value)</td><td>Used to set the <strong>actual value</strong> of the global variable, so that subsequent nodes can use it directly.</td></tr></tbody></table>

### Guardrail

Automatically labels input or routes it based on pre-defined logic or model-based classification.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (34).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Configure Variable</td><td>Type / to configure a variable</td></tr><tr><td>2</td><td>Block/Mask</td><td>Select the operating mode of the guardrail</td></tr><tr><td>3</td><td>Category</td><td>Select the content to block or mask based on different types</td></tr></tbody></table>

### **Classification**

Automatically labels input or routes it based on pre-defined logic or model-based classification.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (35).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Model</td><td>Switch the language model used by this node</td></tr><tr><td>2</td><td>Context</td><td>The content of the Input (type "/" and select query as the user's question)</td></tr><tr><td>3</td><td>Category</td><td>Classify the question into a category</td></tr></tbody></table>

### Fork

Describes the flow and order of data between nodes so that tasks can be executed automatically.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (36).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Branch</td><td>View the current number of branches</td></tr><tr><td>2</td><td>Branch Status</td><td>View the current status of branches</td></tr></tbody></table>

### Merge

Converges the outputs of different branches into a single node, handing them off together to subsequent nodes for processing.

<div data-with-frame="true"><figure><img src="../.gitbook/assets/image (37).png" alt="" width="375"><figcaption></figcaption></figure></div>

<table><thead><tr><th width="80">Item</th><th width="160">Feature Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Waiting</td><td>View the number of nodes currently waiting</td></tr><tr><td>2</td><td>Input Status</td><td>View the current input status</td></tr><tr><td>3</td><td>Wait Timeout</td><td>Set the wait timeout</td></tr></tbody></table>
