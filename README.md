# Experiment 13: RAG Chain Using LCEL and FAISS

## Aim
To construct a Retrieval-Augmented Generation (RAG) chain using LangChain Expression Language (LCEL), FAISS, and Gemini to answer questions based on an indexed climate-change document.

## Problem Statement
Build a RAG pipeline that retrieves relevant text chunks, combines them with a question, and generates an answer grounded in the retrieved context.

## Tools and Technologies
- Python
- Google Gemini API
- LangChain
- LCEL
- FAISS vector store
- Google Colab

## Algorithm
1. Configure the Gemini API key.
2. Define a sample climate-change document.
3. Split the document into chunks using `RecursiveCharacterTextSplitter`.
4. Generate embeddings using `GoogleGenerativeAIEmbeddings`.
5. Create a FAISS vector store.
6. Convert the vector store into a retriever with `k=2`.
7. Define a prompt that instructs the model to use only the retrieved context.
8. Build the LCEL chain using the pipe operator.
9. Test the chain with two questions.
10. Display the generated answers and retrieved chunks.
11. Save the results in `output.txt`.

## LCEL Chain
The chain combines the retriever, prompt template, Gemini model, and string output parser.

## Test Questions
1. What are the effects of climate change?
2. What causes climate change, and how can it be reduced?

## Expected Output
The program prints answers generated from the retrieved text and displays the retrieved chunks for verification.

## Conclusion
This experiment demonstrates how retrieval and language generation can be combined in an LCEL pipeline. Using retrieved context helps ground answers in the indexed document and makes the information used for answering easier to inspect.
