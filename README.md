# **D-BOTT: Doctor’s Bot for Operational Trackers**

---

## **Introduction**  

D-BOTT is a real-time document query system that allows users to upload PDFs and interact with them via **text or voice commands**. It utilizes **Google Gemini AI** for processing queries and **LlamaIndex** for document retrieval, enabling intelligent responses based on indexed documents.

---

## **Features**
✅ **Upload and Index PDFs** - Users can upload PDF documents that are indexed for future queries.  
✅ **AI-Powered Queries** - Users can ask questions about uploaded documents, and the AI retrieves relevant responses.  
✅ **Voice and Text Input** - Interact with the system using either text input or real-time voice commands.  
✅ **WebSocket-Based Communication** - Ensures seamless real-time interaction between client and server.  

---

## **Project Structure**
```
/d-bott
│── main.py                  # WebSocket server and AI logic
│── index.html                # Frontend UI for user interaction
│── pcm-processor.js          # Handles audio processing in WebAssembly
│── downloads/                # Stores uploaded PDFs
│── storage/                  # Stores indexed document embeddings
│── README.md                 # This file
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
pip install -U google-genai==0.5.0 llama-index==0.12.11 llama-index-llms-gemini==0.4.3 llama-index-embeddings-gemini==0.3.1 websockets
```

### **3. Set Up Google Gemini API Key**
Replace `"YOUR_GEMINI_API_KEY"` with your actual Google API key:
```sh
export GOOGLE_API_KEY="YOUR_GEMINI_API_KEY"
```

### **4. Run the WebSocket Server**
```sh
python main.py
```
The server starts on **localhost:9084**.

---

## **How It Works**
1. **Upload a PDF** via the web interface.  
2. The document is **processed and indexed** using LlamaIndex.  
3. Users can **ask questions** about the document via **text or voice commands**.  
4. **Google Gemini AI** searches the indexed data and returns an answer.  
5. The response is **displayed in the chat box** or played as **audio**.  

---

## **Frontend (index.html)**
- **Provides a UI** for uploading PDFs and querying documents.  
- Uses **Material Design Lite (MDL)** for styling.  
- Supports **real-time voice control** via a toggle switch.  
- Connects to the **WebSocket server** to send and receive data.  

---

## **Backend (main.py)**
- **Handles WebSocket connections** and processes real-time user queries.  
- Uses **Google Gemini AI** for AI-driven responses.  
- **Stores and indexes PDFs** using LlamaIndex for fast retrieval.  
- Supports **audio and text-based interactions**.  

---

## **Audio Processing (pcm-processor.js)**
- **Processes raw PCM audio** and streams it for AI-based speech recognition.  
- Implements **Web Audio API's AudioWorkletProcessor** for efficient handling.  

---

## **Usage**
### **1. Open the Web UI**
Navigate to:  
```
http://localhost:9084
```
### **2. Upload a PDF**
- Click **Upload** and select a PDF.  
- The file is indexed and ready for queries.  

### **3. Ask a Question**
- Type a question in the **chat box** or use the **voice toggle** for speech input.  

### **4. Get AI-Powered Responses**
- AI extracts relevant answers from the PDF.  
- Responses are displayed in text or played as audio.  

---

## **Troubleshooting**
🔹 **WebSocket Connection Issues**  
- Ensure the server is running on `localhost:9084`.  
- Check your WebSocket URL in `index.html`.  

🔹 **PDF Not Indexing**  
- Ensure the `downloads/` directory exists.  
- Try restarting the server after uploading a document.  

🔹 **Audio Not Working**  
- Ensure your microphone is enabled.  
- Try switching browsers (Chrome recommended).  

---

## **Future Enhancements**
🚀 Support for **multiple document indexing**.  
🎤 Improved **speech-to-text accuracy**.  
☁️ Deployment as a **cloud-based application**.  

---

## **License**
This project is licensed under the **MIT License**.  

---

## **Contributors**
👨‍💻 **[FARDEEN S KHADRI]** - Developer
👨‍💻 **[ANUSHA RAO M]** - Developer
👨‍💻 **[SPOORTHI R C]** - Developer
👨‍💻 **[SHREE PRIYA V]** - Developer
👨‍💻 **[MANOJ GOWDA R]** - Developer  
 

