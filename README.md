# 📄 Multilingual RAG-Based Question Answering (Hindi–Tamil)

## 🔍 Project Overview
This project implements a multilingual Question Answering (QA) system for Hindi and Tamil using the XLM-RoBERTa-base transformer model.
The system is trained on Kaggle competition data consisting of context, question, and answer triples, where the answer is always a text span extracted from the given context.

To support real-world document-based QA, the project integrates a Retrieval-Augmented Generation (RAG) pipeline that enables users to upload PDF documents, ask questions, and receive answers grounded strictly in the document content, with clear visualization of the source text.

## **🎯 Problem Statement**

Given:

A context (paragraph or document),

A question,

An answer span located inside the context,

the model learns to extract the correct answer from the context.

To extend this to long documents (e.g., PDFs), RAG is applied to retrieve the most relevant text segments before performing extractive question answering.

## **🧠 Key Features**

- Multilingual QA (Hindi & Tamil)

- Extractive Question Answering

- XLM-RoBERTa-base backbone

- Retrieval-Augmented Generation (RAG)

- PDF upload and processing

- Relevant context retrieval

- Answer span visualization

- Kaggle competition–ready pipeline

## **🏗️ System Architecture**

PDF Upload

User uploads a PDF document

Text Extraction & Chunking

Extract text and split into overlapping chunks

Retrieval (RAG)

Retrieve the most relevant chunks based on the question

Extractive QA

Apply XLM-RoBERTa-base to extract the answer span

Answer Visualization

Highlight the exact text used to answer the question

## **📊 Dataset**

Source: Kaggle Competition Dataset

Languages: Hindi, Tamil

Format:

context

question

answer (text span inside context)

Task Type: Extractive Question Answering

Data Modality: Text only

## **🤖 Model Details**

Base Model: xlm-roberta-base

Framework: Hugging Face Transformers

Task: Question Answering

Answer Type: Extractive (no text generation)

The model predicts start and end positions of the answer within the retrieved context.

## **🚀 Why RAG?**

Although the model is extractive, RAG is used to:

Handle long PDF documents

Reduce irrelevant context

Improve answer accuracy

Enable scalable document-based QA

RAG retrieves the most relevant context before applying extractive QA.

## **🧪 Evaluation**

Evaluated using Kaggle competition metrics

Focus on:

Answer accuracy

Context relevance

Multilingual performance

## **📂 Repository Structure**

├── data/                 # Kaggle dataset and processed files
├── notebooks/            # Training and experiments
├── models/               # Fine-tuned XLM-RoBERTa checkpoints
├── inference/             # RAG + PDF QA pipeline
├── README.md             # Documentation
└── requirements.txt      # Dependencies

## **🏷️ Keywords**

nlp
question-answering
rag
xlm-roberta
multilingual
hindi
tamil
huggingface
kaggle
pdf-qa

## **📌 Notes**

Answers are always grounded in the source document

Designed for low-resource multilingual QA

Suitable for academic evaluation and real-world usage
