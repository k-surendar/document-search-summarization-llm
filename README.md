# Document Search and Summarization System

## Project Overview

This project implements an intelligent document search and summarization system that helps users find relevant information from a collection of documents and generate concise, context-grounded summaries using a Large Language Model (LLM).

The system combines keyword-based search and semantic similarity to retrieve relevant document chunks and uses Google's Gemini API to generate summaries in different lengths.

## Key Features

- Document cleaning and duplicate removal
- Text preprocessing and chunking with overlapping segments
- Keyword-based retrieval using TF-IDF
- Semantic search using sentence embeddings
- Hybrid search combining keyword and semantic relevance
- LLM-powered document summarization
- Short, medium, and detailed summary options
- Search and summary evaluation reports

## Technologies Used

- Python
- Pandas
- Scikit-learn
- Sentence Transformers
- TF-IDF
- Google Gemini API (`gemini-2.5-flash`)
- ROUGE evaluation metrics
- Google Colab

## Dataset

The project uses the **20 Newsgroups dataset**, a collection of text documents organized into different discussion categories.

## System Workflow

1. **Data collection:** Load the document dataset.
2. **Data cleaning:** Clean text, normalize content, and remove duplicate documents.
3. **Text chunking:** Split documents into chunks of approximately 150 words with a 30-word overlap.
4. **Keyword search:** Use TF-IDF with unigrams and bigrams to identify keyword-relevant chunks.
5. **Semantic search:** Generate embeddings using `all-MiniLM-L6-v2` to identify semantically relevant content.
6. **Hybrid retrieval:** Combine semantic and keyword scores using a weighted scoring approach.
7. **Summarization:** Send retrieved context to Gemini to generate grounded summaries.
8. **Evaluation:** Evaluate retrieval and summarization using the generated reports and ROUGE metrics.

## Hybrid Search Approach

The system combines two retrieval methods:

- Semantic similarity score: 60%
- Keyword relevance score: 40%

The combined score helps retrieve documents that match both the meaning of the query and its keywords.

## Summarization Evaluation

The project produced the following ROUGE results for its evaluated summaries:

| Metric | F1 Score |
|---|---:|
| ROUGE-1 | 0.4063 |
| ROUGE-L | 0.2864 |

These scores were obtained using source document chunks as the comparison baseline, not independently written human reference summaries. They should therefore be interpreted as preliminary evaluation results rather than definitive measures of summary quality.

## Generated Project Files

The project generates the following files:

- `cleaned_documents.csv` — cleaned document dataset
- `document_chunks.csv` — chunked document text
- `search_evaluation.csv` — search evaluation results
- `summary_evaluation.csv` — summary evaluation results
- `rouge_report.txt` — ROUGE evaluation report
- `project_report.md` — project report
- `README.md` — project documentation

## How to Run

1. Open the notebook in Google Colab.
2. Install the required Python packages.
3. Load and preprocess the dataset.
4. Configure your Gemini API key securely.
5. Run the notebook cells in order.
6. Enter a search query to retrieve relevant document chunks.
7. Generate a summary using the retrieved context.
8. Review the evaluation reports.

**Note:** A valid Gemini API key is required for the LLM summarization component. Do not upload API keys or other secrets to GitHub.

## Learning Outcomes

- Text preprocessing and data cleaning
- Document chunking and overlapping text segmentation
- Keyword-based information retrieval
- Semantic search using sentence embeddings
- Hybrid search system design
- Retrieval-augmented generation concepts
- LLM-based summarization
- Evaluation using ROUGE metrics

## Future Improvements

- Evaluate summaries against human-written reference summaries.
- Improve retrieval ranking and relevance.
- Add a web-based interface for easier interaction.
- Support uploading custom documents.
- Explore vector databases for scalable document retrieval.

## Author

K. Surendar
