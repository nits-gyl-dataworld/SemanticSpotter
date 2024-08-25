# Fashion Product Chatbot

This project implements a fashion product chatbot using LlamaIndex. The chatbot provides detailed responses about fashion products by leveraging vector-based indexing and Retrieval-Augmented Generation (RAG).

## Problem Statement

The goal is to develop a chatbot capable of providing detailed responses about fashion products from a Myntra dataset. This chatbot must effectively understand user queries, retrieve relevant product information, and generate comprehensive explanations. The solution involves:

- Preprocessing the dataset
- Creating a vector-based index for efficient querying
- Implementing Retrieval-Augmented Generation (RAG) using LlamaIndex
- Managing conversational context and memory across interactions

## Why LlamaIndex

LlamaIndex is an ideal framework for this project because it provides robust tools for creating vector-based search indices and implementing Retrieval-Augmented Generation. It supports efficient querying and retrieval of documents, crucial for generating detailed and contextually relevant responses by combining retrieval with generated content.

## Project Goals

1. **Preprocess and Clean Dataset:** Prepare the fashion product dataset by filling missing values and cleaning text fields.
2. **Build Vector-Based Index:** Create a vector store index using LlamaIndex for efficient querying and retrieval of product information.
3. **Implement RAG:** Build Retrieval-Augmented Generation using LlamaIndex to provide detailed, context-aware responses by combining retrieval with generated content.
4. **Develop Conversational Interface:** Build a chatbot interface that manages conversational history and provides relevant responses based on user input.
5. **Feedback Mechanism:** Implement a feedback system to evaluate the quality of responses and improve the chatbot’s performance over time.

## Data Sources

- **Myntra Fashion Dataset:** The primary data source is a CSV file containing fashion product information such as descriptions, attributes, ratings, etc.

## System Design

### 1. Data Preprocessing
- Clean and prepare the raw data to ensure it is suitable for further processing and analysis.
- Remove null values, handle missing data, normalize text, and perform other data cleaning steps.

### 2. Loading and Creating Data/Documents
- Load the pre-processed data and organize it into a format that can be indexed.
- Load the dataset and create documents for indexing.

### 3. Indexing the Documents Using LlamaIndex
- Create an index of the documents for efficient querying.
- Parse the documents into nodes and create an index.

### 4. Build Query Engine
- Construct a query engine to handle and process user queries.
- Set up the query engine based on the indexed data.

### 5. Initialize Conversation
- Set up the initial state for the chatbot conversation.
- Initialize variables to store conversation history and other relevant data.

### 6. Query Response
- Process user inputs and generate responses based on the indexed data, pass this data in API calls, and generate relevant responses.
- Handle user queries, generate detailed responses, and update conversation history.

### 7. Feedback
- Collect feedback from users about the responses provided by the chatbot to improve future interactions.
- Ask users for feedback and store their responses.

### 8. End Conversation
- Conclude the interaction with the user.
- Provide final outputs, save conversation logs, and exit the interaction.

## Design Choices

1. **Data Preprocessing:** Text fields are cleaned to remove HTML tags, punctuation, and extra spaces for better indexing and retrieval.
2. **Indexing:** LlamaIndex is used to create a vector-based index of the documents to facilitate efficient querying.
3. **Query Engine:** The Query Engine enhances response quality by combining retrieved data with generated explanations.
4. **Conversational Memory:** The chatbot maintains a conversation history to provide contextually relevant responses.

## Challenges Faced

1. **Data Quality:** Handling missing values and cleaning text data to ensure high-quality input for indexing.
2. **Context Management:** Ensuring that the chatbot maintains conversational context over multiple interactions.
3. **RAG by LlamaIndex:** Effectively crafting retrieval and generation in LlamaIndex to produce detailed and relevant responses.
4. **User Feedback:** Collecting and analyzing feedback to continuously improve the chatbot’s performance.

## Installation

1. Install dependencies:
    ```sh
    pip install llama-index openai pandas
    ```

## Usage

1. Mount Google Drive and Set API Key:
    - Ensure Google Drive is mounted and the OpenAI API key is set.
2. Run the Chatbot:
    ```python
    Dialogue_Management()
    ```
3. Interaction:
    - Type queries related to fashion products.
    - Type "exit" to end the session.
4. Feedback:
    - Optionally provide feedback on responses after the session ends.

## Data

- CSV File: `fashion_dataset.csv` from Myntra.
