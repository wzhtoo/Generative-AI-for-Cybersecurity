# 01_Choosing the Right Technology Stack for LLM Applications

[👉VIDEO_Choosing the Right Technology Stack for LLM Applications &#128279;](https://codered.eccouncil.org/courseVideo/generative-ai-for-cybersecurity-course?lessonId=3876add2-8705-4ebd-a383-61e3df329ace&finalAssessment=false)

# Tech Stacks

- **Azure**:  
  Azure AI Studio, Cognitive Search, Data Fabric, Semantic Kernel

- **Google**:  
  Vertex AI, Generative AI Studio, PaLM APIs, Gemini multimodal

- **Amazon**:  
  Bedrock ML and Foundation Models

- **Other Tools**:  
  Langchain, AutoGPT, PineCone, LlamaIndex, and open-source LLMs, etc.

---

## Azure AI Studio Features

- Build and train your own models
- Ground Azure OpenAI Service and OSS models using your data
- Built-in vector indexing
- Retrieval-augmented generation made easy
- Create prompt workflows
- AI safety built-in

# AWS vs. Google vs. Azure: Generative AI Capabilities

| **GenAI Category**               | **GenAI Component** | **Amazon Web Services (AWS)**            | **Google Cloud**         | **Microsoft Azure**          |
| -------------------------------- | ------------------- | ---------------------------------------- | ------------------------ | ---------------------------- |
| **Runtime**                      |                     | Amazon Bedrock                           | Vertex AI                | Azure OpenAI                 |
| **Foundation Models**            | Text / Chat         | TBD                                      | PaLM                     | GPT                          |
|                                  | Code                | TBD                                      | Codey                    | GPT                          |
|                                  | Image Generation    | TBD                                      | Imagen                   | DALL-E                       |
|                                  | Translation         | TBD                                      | Chirp                    | None                         |
| **Model Catalog**                | Commercial          | Amazon SageMaker JumpStart, Amazon Titan | Vertex AI Model Garden   | Azure ML Foundation Models   |
|                                  | Open Source         | Amazon SageMaker JumpStart, Hugging Face | Vertex AI Model Garden   | Azure ML Hugging Face        |
| **Vector Database**              |                     | Amazon RDS (pgvector)                    | Cloud SQL (pgvector)     | Azure Cosmos DB, Azure Cache |
| **Model Deployment & Inference** |                     | Amazon SageMaker                         | Vertex AI                | Azure ML                     |
| **Fine-tuning**                  |                     | Amazon Bedrock                           | Vertex AI                | Azure OpenAI                 |
| **Low-code/No-code Development** |                     | TBD                                      | Gen App Builder          | Power Apps                   |
| **Code Completion**              |                     | Amazon Code Whisperer                    | Duet AI for Google Cloud | GitHub Copilot               |

---

## Additional Insights:

### **Amazon Web Services (AWS)**:

- **Amazon Bedrock**: Provides foundational runtime and supports various GenAI components.
- **Amazon SageMaker**: Enables both commercial and open-source model deployment, including integrations with Hugging Face.
- **Amazon Code Whisperer**: Focused on improving developer productivity through AI-assisted code completion.
- **TBD**: Several GenAI capabilities (e.g., text/chat, image generation) remain under development.

### **Google Cloud**:

- **Vertex AI**: Central platform for AI model deployment and inference, including fine-tuning.
- **PaLM**: Google’s advanced language model for text/chat capabilities.
- **Imagen**: Specializes in AI-powered image generation.
- **Gen App Builder**: A low-code platform for building applications integrated with GenAI.

### **Microsoft Azure**:

- **Azure OpenAI**: Hosts state-of-the-art language and image generation models like GPT and DALL-E.
- **Azure ML**: Supports model cataloging, fine-tuning, and deployment.
- **GitHub Copilot**: Integrates seamlessly with Azure for AI-assisted code completion.
- **Power Apps**: Enables low-code application development.

---

This comparison highlights the distinct strengths and focus areas of AWS, Google Cloud, and Microsoft Azure in the GenAI ecosystem. Let me know if you’d like deeper insights on any specific category!

# Azure OpenAI Tool Set

## **Overview**

The Azure OpenAI Tool Set enables seamless integration of AI-powered tools for applications, leveraging both text and image embeddings, cognitive search, and vector indexing for comprehensive functionality.

---

## **Diagram: Workflow**

1. **App UX**:
   - The user interface interacts with the system.
2. **App Server (Orchestrator)**:
   - Acts as the intermediary, processing and forwarding requests.
3. **Azure Cognitive Search**:
   - Handles queries by retrieving knowledge from indexed data sources (files, databases, etc.).
4. **Azure OpenAI (GPT/ChatGPT)**:
   - Combines the query with retrieved knowledge to generate a response.
5. **Data Sources**:
   - Includes files, databases, and other structured or unstructured data formats.

---

## **Core Components**

### 1. **Azure OpenAI**:

- Text embedding models for generating embeddings that enhance search and semantic understanding.

### 2. **Image Retrieval Vectorize Image API**:

- Enables the generation of image embeddings, enhancing image-based queries and AI-powered visual recognition.

### 3. **Azure Cognitive Search**:

- Automates the indexing of vector data from:
  - Azure Blob Indexers
  - Azure Cosmos DB (for NoSQL data indexing)

### 4. **LangChain**:

- Simplifies the development of LLM-powered applications.
- Uses Azure Cognitive Search as the vector datastore for efficient data retrieval.

### 5. **Semantic Kernel SDK**:

- Integrates LLMs with programming languages for:
  - Document chunking
  - Advanced semantic tasks

---

## **Key Benefits**

- **Unified Workflow**: Combines search, embeddings, and LLM processing into a single pipeline.
- **Extensibility**: Compatible with a wide range of data sources (SQL, NoSQL, Blob storage).
- **Developer Support**: Tools like LangChain and Semantic Kernel SDK make it easier for developers to integrate and utilize advanced AI capabilities.

# Building LLM-Powered Apps with OPL or OpCL Stack

Developing applications powered by large language models (LLMs) can be done efficiently while prioritizing privacy by using the OPL or OpCL stack. Here’s an overview:

## OpCL Stack Components

The OpCL stack replaces proprietary tools with open-source alternatives to ensure privacy and control over the data.

1. **Open-Source LLMs**  
   Use open-source large language models such as those provided by [Hugging Face Transformers](https://huggingface.co/transformers). These allow for fine-tuning and deployment on your infrastructure without external dependencies.

2. **C: Chroma (Mivus)**  
   Chroma serves as a vector database (alternative to Pinecone) to store embeddings and enable fast similarity searches. It is a self-hosted solution designed for scalability and privacy.

3. **L: LangChain**  
   LangChain provides a robust framework for interacting with LLMs, including support for:
   - **Models**: Integration with open-source and proprietary LLMs
   - **Prompts**: Efficient prompt engineering
   - **Indexes**: Advanced indexing for knowledge retrieval
   - **Memory**: Storing conversational context
   - **Chains**: Creating workflows involving multiple tasks
   - **Agents**: Combining tools and models to dynamically execute tasks

## OPL Alternative

The OPL stack utilizes:

- **O (OpenAI)**: Large language models such as GPT-3, GPT-3.5 (ChatGPT), or GPT-4 for processing and generating text.
- **P (Pinecone)**: A managed vector store for fast retrieval and knowledge base management.
- **L (LangChain)**: As described above, LangChain ties the components together with its flexible framework.

## Why Choose OpCL?

- **Privacy**: Replacing OpenAI with open-source LLMs and Pinecone with Chroma allows for complete data control.
- **Customization**: Open-source models and tools enable customization tailored to specific use cases.
- **Cost-Effectiveness**: Avoid recurring fees associated with managed services like OpenAI or Pinecone.

## Example Use Cases

- **Knowledge Base Applications**: Develop apps that retrieve and summarize information from large document collections.
- **Conversational Agents**: Build chatbots or virtual assistants with domain-specific knowledge.
- **Automated Workflows**: Create end-to-end pipelines for generating, summarizing, or analyzing text using LangChain’s chaining capabilities.

> **Tip**: Always evaluate the performance of open-source LLMs to ensure they meet the requirements of your application.

By leveraging the OpCL stack, developers can create powerful, private, and cost-effective LLM-powered applications tailored to their needs.

# The Current LLM Tech Stack

The landscape of Large Language Model (LLM) development and deployment consists of several interconnected layers. Each layer focuses on a specific aspect of building, fine-tuning, deploying, and leveraging LLMs for applications across various domains.

---

## 1. **Application Layer**

This is the front-end layer where LLM-powered tools and applications are delivered to users. It includes both **newly created applications** and **reimagined existing tools** enhanced by foundation models.

### Key Examples:

- **New Applications**: Jasper, HyperWrite, Runway, Adept, Tome
- **Existing Tools with LLM Enhancements**: Notion, Microsoft, Adobe, ChatGPT, GitHub Copilot

### **Opportunity**:

- The explosion of LLM-powered applications will lead to the reimagining of virtually all kinds of tools and workflows.
- Differentiation will come from how foundation models are fine-tuned to fit specific use cases.

---

## 2. **Tooling Layer**

This layer helps developers build LLM applications faster by offering orchestration frameworks, evaluation tools, and data connections.

### Categories:

- **Orchestration**: Tools like LangChain, Dust, and GPtIndex enable easy interaction between models, prompts, and external systems.
- **Evaluation**: Platforms such as Humanloop and WhyLabs provide metrics to measure model effectiveness and safety.
- **Data Sources & Actions**: External databases and APIs for integrating real-world data and actions into LLM-powered apps.

### **Opportunity**:

- Tooling frameworks are emerging as critical components for developers to build and iterate on applications.
- These tools make it easier to add data, evaluate performance, and implement models faster.

---

## 3. **Foundation Model Layer**

This is the core layer where large language models (LLMs) and their training datasets are developed.

### Categories:

- **Proprietary Foundation Models**: Developed by companies like OpenAI, Anthropic, Cohere, and AI21 Labs. Examples include GPT-4 and Claude.
- **Open-Source Models**: Tools like Hugging Face Transformers and models such as Stable Diffusion, Bloom, OPT, and GLM-130B.
- **Open-Source Data Sources**: Datasets like LAION, The Pile, and Common Crawl form the backbone of LLM training.

### **Opportunity**:

- A rivalry is emerging between proprietary and open-source models, similar to the competition between iOS and Android.
- Open-source models allow developers to customize and train models for specific needs while proprietary models focus on pre-trained robustness and convenience.

---

## 4. **FM Operations (FM Ops)**

This layer enables the efficient deployment, optimization, and maintenance of foundation models.

### Components:

- **Deployment Optimization**: Tools like OctoML help optimize model deployment for performance and cost efficiency.
- **Inference Platforms**: Modal, Banana, and other frameworks provide infrastructure for running models in production.
- **Training**: Platforms such as MosaicML, Lightning, and Cerebras focus on fine-tuning models for specific tasks.
- **Data Tooling**: Tools like Snorkel and Fastdup enhance data quality for model training.

### **Opportunity**:

- FM Ops are critical for sophisticated teams to achieve efficient scaling and cost-effective model operations.
- These platforms support differentiation by enabling faster deployments and more control over model behavior.

---

## 5. **Cloud Infrastructure**

Cloud platforms form the backbone of LLM operations, offering scalable computing and storage for model training, fine-tuning, and inference.

### Major Players:

- Microsoft Azure
- Amazon AWS
- Google Cloud

### **Opportunity**:

- The strategic importance of FM apps is driving developers' cloud platform choices. Providers with LLM-optimized solutions gain a competitive edge.

---

## 6. **Silicon Layer**

Hardware is the foundation for LLM training and inference, with GPUs and AI-specialized silicon chips being the most critical components.

### Major Players:

- NVIDIA
- AMD
- Amazon (SambaNova)
- Google (TPUs)
- Cerebras (AI-dedicated chips)

### **Opportunity**:

- Access to advanced hardware accelerates training times and reduces costs.
- The availability of GPUs and custom silicon chips determines an organization's ability to develop and scale LLMs effectively.

---

## Summary of Opportunities

1. **Application Innovation**: Every category of application will likely be reimagined to integrate the capabilities of LLMs.
2. **Tooling Differentiation**: Developing better tooling frameworks will drive developer productivity and application performance.
3. **Open vs. Proprietary Models**: Teams will choose between open-source flexibility and proprietary ease-of-use based on their needs.
4. **Operational Efficiency**: FM Ops solutions are critical for fine-tuning cost structures and scaling LLM deployments.
5. **Cloud Alignment**: Cloud providers with LLM-focused offerings will influence the broader landscape of app development.
6. **Hardware Access**: The supply of GPUs and other silicon technologies remains a critical factor in the LLM ecosystem.

---

This tech stack highlights the interconnected components required to build, deploy, and maintain LLM-powered applications, along with the opportunities for innovation and differentiation across each layer.
