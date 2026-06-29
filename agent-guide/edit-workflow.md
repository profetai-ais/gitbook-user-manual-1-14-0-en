# Edit Workflow

## **Page Navigation**

The image below shows the workflow editing interface, which includes the following controls:

<figure><img src="../.gitbook/assets/image (219).png" alt=""><figcaption></figcaption></figure>

1. **Node List**: Workflow functional components provided by AI Studio. See the [Workflow Nodes](gong-zuo-liu-cheng-jie-dian.md) page for details on available nodes.
2. **Workflow Toolbar**: Provides editor operations; see descriptions below
3. **Workflow Editing Area**: Drag and drop functional nodes here to edit the workflow
4. **Editor Minimap**: Helps users quickly navigate to specific areas of the editor

<table><thead><tr><th width="183">Workflow Toolbar Items (left to right per image above)</th><th>Description</th></tr></thead><tbody><tr><td>Undo, Redo</td><td>Go back to the previous step, or return to the next step</td></tr><tr><td>History</td><td>Manage the workflow's edit history</td></tr><tr><td>Export File</td><td>Export this workflow as a file</td></tr><tr><td>Show Minimap</td><td>Show or hide the minimap in the bottom-right corner</td></tr><tr><td>Reset View</td><td>Center and display the entire workflow</td></tr><tr><td>Collapse</td><td>Collapse all nodes in the editor</td></tr><tr><td>Edit Global Variables</td><td>Edit global variables in the workflow</td></tr><tr><td>Clipboard</td><td>Save selected nodes and retrieve them at any time</td></tr><tr><td>Save</td><td>Save workflow changes</td></tr><tr><td>Test Preview</td><td>Open a chat window to test the workflow (not shown when editing from a workflow template)</td></tr></tbody></table>

## **Create / Edit Workflow**

> Note: It is recommended to open the workflow editor from the agent settings so you can use Test Preview directly after editing.

<figure><img src="../.gitbook/assets/image (220).png" alt=""><figcaption></figcaption></figure>

Using a blank workflow as an example, the canvas defaults to a single **"Start"** node. Clicking this node displays several basic variables:

| Variable Name                  | Description                                     | Sample Value                                        |
| ------------------------------ | ----------------------------------------------- | --------------------------------------------------- |
| `(x)${{start}.{query}}`    | The user's input prompt                         | _User input, e.g.:_ `summarize the attached document` |
| `(x)${{start}.{files}}`    | List of files attached by the user in chat      | `metadata of the files in a JSON array`             |
| `(x)${{start}.{time}}`     | Current system time                             | `17:19:13`                                          |
| `(x)${{start}.{date}}`     | Current system date                             | `2025-06-06 Friday`                                 |
| `(x)${{start}.{dateTime}}` | Current system date and time                    | `2025-06-06 Friday 17:19:13`                        |

Here is a simple example demonstrating basic workflow operations:

<figure><img src="../.gitbook/assets/image (221).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (222).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (223).png" alt=""><figcaption></figcaption></figure>

1. In the new workflow, click the "Start" node to view the basic variables
2. Drag the "Reply" node from the node list into the editing area
3. Connect the output of the "Start" node to the input of the "Reply" node
4. This example will display the contents of the basic variables. Click the "Reply" node to open its edit window and edit the assistant's response in the input area
5. Typing "/" will display a list of available workflow variables — refer to the table above to select the variable to display in the reply
6. After editing, click the "Save" button in the toolbar, then click "Test Preview" to test the workflow
7. Attach a file and enter a prompt in the "Test Preview" chat area and submit — you can see the assistant's processing steps in real time
8. Once the assistant finishes processing, you can expand the "Reply" item in the chat to view the workflow result

Follow these steps to try different nodes and build a workflow that fits your application needs!

### Example Scenario

#### Workflow Nodes (Fork / Merge) — News Search Agent

This scenario demonstrates how a single user query can trigger parallel searches across multiple data sources simultaneously, with results automatically merged and summarized by AI. The Fork and Merge design significantly improves data collection and analysis efficiency, making complex workflows fast and clear.

{% file src="../.gitbook/assets/Understanding Fork & Merge Nodes_ A News Search Agent_2026-02-02_影片.mp4" %}

## Node Copy and Paste (Clipboard Copy / Paste)

