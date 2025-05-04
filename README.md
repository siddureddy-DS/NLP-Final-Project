This project implements an Emotion-Aware Retrieval-Augmented Generation (RAG) system designed to generate empathetic, emotionally-aligned responses for users experiencing mental health challenges. The system combines emotion detection, semantic retrieval of support content, and large language model (LLM)-based response generation to produce safe and supportive replies.

We developed an Emotion-Aware RAG system that detects user emotions, retrieves emotionally relevant mental health posts, and generates empathetic replies using lightweight language models like Phi-3 Mini.

By combining retrieval with generation, we ensure safer, contextually grounded responses.

The system was evaluated for emotion detection, retrieval precision, and response quality, achieving strong performance across all metrics.

This project shows how AI can be responsibly applied to support mental health.


### 1. Emotion Detection
- Model: `roberta-base-go_emotions`
- Output: One of 28 emotion classes (e.g., sadness, fear, optimism)
- Purpose: Tags input query with dominant emotion for use in retrieval and generation

### 2. Semantic Retrieval
- Model: `all-MiniLM-L6-v2`
- Tool: FAISS index for fast similarity search
- Output: Top-k similar Reddit posts emotionally aligned with user query

### 3. Response Generation
- Models:
  - `Phi-3 Mini` (lightweight, empathy-first)
  - `Falcon-7 B-Instruct` (fluent, but higher hallucination risk)
- Prompts are generated using the input query, retrieved posts, and emotion tag

### 4. Evaluation
- Emotion Detection: Accuracy, F1 Score
- Retrieval: Precision@k
- Generation: BLEU, ROUGE-1, ROUGE-2, ROUGE-L
- Qualitative: Human reviews for empathy, hallucination, fluency


You can run code via Google Colab using the T4 GPU Runtype: https://colab.research.google.com/drive/16MgWIaGyeOPNtsZal3XzTrrtcXbK8fqT?usp=sharing

You can watch the Code Demo Presentation : https://youtu.be/oZjSxAQhovY 
