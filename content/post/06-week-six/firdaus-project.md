---
title: "Week 6: Exploring RAG"
description: Retrieval Augmented Generation
slug: week-six-project1
date: 2025-10-18T10:02:15.191Z
lastMod: 2025-10-18T10:02:10.773Z
authors:
    - Firdaus
image: week-six-cover2.jpg
categories:
    - projects
tags: 
    - week6
---

# RAG Testing With Raspberry Pi 4

I was curious on how to implement RAG into edge devices so I borrowed the Raspberry Pi 4 provided by IC2 and work my way through at the dorm. 

![Raspberry Pi 4](rp4.jpeg) 

# Choosing The Right Embedding Models
In my RAG system for Thailand climate awareness, I chose the **sentence-transformers/multi-qa-MiniLM-L6-cos-v1** embedding model for document retrieval. This model is specifically designed for question-answering tasks and performs well with multi-domain queries, making it ideal for my use case where users ask various questions about Thailand's climate data. I implemented the embedding functionality using HuggingFace Embeddings through LangChain, which allowed me to easily integrate the model with my FAISS vector store. The model efficiently converts both my document chunks and user queries into dense vector representations, enabling semantic search across my collection of PDFs, text files, and JSON documents containing Thailand climate information. I configured my system with a chunk size of 128 tokens and 20-token overlap to ensure optimal retrieval performance while maintaining context coherence.

![Config file](config.jpg) ![Installing Libraries and Dependencies](img/embeddingmodels.jpg)

# Quick Evaluation
For evaluating my RAG system's performance, I implemented a comprehensive evaluation framework using the RAGAS library, which provides specialized metrics for retrieval-augmented generation systems. I created a custom RagEvaluator class that measures four key metrics: context recall, faithfulness, context precision, and answer relevancy. My evaluation dataset includes carefully crafted questions about Thailand's climate data with corresponding ground truth answers, covering topics like disaster prevention responsibilities, seasonal patterns, regional climate issues, and national adaptation plans. Additionally, I built a performance benchmarking system that measures inference speed, tokens per second, memory usage, and CPU utilization during RAG operations. This dual approach allows me to assess both the quality of my system's responses through RAGAS metrics and its operational efficiency through performance benchmarks, ensuring my Thailand climate chatbot delivers accurate information quickly and reliably.

![RAGAS Evaluation](quick-evaluation.jpg)





