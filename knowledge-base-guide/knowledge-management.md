---
description: Click a knowledge card on the knowledge base page to enter the settings page.
---

# Manage Knowledge

## **Page Navigation**

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="180">Action Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Back</td><td>Click to return to the knowledge base home page</td></tr><tr><td>2</td><td>Collapse</td><td>Click to minimize the menu area</td></tr><tr><td>3</td><td>Knowledge Settings Menu</td><td>Provides various knowledge settings and test functions</td></tr><tr><td>4</td><td>Settings Input Area</td><td>Opens the corresponding operation page based on the menu item selected by the user</td></tr></tbody></table>

## **Basic Settings**

Users can modify the name and description of the knowledge through Basic Settings.

Steps:

1. Click the _Basic Settings_ item in the "Knowledge Settings Menu"
2. Edit the text in the "Name" or "Description" field
3. Click "Save" to complete the settings

> Note: The Index Model cannot be changed after it has been selected when creating the knowledge base.

## **Dataset**

The Dataset settings page allows users to upload and manage files. The file types supported by AI Studio are:

* Long-form text content (e.g., TXT, Markdown, DOCX, HTML, JSONL, non-image-only PDFs, etc.)
* Structured data (CSV, Excel, etc.)

<figure><img src="../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="180">Action Name</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Edit Table</td><td>Allows users to edit the display format of the table</td></tr><tr><td>2</td><td>Refresh</td><td>Click to reload the table</td></tr><tr><td>3</td><td>Filter</td><td>Content can be filtered by field</td></tr><tr><td>4</td><td>My List</td><td>When enabled, only data created by the user will be displayed</td></tr><tr><td>5</td><td>Batch Download</td><td>Allows selecting multiple items at once for batch download</td></tr><tr><td>6</td><td>Delete</td><td>A delete button appears after checking datasets in the list; clicking it deletes the selected datasets</td></tr><tr><td>7</td><td>Search</td><td>Users can enter keywords to filter</td></tr><tr><td>8</td><td>Add / Import</td><td>Upload a file, or create an empty dataset</td></tr><tr><td>9</td><td>Actions</td><td>Users can edit or delete the corresponding dataset</td></tr></tbody></table>

## **Add Dataset**

<figure><img src="../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

1. Click the _Dataset_ item in the "Knowledge Settings Menu"
2. Click the "Add / Import" button and select _Import File_
3. Click the "Upload Area" to open the system window, select the file to upload, then click _Next_ when done
4. In the data processing section, users can select a strategy for splitting the file content using the "File Processing" options on the left. After clicking _Generate Segmentation Results_, a preview of the split data will be displayed on the right. After confirming the processing method, click _Next_
5. Confirm the content again, then click the "Upload" button to upload the file
6. The page returns to the dataset list. The data can be used once the file status column shows "Complete"

### File Upload Limits

To ensure data processing performance and index quality, the following limits apply when importing files into a dataset:

| Item | Limit |
| ---------- | -------------- |
| Maximum number of files per import | Up to **100** files |
| Maximum size per file | 300MB |

Additional notes:

* If either of the above limits is exceeded, the system will display a warning message and block the upload. Please adjust the number of files or split the files before re-importing.
* If the file is a large document (e.g., a long PDF / DOCX), it is recommended to remove unnecessary images or appendix content first to avoid excessively long processing times.

#### Download Access Control

The download behavior of a dataset's original files is affected by "Dataset Access Permissions":

* Authorized users: Can download/access the original files from the dataset list or Chunk view (subject to the operation buttons available on the screen).
* Unauthorized users: When attempting to download or access original files, the system will block the action and display an insufficient permissions message; some screens may not display the download entry or may set it as non-operable.

To authorize others to download/access dataset files, the administrator should go to the "# Dataset Access Permissions" section at the bottom of this page, add the organizations or users that can access the specified dataset, and save the settings.

#### Troubleshooting: Permission Settings Display Issues

If permission details are not displayed, the section is blank, or expanding shows no content on the "Dataset Access Permissions" page, try the following in order:

