# Generative-AI-Healthcare-Bot-with-RAG-Pipeline

<img width="678" alt="image" src="https://github.com/user-attachments/assets/70b401ec-8ef5-4bd9-a41e-f51a0c1dcef6">


## Multimodal RAG Application for Healthcare
### Overview
This project showcases a cutting-edge Multimodal Retrieval Augmented Generation (RAG) application tailored for medical use cases. By integrating GPT-4V with an embedding model and a vector database, the application offers precise, context-aware responses to user queries, including relevant images extracted from PDF documents.
![image](https://github.com/user-attachments/assets/067035fc-ae0b-41be-b193-07a50318ea51)

### Features
Multimodal Capabilities: Combines text and visual data for comprehensive query responses.
Advanced AI Integration: Utilizes GPT-4V for generating detailed and accurate responses.
Efficient Backend: Built with FastAPI for high-performance API handling.
Document Processing: Leverages the unstructured library to process tables and images within PDFs.
Healthcare Focused: Designed specifically for medical use cases, enhancing data retrieval and user interaction.

### Technology Stack
GPT-4V: Versatile large language model for generating responses.
FastAPI: Modern, fast web framework for building APIs with Python.
Vector Database: Ensures efficient data retrieval and management.
Unstructured Library: Handles diverse data types such as tables and images in PDF documents.

Setting Up the Multimodal RAG Application
We will build this application using several powerful tools and libraries:

Unstructured: A library that helps extract and process data from various formats like PDFs, including text, tables, and images.
FastAPI: A modern web framework for building APIs with Python.
LangChain: An orchestration framework that facilitates working with language models.
Step 1: Setting Up the Environment
First, we set up our environment using Google Colab to write and run our code. We begin by installing the necessary libraries, including unstructured, LangChain, OpenAI, and FastAPI.

Step 2: Extracting and Processing Data
Using the Unstructured library, we extract data from a sample PDF related to canine periodontal disease. This step involves extracting both the textual content and the images embedded within the PDF.

We use an ONNX-based object detection model to identify and extract images, which are then saved locally. This process ensures that our application can handle and retrieve multimodal data effectively.

Step 3: Summarizing and Storing Data
Next, we summarize the extracted text and tables using the GPT-3.5 Turbo model. For images, we use GPT-4 Vision to generate detailed descriptions. All this data is then stored in a vector store, which allows for efficient retrieval during the application’s runtime.

Step 4: Building the FastAPI Application
With our vector store ready, we move on to building the FastAPI application. The app allows users to query the multimodal data by sending a request via the API. The response includes both the relevant text and images, providing a comprehensive answer to the user’s query.

Step 5: Deploying the Application
In the upcoming articles, we will cover how to:

Use open-source models like LLaVA for the same application.
Deploy the application on AWS using EC2, making it accessible for real-world use cases.
