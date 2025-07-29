# Build_a_Semantic_Book_Recommender_with_LLMs
1. Text Data Cleaning (data-exploration.ipynb)
Outcome:
Cleaned and preprocessed a book dataset (from Kaggle) to remove missing/invalid descriptions, standardize categories, and prepare text for NLP tasks.

Key steps:

Handling missing values (e.g., descriptions, categories).

Filtering out short/uninformative descriptions.

Creating composite fields (e.g., combining title and subtitle).

Tagging descriptions with unique identifiers (ISBN) for later retrieval.

Expectation:
A structured dataset (books_cleaned.csv) ready for semantic search and NLP tasks.

Insights into data quality (e.g., distribution of categories, missing values).

2. Semantic (Vector) Search (vector-search.ipynb)
Outcome:
Built a vector database using LangChain and OpenAI embeddings to enable semantic search.

Implemented a function to retrieve book recommendations based on natural language queries (e.g., "a book about revenge").

Used ChromaDB (a vector database) to store and query embeddings efficiently.

Expectation:
Users can input a query (e.g., "a heartwarming story about friendship") and get a list of semantically similar books.

Recommendations are based on the meaning of the query, not just keyword matching.

3. Text Classification (text-classification.ipynb)
Outcome:
Used zero-shot classification with Hugging Face's BART model to classify books into categories:

Fiction / Non-fiction

Children's fiction / Children's non-fiction

Validated model accuracy (~78%) on labeled data.

Applied predictions to books with missing categories.

Expectation:
Users can filter recommendations by genre (e.g., "Show only fiction books").

Improved organization of book categories for better recommendations.

4. Sentiment Analysis (sentiment-analysis.ipynb)
Outcome:
Used a fine-tuned RoBERTa model (from Hugging Face) to extract emotions from book descriptions:

Anger, Disgust, Fear, Joy, Sadness, Surprise, Neutral.

Calculated the maximum emotion score per book (e.g., "This book is 85% Joyful").

Added emotion scores to the dataset for sorting/filtering.

Expectation:
Users can sort books by emotional tone (e.g., "Show me suspenseful books" or "Sort by happiest").

Adds a personalized touch to recommendations (e.g., "I want a sad historical novel").

5. Web Application (gradio-dashboard.py)
Outcome:
Built an interactive Gradio dashboard where users can:

Enter a natural language query (e.g., "a mystery novel set in Paris").

Filter by category (fiction/non-fiction) or emotion (happy/sad/suspenseful).

View recommendations as a gallery of book covers with titles/authors.

Integrated all previous components (vector search, classification, sentiment analysis).

Expectation:
A user-friendly interface for book recommendations.

Combines semantic search + filtering + sorting for a powerful recommendation system.
#Output Dashboard
<img width="1916" height="907" alt="image" src="https://github.com/user-attachments/assets/06bb539c-b5dd-4dc1-8780-a529f57cb3d4" />
<img width="1912" height="984" alt="image" src="https://github.com/user-attachments/assets/c5c1f4fe-f254-4987-9311-639e96de4395" />
<img width="1919" height="1032" alt="image" src="https://github.com/user-attachments/assets/3940ad38-b545-4e41-a82b-665cf6519149" />
<img width="1919" height="1025" alt="image" src="https://github.com/user-attachments/assets/e7be57b1-8083-4007-a94b-6239eae81bbf" />
Enables to download.
<img width="1919" height="1023" alt="image" src="https://github.com/user-attachments/assets/3a1e6157-65d8-48a0-b122-e20c61a16f08" />




