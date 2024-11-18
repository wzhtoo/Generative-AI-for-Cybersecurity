# 02_Tools for Emaluating Open-sourced LLMs

[👉Tools for Emaluating Open-sourced LLMs &#128279;](https://codered.eccouncil.org/courseVideo/generative-ai-for-cybersecurity-course?lessonId=f25c6637-e8a3-47e9-8463-2da45fba674f&finalAssessment=false)

# Hugging Face Overview

Hugging Face is a leading platform for machine learning models, offering tools and resources to simplify the development and deployment of state-of-the-art models.

## Key Features

- **Website**: [Hugging Face Models](https://huggingface.co/models)
- **Model Repository**:
  - Over **80,000+ Transformers models** available.
  - Includes models for tasks such as natural language processing, computer vision, and audio.

## Hugging Face Endpoints Architecture

Hugging Face provides a secure and flexible architecture to deploy and use models via endpoints. Below are the access modes:

### 1. **Public**

- Open access secured with **TLS/SSL**.
- Suitable for general use cases where public access is sufficient.

### 2. **Protected**

- Requires authentication with a Hugging Face **API Token**.
- Adds a layer of security for sensitive applications.

### 3. **Private**

- Direct intra-region **VPC (Virtual Private Cloud)** connection.
- Designed for high-security environments.
- Uses **AWS PrivateLink** for secure communication between customer VPCs and Hugging Face endpoints.

## Use Case Integration

- Applications (e.g., **App1**, **App2**, **App3**) can connect to Hugging Face endpoints with varying security protocols.
- Options include encrypted connections, authenticated access, and private networking.
- Example: Deployment in **AWS us-east1** for optimized regional access and minimal latency.

## Why Use Hugging Face?

1. **Extensive Model Library**:

   - Offers pre-trained models for quick implementation.
   - Supports fine-tuning for custom applications.

2. **Secure Deployment**:

   - Provides options for encrypted and private model usage.
   - Meets the needs of industries requiring strict compliance, such as finance and healthcare.

3. **Flexibility**:
   - Accessible via API for seamless integration into applications.
   - Multiple security levels to suit diverse project requirements.

Hugging Face empowers developers and organizations to leverage machine learning efficiently with its robust model ecosystem and secure deployment options.

# AnyScale Aviary Overview

**AnyScale Aviary** is an advanced platform designed for exploring and comparing various Large Language Models (LLMs) efficiently. It provides tools to study and evaluate models based on performance metrics.

## Key Features

- **Website**: [Aviary Explorer](https://aviary.anyscale.com/)
- **Purpose**:
  - A hub for comparing different LLMs.
  - Helps researchers and developers choose the best model for their specific use cases.

## Aviary Explorer

### Features:

1. **Comparison**:
   - Directly compare the performance of multiple LLMs across various benchmarks.
2. **Leaderboard**:
   - Displays rankings of models based on user votes, contention, and win ratio metrics.
3. **Model Metrics**:
   - **Votes**: Indicates the popularity or user preference.
   - **In Contention**: The number of times the model was part of a head-to-head comparison.
   - **Win Ratio**: A metric indicating model performance in comparisons.

### Example Models on the Leaderboard:

| **Model**                               | **Votes** | **In Contention** | **Win Ratio** |
| --------------------------------------- | --------- | ----------------- | ------------- |
| lmsys/vicuna-33b-v1_3                   | 6         | 7                 | 2099          |
| lmsys/vicuna-13b-delta-v1_1             | 4         | 6                 | 1666          |
| mosaicml/mpt-30b-chat                   | 44        | 70                | 1479          |
| OpenAssistant/oasst-sft-7-llama-30b-xor | 146       | 312               | 1400          |
| mosaicml/mpt-7b-chat                    | 386       | 856               | 1351          |

## Why Use AnyScale Aviary?

1. **Comprehensive Model Analysis**:
   - Quickly identify the most effective model for specific applications.
2. **Dynamic Metrics**:
   - Regular updates with live statistics to reflect real-time performance trends.
3. **Community Insights**:

   - Incorporates user feedback through votes to highlight preferred models.

4. **Ease of Use**:

   - Simple interface to explore and evaluate LLMs.

5. **Research-Friendly**:
   - Facilitates studying the behavior of "stochastic parrots" and their performance across diverse datasets.

## Conclusion

AnyScale Aviary empowers developers and researchers to navigate the growing landscape of LLMs. By providing detailed comparisons and insights, it ensures the selection of the most suitable model for any task or domain.
