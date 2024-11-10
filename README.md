
# Multimodal Retrieval with Deep Lake, Bedrock, and AI Integrations 
This project showcases a multimodal retrieval system combining the **Deep Lake**  REST API, **Bedrock** , and **OpenAI**  for image and text processing. It allows users to query a dataset with text prompts, retrieve relevant images, and leverage AI models for context-aware responses.
## Overview 

This solution is designed to enable multimodal data retrieval and answer generation by:
 
- **Querying Datasets** : Supports querying datasets in Deep Lake and retrieving top matches based on text-based queries.
 
- **AI-Powered Insights** : Uses Bedrock and OpenAI models for answering questions about retrieved images or text segments.
 
- **Deep Memory** : Integrates deep memory retrieval to enhance context-aware responses, leveraging the Deep Lake database for improved AI-driven answers.

## Project Components 
1. Main Retrieval and Processing (`main.py`)

    The core script:

    - Queries Deep Lake datasets based on user-defined prompts.

    - Uses Bedrock and Deep Lake integrations to retrieve relevant images.
    
    - Leverages functions from `bedrock_code.py` and `deeplake_deepmemory.py` to generate context-aware answers from images and text.

    - Saves and displays retrieved images for each query.
2. Bedrock Integration (`bedrock_code.py`)

    This file provides:
    
    - Functions to send messages to Bedrock’s AI models (e.g., Claude 3 Sonnet) using the AWS `boto3` client.

    - Supports both image and text-based question-answering by converting inputs into compatible formats for Bedrock’s AI models.

    - A sample use case for processing an image with Bedrock’s API.
3. Deep Memory and Embedding (`deeplake_deepmemory.py`)

    This module includes:

    - Functions to retrieve context from a Deep Lake vector database based on user queries.

    - An embedding function using OpenAI’s embedding model for efficient text similarity and context-aware retrieval.

    - Options to enable or disable deep memory


4. Utility Functions (`utils.py`)

    Helper functions to:

    - Convert images to byte format for API compatibility.

    - Structure messages for both text and image prompts, formatting them to interact with Bedrock and OpenAI models.

    - Generate embeddings for text inputs using OpenAI’s API.

5. Notebook Examples (`notebook_bedrock.ipynb` and `notebook.ipynb`)

    Notebooks demonstrate how to use the multimodal retrieval system:
 
    - **Multimodal Retrieval with Bedrock and Deep Lake** : Examples of setting up queries, sending them to the Deep Lake API, and processing responses.
    
    - **Visualization** : Displays images retrieved based on query results and shows how Bedrock can answer questions about these images.
6. Requirements (`requirements.txt`)
The necessary Python libraries for this project:
 
    - `deeplake V3`: For handling datasets and vector stores.
    
    - `openai`: To access embedding functions for text processing.

## Installation 

Install the necessary dependencies:


```bash
pip install -r requirements.txt
```

## Environment Setup 

Define environment variables for secure access to APIs:
 
- `TOKEN`: Deep Lake API access token.
 
- `AWS_ACCESS_KEY_ID` and `AWS_SECRET_ACCESS_KEY`: AWS credentials for Bedrock.
 
- `ACTIVELOOP_TOKEN`: Token for ActiveLoop’s Deep Lake.
 
- `OPENAI_API_KEY`: OpenAI API key for embedding functions.

