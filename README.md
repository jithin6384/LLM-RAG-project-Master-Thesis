# Thesis
Retrieval Augmented Generation (RAG) Thesis Project

This repository contains the implementation of my master’s thesis on Retrieval Augmented Generation (RAG). The project explores how different chunking and embedding strategies impact the accuracy, efficiency, and environmental footprint of LLM responses.

Project Overview

Large language models (LLMs) are limited by their context window and rely on static training data, which can lead to hallucinations—confident but incorrect answers. RAG mitigates this by retrieving relevant information from external knowledge sources to enrich the model’s context in real time.

Dataset

Used the CRACK database, a question-answer dataset, to test retrieval accuracy.

Long HTML documents were parsed and processed for chunking and embedding.

Methodology

Chunking Strategies

Sliding window

Paragraph-based

Semantic clustering

Sentence-based

[Other strategies]

Embeddings

MiniLM

10-LargePar (10-Lapar)

In-Float

Combinations of chunking + embedding were tested to evaluate retrieval quality.

Vector Database

FAISS used to store and retrieve embeddings efficiently.

Evaluation Metrics

Accuracy of retrieval vs. expected answers

Computational cost

Carbon emissions of different model combinations

Key Insights

Different combinations of chunking and embeddings significantly affect both accuracy and environmental impact.

Analysis:
This thesis focused on designing and evaluating a Retrieval-Augmented Generation pipeline to study the impact of different chunking and embedding strategies on answer quality and efficiency.
I built an end-to-end RAG pipeline on the CRAG QA dataset using LLaMA and OpenAI models, with three Hugging Face sentence transformer models and five chunking strategies. Embeddings were stored in FAISS, with cosine similarity used to retrieve candidate chunks, followed by reranking using OpenAI relevance scoring.
Answer generation was performed using LLaMA, while OpenAI models were used to evaluate accuracy against ground truth. The best configuration achieved an F1 score of 0.82 while reducing estimated CO₂ emissions by 30 percent compared to the baseline dense retrieval approach.
Technologies: LLaMA | OpenAI | GPT-3.5 | GPT-4 | FAISS | Sentence Transformers (MiniLM, IntFloat, GTE-Large)

Evaluating carbon emission and computation cost alongside retrieval quality is critical for responsible AI.
