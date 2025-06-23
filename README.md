# BonBon FAQ Assistant

## Overview

This project is a customer support chatbot powered by LangChain and Azure OpenAI, able to answer frequently asked questions from the provided BonBon FAQ.pdf and search the internet when needed.

It supports conversation context and leverages both Azure OpenAI GPT-3.5 and Azure Cognitive Search/ChromaDB.

## Features

* **Conversational agent** using Azure OpenAI GPT-3.5 (or GPT-4o if configured)
* **Knowledge Base search** : answers from BonBon FAQ.pdf (with page citation)
* **Internet search** fallback using DuckDuckGo
* **Context awareness** with conversation memory

## Getting Started

### 1. **Clone the repository**

git clone `<your-repo-url>`
cd BonBon_Assignment-main

### 2. **Set up environment variables**

Create a `.env` file in the project root:

OPENAI_API_TYPE=azure
OPENAI_API_KEY=your-azure-api-key
AZURE_OPENAI_API_VERSION=2024-12-01-preview
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=text-embedding-3-small-deployment
AZURE_OPENAI_CHAT_DEPLOYMENT=gpt-35-turbo-deployment

### 5. **Run the Chatbot**

* Start the chatbot script (or use provided `assignment.ipynb` notebook):


## Usage

* The bot will **first try to answer from the BonBon FAQ** (and cite the source and page).
* If the answer is not in the FAQ, it will **search the internet** using DuckDuckGo.
* Example prompt:

  User: How do I reset my VPN password?
  🤖 Answer:
  [Answer from FAQ with citation]
* To exit, type `exit`.