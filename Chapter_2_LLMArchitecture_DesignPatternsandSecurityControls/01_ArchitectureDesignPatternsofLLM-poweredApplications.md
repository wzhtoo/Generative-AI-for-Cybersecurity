# 01_ArchitectureDesignPatternsofLLM-poweredApplications

[👉VIDEO_Architecture Design Patterns of LLM-powered Applications &#128279;](https://codered.eccouncil.org/courseVideo/generative-ai-for-cybersecurity-course?lessonId=668446bc-da61-496e-a70c-725b4eeb6ca4&finalAssessment=false)

### Typical Architecture Design Patterns (Not Exhaustive)

- [ ] Prompt Engineering Only
- [ ] Prompt Engineerign + Fine Tuning
- [ ] Prompt Engineerign + ChatGPT Plug-ins and/or Function
- [ ] Build your own LLMs

# Prompt Engineering and LLM Control

## Access Controls

- **Vector embedding database, OpenAI API**
  - Prompt validation
  - Avoid prompt injection
  - Detect PII/PHI Data

## Misuse Detection

- Detect misuse

## Output Moderation

- Output moderation

## Monitoring

- Audit Logs and Monitoring

## What is Prompt Engineering?

Prompt Engineering enables developers to control LLM responses by providing instructions.

---

## Diagram

1. **Prompt Engineering**
2. **Vector Database as Index Database**
3. **OpenAI as LLM**

# Best Practices in Prompt Engineering for Developers

This guide provides essential practices to help developers effectively engineer prompts for AI systems.

## 1. Role-playing

Use role-playing to create context. Assign roles to the AI (e.g., "You are a cybersecurity analyst") to frame responses in a specific perspective.

## 2. System Message

Provide a system message to set the scene or theme for the AI. For instance, a system message might introduce the AI to a specific task or area of expertise.

Example:

> "Welcome to Cyber Security Role-play! Describe the scenario. I’ll generate prompts for your adventure."

## 3. User Instruction and Few-shot Examples

Include clear user instructions and example prompts to guide the AI's responses. This helps the AI understand the desired output format and tone.

Example Instructions:

- **Defend against a cyber attack:** "Prevent network breach! Act quickly to safeguard data."
- **Identify a social engineering attack:** "Unfamiliar caller asks for sensitive info. What action do you take?"
- **Investigate a data breach:** "Track breach source, reveal hacker's identity."

## 4. Context from Vector DB

Incorporate context from a vector database to provide the AI with specific, relevant information that can guide its responses.

## 5. Query (User Input)

Structure user input as a query to provide the AI with specific information or questions for a targeted response.

## 6. Output Formatting

Request specific output formats to improve the quality of responses. You can ask the AI to respond in lists, paragraphs, or concise statements.

Example:

> "Prompt in plain text format. Keep responses within 300 tokens."

## 7. Constraints

Impose constraints on the AI's responses, such as:

- Limiting response length (e.g., 20 tokens)
- Setting a specific tone (e.g., urgent, professional)
- Using simple language if necessary

## 8. Temperature and Max Tokens

Adjust the **temperature** and **max tokens** to control the creativity and length of the response:

- Lower temperature for more predictable responses.
- Limit max tokens to control response length.

Example:

> "Set temperature low and max tokens to 300."

## Example Prompt

**Prompt:** Cyber Security Role-playing System

**System Message:**
Welcome to Cyber Security Role-play! Describe the scenario. I’ll generate prompts for your adventure.

**User Instruction and Examples:**

1. **Defend against a cyber attack on a company's network.** Prompt in an urgent tone.
   - Example: "Prevent network breach! Act quickly to safeguard data."
2. **Identify a social engineering attack.** Limit response to 20 tokens.
   - Example: "Unfamiliar caller asks for sensitive info. What action do you take?"
3. **Investigate a data breach.** Prompt concisely.
   - Example: "Track breach source, reveal hacker's identity."

**Output Formatting:**
Prompt in plain text format. Keep responses within 300 tokens.

**Constraints:**
Ensure responses are 300 tokens or less. Use simple language. Set temperature low and max tokens to 300.

# Prompt Engineering + Fine Tuning of LLM (Large Language Models)

This document outlines the essentials of fine-tuning large language models to enhance their performance and tailor them to specific tasks.

## What and Why Fine-Tuning?

- **Fine-tuning** is the process of refining and adapting a pre-trained model on specific datasets to improve its performance.
- Benefits of fine-tuning:
  - **Adapts to specific domains**: Enables the model to specialize in certain industries or topics.
  - **Boosts task performance**: Enhances the model's effectiveness in targeted tasks.
  - **Saves computational resources**: Reduces the need for extensive retraining from scratch.
  - **Reduces model biases**: Adjusts the model to be more balanced and fair in its responses.
  - **Small data set**: Can often be achieved with a smaller dataset relative to initial training.

## Key Concepts

- **Foundation Models or Base Models**: Large pre-trained models that serve as a starting point for fine-tuning. These are typically trained on massive datasets to gain general language understanding.
- **LoRA (Low-Rank Adaptation)** and **QRoLa (Quantized and Regularized Low-Rank Adaptation)**: Techniques to efficiently fine-tune models by adapting only specific parts of the model, which can help reduce computational costs.

## Fine-Tuning Workflow

1. **Prepare Data**: Collect and preprocess the dataset you will use for fine-tuning.
2. **Choose Foundation Model**: Select a foundation model (FM) to fine-tune, such as through Azure AI Studio.
3. **Monitor Customization**: Check the status of your customized model during the fine-tuning process to ensure quality and alignment.
4. **Deploy Customized Model**: Deploy the fine-tuned model for use in applications or testing environments.
5. **Analyze Model Performance**: Evaluate the customized model’s performance to ensure it meets the desired specifications and improvements.

This workflow ensures that models are efficiently and effectively adapted for specific tasks, saving resources and improving task accuracy.

- [ ] Security Controls
  - Secure/Sanitize Data
  - Model validation
  - Secure Deployment of Model

# Prompt Engineering + ChatGPT Plugins and/or Function Calls

This guide covers the integration of ChatGPT plugins and function calls in prompt engineering, along with the necessary security and validation controls.

## Security Controls

To secure ChatGPT plugin and function calls, implement the following measures:

- **API Security**:

  - **OAuth/OIDC**: Use OAuth (Open Authorization) or OIDC (OpenID Connect) for secure access management.
  - **Rate Limit**: Control the frequency of API calls to prevent abuse and manage resources effectively.
  - **API Gateway**: Use an API gateway to manage and secure API traffic.

- **Validate 3rd Party Plugin and Function Deployment**:

  - Ensure that third-party plugins and function deployments of models comply with required regulatory and compliance standards.

- **Validate Data in Transit**:

  - Secure data transmission to protect sensitive information during API calls.

- **Validate Response**:
  - Check the accuracy and appropriateness of responses generated through plugins and function calls.

## ChatGPT Plugins and Function Calls

- **ChatGPT Plugin APIs**:

  - These APIs allow developers to integrate plugins into their applications, enabling real-time information retrieval and functionality within the ChatGPT environment.

- **Function Calling in ChatGPT**:
  - Function calling enables developers to specify particular functions for ChatGPT models to execute within an API call, allowing for more customized and controlled interactions.

## Workflow Diagram

1. **LLM Application**: The main large language model (LLM) application.
2. **OpenAI Model API**: Interface for interacting with the LLM.
3. **ChatGPT Plugins and Function Calls**:
   - Users can invoke either ChatGPT plugins or specific function calls.
4. **Processing**: The selected plugin or function processes the request.
5. **GPT-4**: Model processes the request and generates a response.
6. **Generating Final Response**: Combines outputs from plugins, functions, and the model to produce a final response.
7. **Output**: The final response is sent back to the user.

This setup ensures secure, compliant, and efficient use of plugins and function calls with ChatGPT.

# Sample Validation Tools

- [OpenAI Moderation Guide](https://platform.openai.com/docs/guides/moderation)
- [Guardrails by ShreyaR](https://github.com/ShreyaR/guardrails)
- [NVIDIA NeMo-Guardrails](https://github.com/NVIDIA/NeMo-Guardrails?nvid=nv-int-tblg-635001#cid=dl28_nv-int-tblg_en-us)

# Training Your LLM from Scratch

## Key Components

- **Security Controls**
  - Secure/Sanitize Data
  - Model Validation
  - Secure Deployment of Model
  - LLM Ops: part of DevSecOps
  - Unlearning

## Process Flowchart

The diagram illustrates the workflow for training and monitoring a Large Language Model (LLM):

1. **Training**

   - Corpus Collection
   - Data Preprocessing & Cleansing
   - Tokenization
   - Feature Extraction
   - Data Splitting
     - Validation Set
     - Training Set
   - LLM Model Training
   - Model Evaluation

2. **Monitoring**
   - Anomaly Detection
     - Alert If Anomaly
     - Check if Model Update is Needed
       - If Yes: Update the Model
       - If No: Continue Monitoring
   - Model Performance Metrics
