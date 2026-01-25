# 🛍️ Style Finder: Multimodal RAG Application

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![PyTorch](https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white)
![Gradio](https://img.shields.io/badge/Gradio-orange?style=for-the-badge&logo=gradio&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

Welcome to **Style Finder**, an advanced AI-powered fashion assistant. This project demonstrates the power of **Multimodal Retrieval Augmented Generation (MM-RAG)**, allowing users to upload images of outfits and receive detailed metadata, material descriptions, and purchase links.

---

## 🚀 Overview
**MM-RAG** (Multimodal Retrieval Augmented Generation) is a cutting-edge approach that combines the strengths of multimodal understanding—processing multiple data types like images and text—with retrieval-augmented generation. While standard AI models are limited to their training data, this application bridges the gap by retrieving relevant information from a specific fashion database to enhance accuracy and detail.

---

## 🛠️ Key Features
* 🌈 **Multimodal Input**: Accepts both images and text queries to provide a comprehensive user experience.
* 🔍 **Intelligent Retrieval**: Uses a pre-trained **ResNet50** model to convert images into feature representations for visual similarity matching.
* 📊 **Contextual Augmentation**: Merges retrieved structured data (prices, URLs, descriptions) with the original query to provide the LLM with "proprietary knowledge".
* 🤖 **Advanced Generation**: Leverages the **Llama Vision** model to produce structured, professional catalog-style analysis grounded in retrieved data.

---

## 🏗️ The MM-RAG Architecture
The application follows a professional four-step pipeline:

1.  **🔵 Data Indexing**: Diverse data types are converted into embeddings and indexed in a vector database for efficient searching.
2.  **🟢 Data Retrieval**: The system performs a semantic search using cosine similarity to find the closest visual and textual matches.
3.  **🟡 Augmentation**: The retrieved multimodal data is combined with the original user query to enrich the context.
4.  **🔴 Response Generation**: An augmented query is sent to a multimodal generative model to produce a response blending all information sources.

---

## 📂 Project Structure
```text
style-finder/
├── app.py                # Main application logic & Gradio UI
├── models/
│   ├── image_processor.py # Image encoding using ResNet50
│   └── llm_service.py     # Llama Vision model integration
├── utils/
│   └── helpers.py         # Data formatting & Base64 utilities
└── swift-style-embeddings.pkl # Pre-computed vector embeddings
