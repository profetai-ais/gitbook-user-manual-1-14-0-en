---
description: This guide provides a step-by-step walkthrough of how to configure an LLM node based on the UI elements in the workflow editor.
---

# Workflow Node Settings

## Page Overview

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Step</th><th width="180">Section</th><th>Instructions</th></tr></thead><tbody><tr><td>1</td><td>Node Name</td><td>Give the LLM node a clear and descriptive name (e.g., 2. Industry Trends). This helps organize the workflow visually and logically, especially in complex flows. <strong>Note:</strong> Node names must be unique in order to save the configuration.</td></tr><tr><td>2</td><td>Node Description</td><td>Provide a brief description for the LLM node (e.g., Includes industry dynamics, policy changes, technology drivers, and corporate behavior). This helps organize the workflow visually and logically, especially in complex flows.</td></tr><tr><td>3</td><td>Model Selection</td><td>Select a language model from the dropdown (e.g., gpt-5.2-thinking or gpt-5.2-instant). Ensure the model meets your response quality and budget requirements.</td></tr><tr><td>4</td><td>Context (Input Variables)</td><td>Configure the input content the LLM should reference during inference. You can use variables from other nodes or user input to pass dynamic inputs. Type <code>/</code> in the context window to view available variables. ⚠️ To access variables such as <code>result</code>, <code>usage</code>, or <code>execution_time</code> from preceding nodes, those nodes must be <strong>explicitly connected</strong> to the current node; otherwise the context cannot resolve the variables correctly.</td></tr><tr><td>5</td><td>Use Node Files</td><td>Specifies which files the LLM is allowed to retrieve from preceding nodes.</td></tr><tr><td>6</td><td>File Handling (optional)</td><td>Choose how uploaded files are handled. For more information, refer to the <a href="liao-tian-agent.md#dang-an-chu-li">File Handling</a> section.</td></tr><tr><td>7</td><td>Knowledge Base</td><td>When enabled, the selected knowledge base is automatically queried during conversations.</td></tr><tr><td>13</td><td>Inference Settings</td><td>Click the gear icon () next to the model selection area to customize model behavior, including:<br><em>1. Parameter Adjustments</em>: Temperature, Top P, Max Tokens (see the parameter table for more information).<br><em>2. System Prompt</em>: Write a prompt to define the role, task, tone, and tool behavior.</td></tr></tbody></table>

<figure><img src="../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Step</th><th width="180">Section</th><th>Instructions</th></tr></thead><tbody><tr><td>8</td><td>Agent Collaboration</td><td>Allows the Agent to chain and collaborate with other Agents to execute tasks.</td></tr><tr><td>9</td><td>Skills</td><td>By configuring different skills, the Agent can support more features and task-handling scenarios.</td></tr><tr><td>10</td><td>Reference Memory</td><td>When enabled, the Agent references the personal memory store during conversations.</td></tr><tr><td>11</td><td>Memory Settings (optional)</td><td>Enable memory if multi-turn conversation context is needed. Set the memory window size when building multi-turn conversations or reasoning chains (recommended value: 3–5). <strong>Note:</strong> It is recommended to keep the number of memory turns consistent across sessions to ensure flow consistency and avoid information loss. ⚠️ One conversation turn refers to one pair of a question (user prompt) and a response (assistant reply).</td></tr><tr><td>12</td><td>Tools (optional)</td><td>If the task requires capabilities beyond the LLM's native abilities, you can attach tools (e.g., use the <strong>Serper Search</strong> tool to perform real-time web searches during generation).</td></tr></tbody></table>

## **How to Use Context and System Prompt**

When configuring an LLM node, both **Context** and **System Prompt** can contain instructions, but they serve different purposes and have a clear priority hierarchy:

### **Context**

> Purpose: Sets dynamic input variables. Think of it as the model's "workspace" — the content the model is currently referencing.

**Notes:**

* Use the **Context** field to pass in **query text**, **user input**, or **data from preceding nodes**.
* Supports variables such as `${start.query}` or `${llm-nodeA.result}` to make responses more personalized or context-aware.
* While brief instructions can be placed here, the context field should focus on **content** rather than behavioral rules.

### **System Prompt**

> Purpose: Defines the model's behavior and role. Think of it as the "permanent job description" for this node.

**Notes:**

* Use it to define **who** the model is, **how it should act**, and **what task it should complete**.
* Instructions in the System Prompt take **priority over** instructions in the Context.
* It is recommended to always explicitly define:
  * **Role** (e.g., Product Manager, Analyst, Mentor)
  * **Task Goal** (e.g., write a report, explain code)
  * **Tone** (e.g., formal, friendly)
  * **Tool Usage Rules** (if tools are attached)

### **File Handling**

The **File Handling** setting allows users to define how the assistant handles uploaded files within the workspace. This is especially useful when the assistant needs to interpret, convert, or extract content from files (e.g., PDFs, DOCX files, images) during a conversation.

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="143">Option</th><th width="120">Visible to MCP Tools</th><th width="102">Visible to LLM</th><th>Description</th><th>Example Use Case</th></tr></thead><tbody><tr><td>No Processing</td><td>X</td><td>X</td><td>The file is uploaded but not visible to the LLM or MCP tools; it will not be opened or parsed.</td><td>–</td></tr><tr><td>Process with Tools Only</td><td>O</td><td>X</td><td>The file is passed to MCP tools for processing but is not provided to the LLM.</td><td>Suitable for cases where data needs to be extracted from a CSV or PDF without requiring AI commentary.</td></tr><tr><td>Convert File to Image</td><td>X</td><td>O</td><td>Converts the file to an image for the LLM to reference only.</td><td>Suitable for scanned documents or visual data where the layout structure needs to be referenced.</td></tr><tr><td>Convert to Image and Process with Tools</td><td>O</td><td>O</td><td>Simultaneously converts the file to an image for the LLM to reference and passes it to MCP tools for processing.</td><td>Suitable for invoices or forms that require both visual structure parsing and structured data extraction.</td></tr></tbody></table>
