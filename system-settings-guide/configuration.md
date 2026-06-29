---
description: The "Configuration" module is primarily used to manage the system's default behavior settings, including GPT default configurations and default system prompt related items.
---

# Configuration

## Translation

Controls the settings for multilingual translation and other related translation features.

<figure><img src="../.gitbook/assets/image (412).png" alt=""><figcaption></figcaption></figure>

## **Related Questions**

The Related Questions feature uses LLM-generated replies to produce related questions that users can click to execute a Q&A session. Administrators can modify the generation settings for related questions.

<figure><img src="../.gitbook/assets/image (274).png" alt=""><figcaption></figcaption></figure>

## Generate Title

Used to automatically generate a title based on user input. The system first identifies the input language, then generates a concise and thematic title.

<figure><img src="../.gitbook/assets/image (275).png" alt=""><figcaption></figcaption></figure>

## **Memory Settings**

### **Memory Language Model**

Used to configure the language model for Personalization-related content found in the avatar in the upper right corner of the screen. Users can select the appropriate language based on actual usage context, such as English or Chinese.

<figure><img src="../.gitbook/assets/image (416).png" alt=""><figcaption></figcaption></figure>

### **Memory Embedding Model**

Used to configure the embedding model for Personalization found in the avatar in the upper right corner of the screen, specifically for vectorizing Memory content and writing it to the database.

<figure><img src="../.gitbook/assets/image (415).png" alt=""><figcaption></figcaption></figure>

### User Memory Tool

Used to configure how AI judges, stores, updates, or deletes user memory, helping the system retain preferences and information for long-term use within the bounds of security rules.

<figure><img src="../.gitbook/assets/image (417).png" alt=""><figcaption></figcaption></figure>

### Agent Memory Extraction

Used to configure how AI extracts reusable task execution experience from conversations, helping the Agent retain validated processes, rules, and operating methods.

<figure><img src="../.gitbook/assets/image (418).png" alt=""><figcaption></figcaption></figure>

## Voice Settings

Defines the rules and constraints required for transcription when using the speech-to-text feature in the workspace.

<figure><img src="../.gitbook/assets/image (419).png" alt=""><figcaption></figcaption></figure>

## **Skill Scan Settings**

Used to control whether the scan mechanism is enabled when uploading skills. When enabled, the system will scan skills upon upload; when disabled, no scanning will be performed at upload time.

<figure><img src="../.gitbook/assets/image (420).png" alt=""><figcaption></figcaption></figure>

## Command Rewriting Settings

Command Rewriting Settings automatically restructures raw user-input commands into clearer, more structured, and executable prompts. While preserving the original intent, the system removes ambiguity and redundancy, supplements necessary formatting, tone, length, or language constraints, and organizes multi-step requirements into clear action instructions, enabling downstream models to understand and execute tasks more accurately.

<figure><img src="../.gitbook/assets/image (421).png" alt=""><figcaption></figcaption></figure>

## Canvas Settings

**Canvas Settings** determines whether a user's request requires canvas-related features to be activated, and automatically routes the request to the appropriate processing workflow. When the request involves charts, flowcharts, relationship diagrams, interactive UIs, or web application descriptions, the system will prioritize routing it to the canvas design feature. If the request includes HTML generation, it will also be handed off to the code editing feature via a designated workflow. If the request does not fall within the scope of visualization or web applications, the standard response process is maintained to avoid unnecessarily activating canvas features.

<figure><img src="../.gitbook/assets/image (422).png" alt=""><figcaption></figcaption></figure>

## Log Analysis

Log Analysis is used to configure how AI evaluates logs, including the judgment method and output format, helping the system assess overall health based on information such as errors, trends, availability, and performance.

<figure><img src="../.gitbook/assets/image (423).png" alt=""><figcaption></figcaption></figure>

## AI Cron Settings

Used to configure how AI converts natural language scheduling descriptions into Spring CronExpressions, helping users quickly generate usable scheduling rules.

<figure><img src="../.gitbook/assets/image (424).png" alt=""><figcaption></figcaption></figure>

## Default Models

Used to configure the display order of models in the model list. The order is displayed sequentially based on the permissions each user has to invoke them.

<figure><img src="../.gitbook/assets/image (425).png" alt=""><figcaption></figcaption></figure>