1. Click Refresh to reload the list, or switch to another menu and switch back.
2. Confirm that the target file/dataset has been selected in the Dataset area on the left.
3. Confirm that the current account has permissions to manage the knowledge base such as "AI Studio Administrator / Knowledge Base Administrator / Domain Expert / Collaborator"; if not, please contact an administrator for assistance.

### Dataset Status Information

Click on the status icon to view details. For detailed operation instructions, please refer to the [Work Management](../fen-xi-zhi-nan/gong-zuo-guan-li.md) page.

.

<figure><img src="../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

## **Data Processing When Adding a Dataset**

Data processing after file upload supports the following two forms:

* **Direct Segmentation**: Applies user options for segmentation
* **QA Segmentation**: For documents with Q\&A content, segmentation is done by question

#### **Direct Segmentation**

When the original content has no clear Q&A structure, or when the user wants to quickly build data segments, "Direct Segmentation" mode can be enabled. The system will automatically split paragraphs according to the settings.

<table><thead><tr><th width="180">Processing Method</th><th>Description</th></tr></thead><tbody><tr><td>Automatic</td><td>The system defaults to automatic segmentation based on the length and linguistic structure of the input content. Suitable for getting started quickly without needing custom rules. When no splitting method is specified, the system performs initial segmentation using common symbols such as line breaks and periods.</td></tr><tr><td>Token Segmentation</td><td>Splits text based on the configured segment token length. It is recommended to keep a single segment within 100–1000 tokens to avoid fragmented semantics or truncated context.</td></tr><tr><td>Custom Rules</td><td>Provides more granular control. In addition to paragraph length (recommended 100–1000) and Overlap Range (e.g., 100 tokens) settings, a delimiter option is added to control segmentation.</td></tr><tr><td>Regex Segmentation</td><td>Splits text using specific characters (e.g., <code>\\n</code>, <code>。</code>, <code>,</code>, <code>;</code>); multiple symbols can be combined and is suitable for general natural language processing scenarios.</td></tr></tbody></table>

<table><thead><tr><th width="180">Processing Options</th><th width="200">Applicable Segmentation Methods</th><th>Description</th></tr></thead><tbody><tr><td>Ideal Segment Length</td><td>Token Segmentation, Custom Rules</td><td>Sets the target length for each segment (in tokens). Smaller values produce finer segments but may weaken contextual links; larger values should be paired with an Overlap Range to maintain context consistency.</td></tr><tr><td>Overlap Range</td><td>Token Segmentation, Custom Rules</td><td>Defines the number of tokens that overlap between a segment and the previous one (e.g., 100), improving context continuity. The recommended value is between 1 and Ideal Segment Length - 1; suitable for multi-turn conversations, technical documents, and other high-context content.</td></tr><tr><td>Custom Delimiter</td><td>Custom Rules</td><td>Sets symbols to identify segmentation points, separated by semicolons. Example: setting <code>;; ;'';</code> will produce a segment when <code>;</code>, <code>(space)</code>, or <code>''</code> appear in the text.</td></tr><tr><td>Rules</td><td>Regex Segmentation</td><td>User-defined Regex syntax for segmentation. Users can click the preset segmentation examples below to edit: <code>.+\\n?</code> (line break segmentation), <code>[^。]+。?</code> (Chinese period segmentation).</td></tr><tr><td>Remove Trailing Newline</td><td>Regex Segmentation</td><td>Whether to automatically remove the trailing newline <code>\\n$</code> symbol at the end of a segment.</td></tr></tbody></table>

> Recommendation: Using Token Segmentation + Overlap Range can effectively preserve semantic and contextual integrity, preventing sentences from being cut off mid-way and causing information loss.

#### **QA Segmentation**

When processing Q&A document content (such as FAQs, customer service records, interview transcripts, etc.), QA segmentation settings can be used to improve structural recognition and semantic clarity. The system provides the following parameters to help identify and split question and answer blocks.