Workflows support quick node copy and paste, useful for creating multiple similar nodes or moving existing logic across workflows.

<figure><img src="../.gitbook/assets/image (224).png" alt=""><figcaption></figcaption></figure>

How to use:

* Select one or more nodes on the canvas
* Use the copy/paste operation
* The pasted nodes appear on the canvas with the same settings and can be fine-tuned as needed

Additional behavior notes:

* Cross-workflow copy/paste: You can copy nodes from workflow A and paste them into workflow B to speed up assembly.
* Batch operations: You can select multiple nodes at once for copy/paste, preserving their configuration.
* Naming conflicts: If duplicate node names or variable names appear after pasting, the system may require you to rename them before saving (follow the prompts to fix this).

> Note: If a node's configuration references "output variables from other nodes," pasting it into a new workflow may cause resolution failures due to missing upstream node connections. It is recommended to check all connections and variable references after pasting.

## Local Storage Draft Sync

To prevent losing edits due to browser refresh or unexpected closure, the editor saves draft state locally (Local Storage) and syncs it across multiple tabs.

<figure><img src="../.gitbook/assets/image (225).png" alt=""><figcaption></figcaption></figure>

## History

History saves every version the user explicitly saves by clicking the Save button. Users can review past edit history and restore an older version via undo.

> Note: Content is only recorded in history when you click the Save button in the top-right corner.

<figure><img src="../.gitbook/assets/image (226).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (227).png" alt=""><figcaption></figcaption></figure>

![](<../.gitbook/assets/image (228).png>)

1. Click "History" in the workflow toolbar
2. The left side of the popup shows a live preview
3. The right side shows the version history — click a card to switch to a different version.
   1. A maximum of 21 saved history entries are kept; when the 22nd is saved, the oldest entry is deleted
   2. To preserve a specific history entry, click the pin icon to save it as a fixed version. A maximum of 20 pinned versions can exist
4. Click the version you want to switch to
5. Click "Restore" to apply it to the workflow

## Edit Global Variables

Global variables can be thought of as "shared constants/settings for this workflow." They are ideal for content that is reused across multiple nodes, such as company policies, tone guidelines, fixed formats, reply template snippets, default API parameter values, etc. Centralizing these avoids making repeated edits across multiple nodes.

<figure><img src="../.gitbook/assets/image (229).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (230).png" alt=""><figcaption></figcaption></figure>

1. Click "Edit Global Variables" in the workflow toolbar
2. Add or edit variable content in the popup
3. When done, click "Save" to apply to the workflow

### Add / Edit Variables

* Name: The identifier used for referencing, only numbers and English letters are allowed.
* Content: The variable value itself, which can be multi-line text (e.g., guidelines, templates, paragraphs).

> Note: If a variable name is changed, the system will sync-update all references within the workflow (though it is still recommended to verify based on actual on-screen prompts). If you have manually copy-pasted a variable as plain text into node content, that text is not treated as a variable reference and must be updated manually.

### Reference Global Variables in Nodes

In node settings (e.g., the "Context" field or other input fields of an LLM node), type `/` to insert available global variables from the list. Once inserted, the system renders them as variable expressions, which automatically populate with the latest value going forward.

<figure><img src="../.gitbook/assets/image (231).png" alt=""><figcaption></figcaption></figure>

### Reference Global Variables in System Prompts

When you want multiple LLM nodes to share consistent roles, tone, or output guidelines, it is recommended to write the guidelines into a global variable and reference that variable directly in each node's System Prompt.

Benefit: When the guidelines change, you only need to update them once, and the change applies to all referencing nodes.

> Note: If you see a "Variable cannot be resolved / reference failed" prompt when saving, please confirm:

1. The variable name contains no special characters or reserved words
2. The node field supports variable references
3. The variable was saved successfully

>

### Example Scenario

#### Global Variables — Localization Translation Agent

This scenario demonstrates how setting a global variable once can control the output behavior of all AI nodes in the entire workflow, such as the output language. Users do not need to modify each node individually — they can quickly switch between Chinese, English, or other languages, ensuring consistent output across the board. This is especially suited for multilingual or cross-regional applications.

{% file src="../.gitbook/assets/Understanding Global Variables A Localization Agent_2026-02-04_影片.mp4" %}
