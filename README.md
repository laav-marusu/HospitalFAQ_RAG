
# Hospital FAQ & Appointment Helper

## 1. Project Overview

The **Hospital FAQ & Appointment Helper** is a Retrieval-Augmented Generation (RAG) based application designed to help users access hospital-related information and appointment details easily.

The system allows users to ask questions about hospital facilities, departments, doctors, OPD timings, consultation fees, and appointment rules. It retrieves relevant information from hospital documents and generates answers using a Large Language Model (LLM).

The application also provides an appointment assistance feature where users can enter their details and book an appointment.

## 2. Problem Statement

Patients and visitors often face difficulties finding accurate information about hospital departments, doctor availability, consultation fees, and appointment procedures.

This project aims to provide a simple, user-friendly platform that makes hospital information easily accessible and helps users with the appointment process.

## 3. Objectives

- Provide quick answers to frequently asked hospital-related questions.
- Retrieve relevant information from hospital documents using RAG.
- Provide information about doctors and departments.
- Display OPD timings and consultation fees.
- Assist users with appointment booking.
- Store appointment details using an SQLite database.
- Reduce the need to search through multiple hospital documents manually.

## 4. Key Features

- **Hospital FAQ Assistant:** Answers questions using information retrieved from hospital documents.
- **Doctor Information:** Provides doctor names and their respective departments.
- **Department Information:** Displays available hospital departments.
- **OPD Timings:** Provides department-wise consultation timings.
- **Fee Information:** Displays consultation and selected service fees.
- **Appointment Assistance:** Allows users to submit appointment details.
- **Database Storage:** Stores appointment records using SQLite.

## 5. Technology Stack

| Technology | Purpose |
|---|---|
| Python | Main programming language |
| Streamlit | User interface |
| LangChain | RAG workflow |
| PyPDF | PDF document loading |
| Sentence Transformers | Text embeddings |
| FAISS | Vector database |
| Gemini API | LLM-based answer generation |
| SQLite | Appointment data storage |

## 6. System Architecture

The project consists of two main modules:

### A. RAG-Based Hospital FAQ Assistant

1. Hospital documents are stored in the documents folder.
2. Documents are loaded and their text is extracted.
3. Text is divided into smaller chunks.
4. Sentence Transformer generates embeddings.
5. Embeddings are stored in the FAISS vector database.
6. When a user asks a question, relevant chunks are retrieved.
7. The retrieved information is provided to the Gemini model to generate an answer.

### B. Appointment Assistance Module

1. User enters appointment details.
2. The application collects the required information.
3. Appointment details are stored in SQLite.
4. The application displays the appointment confirmation.

## 7. Project Folder Structure

```text
HospitalFAQ_RAG/
│
├── documents/
│   ├── hospital_information.txt
│   ├── departments.txt
│   ├── doctors.txt
│   ├── opd_timings.txt
│   ├── fees.txt
│   └── appointment_rules.txt
│
├── vectorstore/
│
├── venv/
│
├── app.py
├── create_vectorstore.py
├── test_retrieval.py
├── requirements.txt
├── .env
└── README.md
```

## 8. Installation and Setup

### Step 1: Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### Step 2: Open the Project Folder

```bash
cd HospitalFAQ_RAG
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 4: Activate the Virtual Environment

For Windows:

```bash
venv\Scripts\activate
```

### Step 5: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 6: Configure the Gemini API Key

Create a `.env` file in the project folder and add:

```env
GOOGLE_API_KEY=your_gemini_api_key
```

Do not upload your actual API key to GitHub.

### Step 7: Create the Vector Database

```bash
python create_vectorstore.py
```

### Step 8: Run the Application

```bash
streamlit run app.py
```

## 9. Example Questions

Users can ask questions such as:

- What are the hospital OPD timings?
- Who is the cardiologist?
- What departments are available?
- What is the consultation fee?
- What are the dermatology OPD timings?
- How can I book an appointment?

## 10. Expected Results

The application is intended to:

- Retrieve relevant hospital information from the knowledge base.
- Generate answers based on the retrieved documents.
- Display doctor, department, fee, and OPD information.
- Collect appointment details and store them in the database.

Actual performance and testing results will be added after implementation and testing.

## 11. Future Enhancements

- Add online appointment cancellation and rescheduling.
- Add appointment status tracking.
- Integrate email or SMS notifications.
- Add multilingual support.
- Improve the user interface.
- Deploy the application online.

## 12. Disclaimer

This project is developed for educational and demonstration purposes using fictional hospital information. It does not provide medical diagnosis or treatment recommendations. Users should contact qualified healthcare professionals for medical advice.

---
## AUTHOR
MARUSU LAVANYA

GitHub: https://github.com/dashboard

Project Repository:

https://github.com/laav-marusu/HospitalFAQ_RAG.git

live link:

https://hospital-react-gamma.vercel.app/


**Project Name:** Hospital FAQ & Appointment Helper  
**Project Type:** Retrieval-Augmented Generation (RAG)  
**Purpose:** Hospital Information Retrieval and Appointment Assistance
