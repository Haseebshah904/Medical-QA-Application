# Medical Question-Answering System
A medical question-answering system that allows users to input a question and retrieve answers based on context derived from medical documents. The system is built using FastAPI, integrates Pinecone for indexing and efficient similarity search, uses Groq LLM for generating answers, and provides a user-friendly interface using Gradio. This project is deployed on Hugging Face Spaces for public access.
# Project Overview
The Medical Question-Answering System is designed to help users get accurate and relevant medical answers by asking natural language questions. It uses the Pinecone vector database for fast and efficient similarity-based search over indexed medical content. The system leverages Groq LLM, a cutting-edge large language model, to generate high-quality answers based on the retrieved context.
The backend is built with FastAPI, while the front-end is provided by a Gradio interface for seamless user interaction. This system is hosted on Hugging Face Spaces for easy public access.
# Features
+ Question-Answering: Users can input questions, and the system will retrieve the most relevant answers from medical data.
+ Pinecone Indexing: Efficient indexing and retrieval of context based on vector similarity search using Pinecone.
+ Gradio Interface: A simple interface for users to ask medical-related questions and receive answers.
+ FastAPI Backend: FastAPI handles requests, retrieves context from Pinecone, and integrates with Groq LLM for answer generation.
+ Hugging Face Deployment: Deployed on Hugging Face Spaces, ensuring scalability and public accessibility.
# Installation
To run this project locally, you can follow these steps:
## 1. Clone the Repository
+ git clone https://github.com/yourusername/medical-question-answering-system.git
+ cd medical-question-answering-system
## 2. Set Up the Environment
+ Create a virtual environment and install the required dependencies:
+ python3 -m venv venv
+ source venv/bin/activate   # On Windows, use venv\Scripts\activate
+ pip install -r requirements.txt
## 3. Set Up Pinecone
+ Before running the system, you need to set up Pinecone to index and search for relevant medical content.
+ Create a Pinecone account and get your API Key: Pinecone.
+ Initialize Pinecone in your code:
+ pip install pinecone-client
+ Then, set the API key and environment:
+ import pinecone
+ pinecone.init(api_key="YOUR_PINECONE_API_KEY", environment="us-west1-gcp")  # Replace with your API key and environment
# How It Works
## System Workflow
## Index Medical Documents:
+ Medical documents are converted into embeddings (vectors) using a pre-trained model.
+ These embeddings are stored in Pinecone for efficient similarity-based retrieval.
## Question Processing:
+ When a user submits a question, it is converted into a query embedding.
+ The system retrieves the most relevant context from Pinecone by calculating the vector similarity.
## Answer Generation:
+ The retrieved context is passed to Groq LLM, which generates a relevant and detailed medical answer.
User Interaction:
+ The question and answer are displayed in the Gradio interface, allowing for seamless interaction.
## API Endpoints
+ The system exposes the following API endpoints:
+ POST /ask
+ Description: Accepts a user’s question and returns the generated answer.
## How It Works Behind the Scenes:
+ The question is converted into a query embedding using a pre-trained model.
+ The Pinecone index is searched for the most relevant context based on vector similarity.
+ The context is passed to Groq LLM, which generates the answer.
# Gradio Interface
+ The Gradio interface allows users to interact with the system through a simple UI.
+ Textbox: Users can type their medical-related questions into a textbox.
+ Output: The generated answer is displayed in the output area.
# Deployment
The system is deployed on Hugging Face Spaces, allowing public access. To deploy:
+ Create a Hugging Face Account: Hugging Face.
+ Create a New Space:
+ Choose Gradio as the environment.
+ Link your GitHub repository.
+ Push Your Code:
+ Push your project to the repository linked to the Hugging Face Space.
+ The deployment will automatically begin, and you can access the system via the provided Hugging Face URL.
# Output
 ![Image Alt]([image_url](https://github.com/Haseebshah904/Medical-QA-Application/blob/main/MedicalQA%20Output%201.PNG?raw=true)).
 ![Image Alt](image_url).
 # Usage
+ Access the System:
+ Visit the deployed Hugging Face Space.
+ Enter your question in the Gradio interface.
 +Example Questions:
+ "What are the side effects of aspirin?"
+ "How does diabetes affect the body?"
+ Answer Generation:
+ The system retrieves context from Pinecone and generates an answer using Groq LLM.
