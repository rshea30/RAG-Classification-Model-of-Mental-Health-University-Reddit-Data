# RAG-Classification-Model-of-Mental-Health-University-Reddit-Data
A RAG-based (Retrieval-Augmented Generation) suicide ideation detection system that analyzes Reddit posts from university subreddits to identify potentially concerning mental health content.

Overview
This project uses machine learning and natural language processing to classify social media posts for signs of suicidal ideation. It's trained on a labeled Twitter dataset and applied to Reddit posts from various university communities.
Features

RAG-based Classification: Uses retrieval-augmented generation with example-based learning
Keyword Filtering: Pre-filters posts using mental health-related keywords before classification
Multi-school Analysis: Processes multiple university subreddit datasets individually
Progress Tracking: Saves individual school results and combines them into a final dataset

Tech Stack
LangChain: Framework for building the RAG pipeline
OpenAI GPT-3.5: Language model for classification
HuggingFace Embeddings: For semantic similarity search
Chroma: Vector database for storing training examples
Pandas: Data processing and manipulation

How It Works
Training: Loads a labeled Twitter suicide ideation dataset and creates a vector store of examples
Filtering: Scans Reddit posts for mental health-related keywords (depression, anxiety, suicide, etc.)
Classification: For each filtered post, retrieves similar examples and uses GPT-3.5 to classify as "SUICIDE" or "NOT_SUICIDE"
Output: selftext of all posts the fit the keys and the classification of "SUICIDE" or "NOT_SUICIDE"
