# EduVisionBot: A Question-Answering Assistant with Contextualization
This project builds a question-answering assistant named EduVisionBot that can reformulate user questions based on conversation history and then answer them using a Retrieval-Augmented Generation (RAG) approach.

## Dependencies
This code requires the following Python libraries:

requests

beautifulsoup4

fitz

langchain (including submodules langchain.text_splitter,

langchain.embeddings.huggingface, 

langchain_community.vectorstores, 

langchain_community.llms,

langchain_core.output_parsers,

langchain_core.prompts, 

and langchain_core.runnables)

gradio

Note: Installation instructions for these libraries can be found on their respective websites or using the pip package manager.

## Functionality Overview
PDF Text Extraction: The code first retrieves a list of PDF links from a user-specified URL (e.g., arXiv). It then downloads and extracts text from each PDF using PyMuPDF.

Question Reformulation: The code utilizes a large language model (LLM) to reformulate user questions based on the conversation history. This ensures questions are clear and understandable even without context.

Retrieval-Augmented Generation (RAG): The system leverages a FAISS vector store to retrieve relevant context from previous questions and answers. This retrieved context is then incorporated into a prompt for the LLM to answer the user's question.

Interactive Interface: The code is implemented using Gradio to create a user-friendly chatbot interface. Users can interact with EduVisionBot by typing their questions, and the system will reformulate and answer them based on the conversation history.

## Usage
Install Dependencies: Ensure you have all the required libraries installed using pip.

Run the Script: Execute the Python script using a Jupyter Notebook environment or a regular Python interpreter.

Interact with the Chatbot: The Gradio interface will launch, allowing you to type your questions and see the chatbot's responses.

## Additional Notes
This code is a starting point and can be further customized for specific use cases.

The provided URL in the script retrieves only one PDF for demonstration purposes. You can modify it to extract from a larger list.
