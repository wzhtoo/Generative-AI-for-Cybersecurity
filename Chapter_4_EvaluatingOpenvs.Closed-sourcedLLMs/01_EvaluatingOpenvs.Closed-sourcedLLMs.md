# 01_Evaluating Open vs.Closed-sourced LLMs

[👉VIDEO_Evaluating Open vs.Closed-sourced LLMs &#128279;](https://codered.eccouncil.org/courseVideo/generative-ai-for-cybersecurity-course?lessonId=b2477f20-c977-42af-84a1-959d69d9c822&finalAssessment=false)

# Open-source vs. Closed-source LLM

| **Feature**                | **Open-source**            | **Closed-source (e.g., OpenAI)** |
| -------------------------- | -------------------------- | -------------------------------- |
| **Quality of LLM**         | From low to medium         | High                             |
| **Test/Alignment Quality** | From low to medium         | High                             |
| **Ownership**              | High                       | None for the latest model        |
| **License Cost**           | Zero if selected carefully | High                             |
| **Operation Cost**         | High                       | Low                              |
| **Security**               | Can be high                | Depends                          |

---

## Additional Information:

### 1. **Quality of LLM**

- **Open-source**: The quality can vary widely depending on the community and contributors. While some open-source models perform decently, they may not achieve state-of-the-art performance in certain tasks compared to closed-source options.
- **Closed-source**: Proprietary models like OpenAI's GPT are often fine-tuned and optimized using cutting-edge resources, ensuring consistently high-quality output.

### 2. **Test/Alignment Quality**

- **Open-source**: Alignment with ethical guidelines and robustness in handling complex queries can be inconsistent. This depends heavily on community support and individual project standards.
- **Closed-source**: Typically undergoes rigorous testing and fine-tuning to align the model with ethical, safety, and performance standards.

### 3. **Ownership**

- **Open-source**: Users often have full access to the model's code and architecture, allowing customization and control over the deployment.
- **Closed-source**: Users do not own the model or its underlying code. This is especially true for the latest models from proprietary vendors.

### 4. **License Cost**

- **Open-source**: Many open-source models are free to use, provided they meet the user's requirements. However, some may have licenses that restrict certain types of use.
- **Closed-source**: Often comes with significant licensing costs, particularly for commercial usage.

### 5. **Operation Cost**

- **Open-source**: Running an open-source model often requires significant computational resources, leading to higher operational costs.
- **Closed-source**: Cloud-based closed-source services may offload operational costs to providers, potentially lowering overall expenses for the user.

### 6. **Security**

- **Open-source**: With proper implementation, open-source models can provide high security, especially in self-hosted environments.
- **Closed-source**: Security depends on the vendor's implementation and trustworthiness, but the user has limited control over the backend.

---

### Key Takeaways

- **Flexibility**: Open-source models are ideal for users who want customization, ownership, and reduced upfront costs but require technical expertise.
- **Convenience**: Closed-source models offer superior performance and ease of use, albeit at higher licensing and dependency costs.

# Open-source LLM Licensing

- **Permissive Licenses**:

  - Examples: **Apache 2.0**.
  - These licenses allow you to use, modify, and distribute the model with minimal restrictions. They are ideal for building commercial and non-commercial applications because they offer flexibility and freedom.

- **Restricted Licenses**:

  - Examples: **Creative Commons Attribution-ShareAlike (CC BY-SA) 3.0**.
  - These licenses impose some restrictions, such as requiring derivatives to maintain the same license. While they don't explicitly prohibit commercial use, the added conditions may impact usability for business purposes.

- **Non-commercial Licenses**:
  - Examples: **Facebook's proprietary licenses**, **Creative Commons Attribution-NonCommercial-ShareAlike (CC BY-NC-SA) 4.0**.
  - These explicitly forbid commercial use. They are unsuitable for building commercial applications, making them a poor choice for businesses or app developers seeking monetization opportunities.

---

## Additional Information:

### Understanding Licensing Impact:

1. **Permissive Licenses** are best for developers who want maximum flexibility and the ability to monetize their applications without legal concerns.
2. **Restricted Licenses** are suitable for collaborative or community-focused projects where sharing improvements under the same terms is prioritized.
3. **Non-commercial Licenses** are tailored for academic, research, or personal projects where commercial use isn't a factor.

### Choosing the Right License:

- Assess your use case: Is it commercial or non-commercial?
- Consider downstream requirements: Will you need to distribute the model or derivatives?
- Evaluate compliance: Can you adhere to the license terms without hindering your goals?

---

# LLM Open-source License Models

| **License**     | **LLMs**                     | **Permissive or Copyleft** | **Commercial Use**     | **Redistribution**     | **Modification** |
| --------------- | ---------------------------- | -------------------------- | ---------------------- | ---------------------- | ---------------- |
| **Apache 2.0**  | BERT, XLNet, and XLM-RoBERTa | Permissive                 | Yes (with attribution) | Yes                    | Yes              |
| **MIT**         | GPT-2, T5, and BLOOM         | Permissive                 | Yes (with attribution) | Yes                    | Yes              |
| **GPL-3.0**     | GLM-130B and NeMo LLM        | Copyleft                   | Yes (with source code) | Yes (with source code) | Yes              |
| **Proprietary** | GPT-3, LaMDA, and Cohere     | Varies                     | Varies                 | Varies                 | Varies           |

---

## Additional Information

### **Apache 2.0**

- **Type**: Permissive.
- **Usage**: Widely used in open-source projects, Apache 2.0 allows almost unrestricted use of the code, provided proper attribution is given.
- **Commercial Use**: Permitted with attribution.
- **Redistribution and Modification**: Fully allowed.

### **MIT License**

- **Type**: Permissive.
- **Usage**: One of the simplest and most permissive licenses, allowing extensive flexibility in usage and modification.
- **Commercial Use**: Permitted, requiring only attribution.
- **Redistribution and Modification**: Fully allowed.

### **GPL-3.0**

- **Type**: Copyleft.
- **Usage**: Ensures that any derivative works are also open-source and licensed under GPL-3.0. This fosters open collaboration but can limit commercial exploitation without disclosure.
- **Commercial Use**: Allowed but requires derivative works to share their source code under GPL.
- **Redistribution and Modification**: Allowed with the condition that the same license terms are applied.

### **Proprietary Licenses**

- **Type**: Varies by provider.
- **Usage**: Licenses for proprietary LLMs like GPT-3, LaMDA, and Cohere are often restrictive. Terms may vary widely and often limit commercial use, redistribution, or modification.
- **Commercial Use**: Subject to license terms, which may include significant costs.
- **Redistribution and Modification**: Usually restricted or prohibited.

---

### Key Considerations for Selecting a License:

1. **Permissive Licenses**:

   - Ideal for projects that prioritize flexibility and commercialization.
   - Minimal restrictions make these licenses business-friendly.

2. **Copyleft Licenses**:

   - Encourage open-source collaboration but require public sharing of derivative works.
   - Suitable for non-commercial or collaborative projects.

3. **Proprietary Licenses**:
   - Best for organizations that require state-of-the-art models but are willing to adhere to vendor-imposed restrictions.
   - Costs and limitations may vary significantly.

---
