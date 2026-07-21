# College Assistant (RAG + LangGraph)

An intelligent **AI-powered College Assistant** built using **LangGraph, RAG (Retrieval-Augmented Generation), and LLMs**.
This assistant helps students by answering queries related to **academics, fees, and general questions** using official college documents.

---

##  Features

*  **Query Classification**

  * Automatically classifies user queries into:

    * Academic
    * Fee
    * General

* **RAG-based Retrieval**

  * Uses PDF documents (Academic Handbook & Fee Structure)
  * Retrieves relevant context using **FAISS + HuggingFace Embeddings**

* **LLM-Powered Responses**

  * Uses **Groq LLM (LLaMA 3.3 70B)** for generating accurate answers

* **Personalized Responses**

  * Tailors answers based on student programme (BCA, BBA, B.Com)

* **Multi-Agent Workflow**

  * Built using **LangGraph state-based pipeline**
  * Modular nodes for classification, retrieval, and response generation

---

## 🏗️ Tech Stack

* **LangGraph**
* **LangChain**
* **Groq LLM (llama-3.3-70b-versatile)**
* **FAISS (Vector Database)**
* **HuggingFace Embeddings**
* **Python**

---

## 📂 Project Structure

```
📁 College-Assistant
│── main.py
│── academics_handbook.pdf
│── fee_structure.pdf
│── .env
│── README.md
```



###  Setup Environment Variables

Create a `.env` file and add:

```env
GROQ_API_KEY=your_api_key_here
```

---


## 🧠 How It Works

1. **User Input**
2. → Classifier Node (Academic / Fee / General)
3. → RAG Retrieval (if needed)
4. → Response Generation using LLM
5. → Output to user

---

## 🔁 LangGraph Flow

```
START → Classifier
        ↓
   ┌───────────────┐
   │ Academic RAG  │
   │ Fee RAG       │
   │ General       │
   └───────────────┘
        ↓
     Response → END
```


⭐ If you like this project, give it a star on GitHub!
