# Intelligent (SHL) Assessment Recommendation System

This project is an AI-powered recommendation system built to suggest the most relevant SHL assessments based on user queries, job descriptions, or unstructured input data. It combines NLP techniques and Large Language Models (LLMs) to provide accurate, efficient, and context-aware results through an intuitive frontend interface.

Try it out @ https://shlassessmentrecommendationsystem.streamlit.app [Example Test Cases given below]


  
Project Overview

Developed an AI-powered recommendation engine that suggests relevant SHL assessments based on job descriptions, unstructured text, URLs, or custom user queries. The system combines semantic NLP techniques with LLM-based contextual understanding to deliver accurate, ranked assessment recommendations through an interactive Streamlit interface.

Key Features

Recommends SHL-like assessments using:

Job descriptions

Unstructured text or URLs

Custom user queries

Semantic similarity matching using Sentence-BERT embeddings

Ranking and scoring using cosine similarity

Contextual feature extraction using Gemini 1.5 Pro (LLM)

Constraint-based filtering (skills, duration, relevance)

Displays top-N assessment recommendations

Interactive Streamlit web application

Tech Stack

Natural Language Processing

Sentence-BERT for generating embeddings

Cosine similarity for ranking relevant assessments

LLM Integration

Gemini 1.5 Pro for extracting structured information (job role, skills, duration) from unstructured inputs

Post-retrieval refinement and relevance filtering using LLM outputs

Frontend

Streamlit for interactive user input and result visualization

How It Works
1. Data Preparation

Uses a mock dataset of 50 SHL-style assessments containing:

Assessment name, URL, duration, test type, skills, description

Remote proctoring and adaptive/IRT support

A combined text column is created by concatenating all relevant fields to generate embeddings.

2. NLP Embedding & Retrieval

Dataset entries and user queries are converted into vector embeddings using Sentence-BERT.

Cosine similarity is computed to retrieve the top matching assessments.

3. LLM-Based Enhancement

Gemini 1.5 Pro processes job descriptions, URLs, or free-text input.

Extracts structured features such as:

Job role

Required skills

Expected assessment duration

Retrieved results are refined based on extracted constraints and relevance.

4. Evaluation

Model performance evaluated using:

Recall@5

MAP@5

Hybrid NLP + LLM approach outperforms the NLP-only baseline.

5. User Interface

Streamlit app allows users to:

Enter queries

View ranked assessment recommendations

Explore assessment details interactively

Performance Metrics

NLP Model: Recall@5 = 0.85, MAP@5 = 0.71

NLP + LLM Model: Recall@5 = 1.0, MAP@5 = 1.0
