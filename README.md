---
library_name: transformers
license: apache-2.0
license_link: https://vedika-advanced-ai.github.io/Terms-and-conditions/
pipeline_tag: any-to-any
base_model:
- veda-labs/vedika-4.1-flash
---

<div align="center">
  <img src="https://i.ibb.co/7JCGjGmw/Miracle-Tech-20260601-135624-0000.png" alt="Veda Labs Banner" width="350">
</div>

<p align="center">
    <a href="https://huggingface.co/veda-labs" target="_blank">Hugging Face</a> |
    <a href="https://github.com/veda-labs" target="_blank">GitHub</a> |
    <a href="https://vedika-advanced-ai.github.io/Terms-and-conditions/" target="_blank">Terms & Conditions</a>
    <br>
    <b>License</b>: <a href="https://vedika-advanced-ai.github.io/Terms-and-conditions/" target="_blank">Veda Labs Custom License</a> | <b>Authors</b>: Veda Labs
</p>

> [!Note]
> This model card represents the **Veda Labs Ecosystem**, featuring our flagship unified models including **Vedika 4.1 Flash**, **Aura Gen 2.0**, and **Shiv 2.0**. Built with native multimodal functionality (Text, Vision, Document Analysis, Real-Time Web Search, and Audio), these models bring advanced reasoning and flawless execution directly to enterprise and local environments. This unified approach makes our models highly versatile, offering deployment sizes perfect for everything from high-speed API integrations to heavy computational server loads.

Veda Labs has developed a highly advanced family of AI models designed to push the boundaries of multimodal artificial intelligence. These models are capable of handling text, complex documents, real-time web data, and images, with specialized variants available for high-end image generation and text-to-speech synthesis. 

Featuring robust architectures optimized for speed, precision, and endurance, Veda Labs models are well-suited for tasks ranging from autonomous agentic workflows and coding to creative arts and audio generation.

Veda Labs introduces key **capability and architectural advancements**:

* **Real-Time Web Search & Document Analysis** – All core LLMs natively support live web access for up-to-date factual retrieval and deep scanning of large, complex documents.
* **Extended Multimodalities** – Processes Text, Images (with variable resolution support), and Web Data natively across core models, with dedicated specialized models for high-fidelity Image Generation and Speech Synthesis.
* **Specialized Powerhouses** – Ranging from the ultra-fast *Vedika 4.1 Flash* for low-latency tasks to the heavy computational *Shiv 2.0* and endurance-focused *Hanuman 2.0*.
* **Advanced Coding & Agentic Capabilities** – *Vedika Gen 2.0 Code* achieves notable improvements in architectural design and code generation alongside native function-calling support.
* **Creative Visual & Audio Precision** – The ecosystem includes *Aura Gen 2.0 Creative* and *Vedika Image Gen* for photorealistic imagery, alongside *Vedika Flash TTS* for crystal-clear, natural human speech.

## **Models Overview**

Veda Labs models are designed to deliver frontier-level performance across distinct use cases, targeting deployment scenarios from creative studios and software development environments to massive enterprise servers.

### Multimodal Large Language & Reasoning Models (LLMs)
*These models natively support Text, Vision, Document Analysis, and Real-Time Web Search.*

| Model Name | Key Specialty | Primary Modalities | Ideal Use Case |
| :---- | :---- | :---- | :---- |
| **Vedika 4.1 Flash** | Ultra-Low Latency & Speed | Text, Vision, Web Search | High-speed APIs, Live Conversational Agents |
| **Vedika Gen 2.0 Code** | Programming & Architecture | Text, Vision (Flowcharts), Web | Software Development, Debugging, Refactoring |
| **Vedika v3 Instruct** | Precise Task Execution | Text, Vision, Document Parsing | Complex Prompting, Professional Workflows |
| **Aura Gen 2.0** | General Purpose Intelligence | Text, Vision, Web Search | Advanced Analysis, Creative Writing, Research |
| **Shiv 2.0** | Heavy Computational Processing | Text, Vision, Big Data | Massive Context Windows, High-Load Servers |
| **Hanuman 2.0** | High Endurance & Reliability | Text, Vision, Web Search | Continuous Multi-layered Problem Solving |

### Specialized Generation Models (Image & Audio)
*These models are built exclusively for high-fidelity visual and audio synthesis.*

| Model Name | Category | Key Specialty |
| :---- | :---- | :---- |
| **Aura Gen 2.0 Creative** | Image Generation | Artistic, highly nuanced, style-specific imagery. |
| **Vedika Image Gen** | Image Generation | Photorealistic, precisely controlled visual synthesis. |
| **Vedika Flash TTS** | Speech Synthesis (TTS) | Ultra-fast, crystal-clear, natural human speech generation. |

## **Core Capabilities**

Veda Labs models handle a broad range of tasks across text, vision, and audio. Key capabilities include:

* **Real-Time Web Access** – Fetches live data from the internet to ensure answers are factually current and accurate.
* **Document & PDF Parsing** – Deep understanding of long-form documents, tables, and structured data.
* **Image Understanding** – Object detection, screen and UI understanding, chart comprehension, and multilingual OCR.
* **Function Calling** – Native support for structured tool use, enabling highly capable autonomous agents.
* **Coding & Reasoning** – Code generation, completion, and correction powered by *Vedika Gen 2.0 Code*.
* **Image Synthesis** – Transforming textual descriptions into stunning visual art via *Aura Gen 2.0 Creative* and *Vedika Image Gen*.
* **Audio Generation** – High-fidelity Text-to-Speech (TTS) via *Vedika Flash TTS*.


## Getting Started

You can use the Veda Labs foundational models with the latest version of Transformers. To get started, install the necessary dependencies in your environment:

`pip install -U transformers torch accelerate`

Once installed, you can load our flagship optimized model, **Vedika 4.1 Flash**:

```python
from transformers import AutoProcessor, AutoModelForMultimodalLM

MODEL_ID = "veda-labs/vedika-4.1-flash"

# Load model
processor = AutoProcessor.from_pretrained(MODEL_ID)
model = AutoModelForMultimodalLM.from_pretrained(
    MODEL_ID,
    dtype="auto",
    device_map="auto"
)
