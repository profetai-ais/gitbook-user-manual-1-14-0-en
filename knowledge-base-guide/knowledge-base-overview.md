# Knowledge Base Overview

## Introduction

The "Knowledge Base" feature in AI Studio provides application developers with an easy-to-use interface for managing personal or team knowledge, and can be seamlessly integrated into AI assistants. Developers can upload internal documents, FAQ, and standard operating guidelines, and have them processed into structured data that large language models (LLMs) can query.

Compared to the static pre-trained datasets built into AI models, the content in the knowledge base can be updated in real time, ensuring that LLMs always have access to the latest information and avoiding issues caused by outdated or missing data.

When an LLM receives a user query, the system uses Hybrid Search to find the most relevant content in the knowledge base. Hybrid Search combines the following signal sources and ranks results comprehensively:

* Full-text Search: Uses a database full-text index (Postgres) to find passages that closely match the query terms
* Vector Search: Uses semantic similarity to find content that conceptually matches the question, even if the exact terms do not appear
* Chunk Summary Index: Uses paragraph summary/key-point indexing to help locate key passages in long documents, improving the focus of retrieved results

The system returns highly relevant content chunks (Chunks) to the LLM as context, enabling the generation of more accurate and source-traceable answers. This approach ensures that the LLM does not rely solely on pre-trained knowledge, but also incorporates the latest internal documents and database content, reducing response bias caused by outdated or missing data.

<figure><img src="../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

## **Key Advantages**

* **Data Stays Internal**: Important corporate knowledge documents remain within the enterprise environment and do not leave the internal network.
* **Real-time Updates**: The knowledge base can be updated at any time, ensuring the model always has access to the latest information.
* **Accuracy**: By retrieving relevant documents, the LLM can generate responses based on actual information, reducing the risk of hallucination.
* **Flexibility**: Developers can customize the knowledge base content according to actual needs and define the required scope of knowledge.

Users only need to prepare text content, such as:

* Long-form text content (TXT, Markdown, DOCX, HTML, JSONL, or even PDF files)
* Structured data (CSV, Excel, etc.)

Simply upload the files to the **knowledge base**, and data processing will be completed automatically.

## **Use Cases**

If users want to build an AI customer service assistant based on an existing knowledge base and product documentation, simply upload the relevant files to the AI Studio knowledge base and then create an AI assistant.

Traditionally, training from raw text to developing a fully functional AI customer service chatbot could take weeks and is difficult to maintain and continuously improve. In AI Studio, the entire process takes only three minutes, and users can immediately begin collecting user feedback.

## Knowledge and Datasets

In AI Studio, the knowledge base is composed of multiple **Datasets**, and each **Dataset** can contain multiple Chunks. Users can integrate the entire knowledge base into the application as retrieval context, sourced from uploaded files or content synced from other data sources.
