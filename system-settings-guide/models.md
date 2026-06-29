---
description: >-
  AI Studio allows IT personnel to connect externally subscribed large language model (LLM) services, such as ChatGPT or
  Gemini, or to configure integration with self-hosted large language models deployed on private compute resources.
---

# Models

## **Add Large Language Model**

<figure><img src="../.gitbook/assets/image (270).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (271).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (272).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (273).png" alt=""><figcaption></figcaption></figure>

1. Once inside, click the "＋ Add" button in the upper right corner to begin configuration.
2. Select a Provider (e.g., OpenAI / Azure / Gemini / Ollama / Claude)
3. Configure the settings based on the selected provider:
   1. Name: Customizable; this will be the model's display name within the system.
   2.  Model: Enter the model to use.

       > Note: Please fill in manually — the system will not automatically list options. (e.g., `gpt-5`, `gpt-4o`, `gemini-pro`, `llama3-70b`, etc.)
       >
       > For example, if the model name is mistyped as `gpt-6`, an error message will appear during Agent testing:
       >
       > Received Model Group=gpt-6
       >
       > Available Model Group Fallbacks=None
       >
       > Mode: If users enter the model manually, users will need to separately select a Mode (e.g., Chat / Embedding).
   3.  API Base: Enter the API Key provided by the provider.

       > Note: If entered incorrectly, the system will return an authorization error.
       >
       > * OpenAI: Enter only the API prefix. For example: `https://api.openai.com/v1`
       > * Gemini: No API Base URL is needed; the system will handle routing automatically.
   4. API Key: Enter the API Key.
   5. Organization: Optional. Can be left blank for general keys; some OpenAI short keys may require this field.
4. Advanced Settings
   1. If using a **Cloud Model** → It is recommended to leave this blank and let the system automatically update to the latest pricing.
   2. If using a **Self-hosted Model** → Users may evaluate whether to manually enter the rate.
5. Click Create to complete the configuration.

### FAQ: Model Logo Does Not Match Actual Provider

<figure><img src="../.gitbook/assets/image (304).png" alt="" width="561"><figcaption></figcaption></figure>

In the model management page, the model logo is displayed based on the Provider selected when the model was created.

For example: if OpenAI was selected as the provider when creating the model, the screen will display the GPT / OpenAI-related logo; if Azure OpenAI was selected, the Azure-related logo will be shown.

If the model is actually connected to an Azure API, but the provider field was set to OpenAI when the model was created, a situation may arise where "the Azure API is actually being used, but the GPT logo is displayed on screen."

This situation is a result of a difference between the provider selection at model creation time and the screen display logic. The model will still make calls based on the configured API URL, Key, and related parameters. If the model can successfully pass the connection test and function normally, it means the API integration is working correctly.

If users need the on-screen logo to match the actual provider, it is recommended to confirm that the provider field is set to the correct service source when adding or re-creating the model.

### **Model Configuration Settings**

<table><thead><tr><th width="186">Setting</th><th width="288">Description</th><th>Options</th></tr></thead><tbody><tr><td>Service Name</td><td>The name of the service providing the model</td><td><code>openai</code>, <code>gemini</code>, <code>ollama</code> (on-premises)</td></tr><tr><td>Mode</td><td>The type of the model</td><td><code>chat</code>, <code>embedding</code></td></tr><tr><td>Model</td><td>The model available from the service provider</td><td>e.g., <code>gpt-4.1</code>, <code>gemini-2.0-flash</code>, etc., depending on the configuration at system installation</td></tr><tr><td>Name</td><td>The name used to identify this model within AI Studio</td><td>Same as model by default; user input</td></tr><tr><td>Description</td><td>A description of the model</td><td>User input</td></tr><tr><td>API Key/API Base</td><td>Enter the key when selecting <code>openai</code> or <code>gemini</code> as the service; enter the model API service URL when selecting <code>ollama</code></td><td>User input</td></tr><tr><td>Custom Pricing (Advanced Settings)</td><td>Whether to provide model service pricing, used to calculate the cost of using generative AI</td><td>User option</td></tr><tr><td>Pricing Model (Advanced Settings)</td><td>How is the service priced?</td><td>Defaults to per million tokens</td></tr><tr><td>Input Cost (Advanced Settings)</td><td>Enter the cost amount</td><td>User input</td></tr><tr><td>Output Cost (Advanced Settings)</td><td>Enter the cost amount</td><td>User input</td></tr><tr><td>Enable Status</td><td>Enable/disable the model</td><td>User option</td></tr></tbody></table>

> Note: Once a model is created, the Service Name, Mode, and Model fields cannot be changed.

### Supported Model List

AI Studio currently supports multiple model integration sources, including:

* OpenAI
* Azure OpenAI
* Google / Gemini
* Ollama
* Anthropic Claude
* AWS Bedrock
* Google Vertex AI
* DeepSeek
* Mistral AI
* Cohere
* OpenRouter
* NVIDIA NIM
* GLM
* MiniMax
* Qwen

> Note: The above list primarily covers the model integration sources currently supported by AI Studio. In actual use, models can be deployed via Cloud or On-premise methods, and will depend on the customer's environment requirements, model licensing, API service availability, or private deployment conditions.

## Permissions

{% hint style="info" %}
The Models module is only accessible to AI Studio administrators, so there are no list permission settings.

For an introduction to AI Studio role permissions, please refer to [AI Studio Roles and Permissions](../ru-men-zhi-nan/ai-studio-jue-se-yu-quan-xian-shuo-ming.md).
{% endhint %}

### Model Permissions

For role permission descriptions, please refer to [Module Permission Role Introduction - Model Permissions](../ru-men-zhi-nan/quan-xian-gong-neng-jie-shao.md#mo-xing).

For permission configuration instructions, please refer to [Permission Operation Function Introduction - Object Role Permissions](../ru-men-zhi-nan/quan-xian-cao-zuo-gong-neng-jie-shao.md#jue-se-quan-xian).
