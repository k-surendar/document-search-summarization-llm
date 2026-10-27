# Document Search and Summarization Using LLMs

## Project Overview
An intelligent document search and summarization system that retrieves
relevant passages from a text dataset and generates summaries using a
Large Language Model (LLM).

## Technologies Used
- Python
- Pandas and NumPy
- Scikit-learn
- TF-IDF and cosine similarity
- Sentence Transformers
- Gemini 2.5 Flash API
- Google Colab
- IPyWidgets

## Dataset
The project uses the 20 Newsgroups dataset from scikit-learn.

## Key Features
- Text cleaning and preprocessing
- Document chunking with overlapping text
- Keyword-based retrieval using TF-IDF
- Semantic retrieval using sentence embeddings
- Hybrid search combining keyword and semantic scores
- LLM-powered summarization
- Adjustable summary length and retrieval count
- Search and summarization evaluation

## Evaluation Results
- ROUGE-1 F1: 0.4063
- ROUGE-L F1: 0.2864

These are initial baseline results. ROUGE measures text overlap and
does not independently establish factual accuracy.

## How It Works
1. Load and preprocess the documents.
2. Split documents into overlapping chunks.
3. Retrieve relevant chunks using hybrid search.
4. Send retrieved context to the Gemini model.
5. Display the generated summary and source passages.
6. Evaluate retrieval and summarization performance.

## Important
A valid Gemini API key is required to generate summaries.
Do not publish your API key in the notebook or repository.

## Future Improvements
- Evaluate with real user queries and labelled relevant documents.
- Add document uploads and persistent vector storage.
- Improve source attribution and factual-grounding checks.