<table><thead><tr><th width="200">Option</th><th>Description</th></tr></thead><tbody><tr><td>Question Prefix</td><td>Specifies the identification string at the beginning of a question (e.g., <code>Q:</code>, <code>Question:</code>). The system will use this as the starting point for a new question segment.</td></tr><tr><td>Answer Prefix</td><td>Specifies the identification string at the beginning of an answer (e.g., <code>A:</code>, <code>Answer:</code>), used to mark the answer content corresponding to the question.</td></tr><tr><td>Remove Prefix</td><td>When enabled, automatically removes the marker strings at the beginning of question and answer segments (e.g., <code>Q:</code>, <code>A:</code>).</td></tr><tr><td>Prefix Expression</td><td>Supports using regular expressions (Regex) to identify question and answer prefixes, suitable for scenarios with inconsistent formats or large-scale data conversion. For example: <code>^Q[0-9]*:</code> can match multiple question numbers.</td></tr><tr><td>Remove Last Newline</td><td>When enabled, automatically removes extra newlines at the end of each QA block.</td></tr></tbody></table>

## **View / Edit Dataset**

Clicking a file name in the file list will open the _Chunk(s)_ view page, allowing users to browse the indexed data content and edit it as needed.

<figure><img src="../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

<table><thead><tr><th width="80">Item</th><th width="180">Option</th><th>Description</th></tr></thead><tbody><tr><td>1</td><td>Chunk(s) Tab</td><td>Displays the chunks generated after the file has been split</td></tr><tr><td>2</td><td>Reference Files Tab</td><td>Displays all files associated with the chunks, including the original files used for splitting and files used as reference data</td></tr><tr><td>3</td><td>Back</td><td>Click to return to the dataset home page</td></tr><tr><td>4</td><td>Search Bar</td><td>Allows users to enter text to search for related chunks</td></tr><tr><td>5</td><td>Add / Import</td><td>Click to manually add a chunk</td></tr><tr><td>6</td><td>Edit</td><td>Click to display the _Edit_ and _Delete_ operation options for the chunk</td></tr></tbody></table>

## **Edit Chunk Content**

Users can optimize chunk content to improve the accuracy of data cited by the LLM when generating responses, for example by adding possible question phrasings for Q\&A type chunks.

<figure><img src="../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

1. Click the "Edit" button on the chunk and select _Edit_
2. Click the "Edit" button in the upper-right corner of the pop-up window to open the editing interface fields
3. Click the "+" button to the right of the _Question_ heading to add a question
4. After entering the question content, click the "✔️" button in the upper-right of the interface to save the changes

## **Create Reference Files**

When AI Studio cites dataset content to generate responses, users can add related files as reference sources, such as specific pages and images from a PDF or PPT.

<figure><img src="../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

1. Click the "Reference Files" tab
2. Click the "+Create" button to open the system window, select the file to upload, then click _Confirm_
3. Confirm that the file has been uploaded correctly in the _Reference Files list_, then click the "Chunk(s)" tab
4. Click the "Edit" button on the chunk and select _Edit_
5. Click "Link File" on the left
6. Click the "+Create" button to open the add file window
7. Click the "File Menu" to select the reference file, then click _Confirm_ to complete creating the reference file attachment

## **Test**

After creating a dataset, users can use the Test function to ask questions, view which chunks' content was cited when generating the response, and score the search results by adjusting Retrieval Parameters, thereby optimizing the data content to improve citation accuracy.

<figure><img src="../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

1. Click the _Test_ item in the "Knowledge Settings Menu"
2. Click the _gear icon_ to the right of the "Retrieval Text" heading to open the Retrieval Parameters settings
3. It is generally recommended to check "Enable Scoring" below
4. Click the "LLM Scoring Model" menu to select the model to use
5. Adjust the "Score Threshold" setting to filter search results by score requirement; only results that meet the score requirement will appear as relevant information in the _Scoring Results_
6. Click the "Confirm" button to save the parameter settings
7. Enter the content/question to query in "Retrieval Text" and click the _Query_ button to submit
8. Search results will be listed under "Retrieved Results", sorted by retrieval score in descending order
9. Click any _Retrieved Result_ to view the full information, and click the "Index" tab to view the index the system used to retrieve that chunk
