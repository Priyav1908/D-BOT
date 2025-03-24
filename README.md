# **D-BOTT: Doctor’s Bot for Operational Trackers Technology**

---

## **Introduction**  

D-BOTT is a real-time document query system that allows users to upload PDFs and interact with them via **text or voice commands**. It utilizes **OLLAMA** for processing queries and **LlamaIndex** for document retrieval, enabling intelligent responses based on indexed documents.

---


---

## **Project Structure**
```
/d-bott
│── main.py                  # WebSocket server and AI logic
│── index.html                # Frontend UI for user interaction
│── pcm-processor.js          # Handles audio processing in WebAssembly

```

---

## **Installation**
### **1. Clone the Repository**
```sh
git clone https://github.com/fardeenKhadri/D-BOT
cd d-bott
```

### **2. Install Dependencies**
Ensure Python 3.8+ is installed, then run:
```sh
pip install  llama-index==0.12.11 
```

### **3. Set Up API Key**
Replace `"OLLAMA_API_KEY"` with your actual OLLAMA API key:


### **4. Run the WebSocket Server**
```sh
python main.py
```
The server starts on **localhost:9084**.

---
