# **HemaBridge: AI-Driven Blood Cancer Detection & Care**  
**Version:** 1.0.0  
---

## **Project Overview**  
HemaBridge is an **AI-powered blood cancer detection system** designed to assist **doctors and patients** in diagnosing and monitoring blood-related disorders. It integrates **deep learning models, automated reporting, and an AI chatbot** to enhance medical diagnostics and streamline patient care.  

### **Key Features**  
✅ **AI-based Blood Cell Analysis** – Detects potential cancerous cells using a pre-trained deep learning model.  
✅ **Automated Report Generation** – Creates professional PDF reports with detailed analysis and recommendations.  
✅ **AI Medical Chatbot** – Provides symptom analysis, medical insights, and basic healthcare guidance.  
✅ **User Authentication & Roles** – Secure access with **separate dashboards for patients and doctors**.  
✅ **Appointment Management** – Patients can book consultations with doctors within the platform.  
✅ **Multi-Language Support** – Chatbot available in **English, French, and Spanish**.  

---

## **Installation Guide**  



#### Installation

1. **Clone the Repository**:
   ```
   git clone https://github.com/sumithsingh/AL_project.git
   cd AL_project
   ```

2. **Set Up a Virtual Environment**:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```
   
3. **Install Dependencies**:
   ```
   pip install -r requirements.txt
   ```

4. **Configure Environment Variables**:
   Create .env file and update the following:
   ```
   DATABASE_URL=postgresql://user:password@localhost:5432/blood_cancer_db
   SECRET_KEY=your-secure-secret-key
   MODEL_PATH=model/blood_cancer_model.keras
   ```

5. **Set Up the Database**:
   Run the following command to initialize the database:
   ```
   python backend.py
   ```
---
### Running the Application

1. **Start the Backend (FastAPI)**:
   ```
   uvicorn backend:app --host 0.0.0.0 --port 8000 --reload
   ```
2. **Run the Frontend (Streamlit)**:
   ```
   streamlit run frontend.py
   ```
   The user interface will be available at http://localhost:8501.
---
### Project Structure
```

AL_project/
│
├── model/
│   └── blood_cancer_model.keras
│
├── backend.py
├── chatbot.py
├── create_user.py
├── frontend.py
├── model_handler.py
├── report_generator.py
├── requirements.txt
├── .env
├── .gitignore
└── README.md
```
---

### Dependencies
The project uses the following Python packages:

📌Machine Learning & AI
* tensorflow >= 2.18.0
* torch >= 2.5.1
* transformers >= 4.48.1

📌 Web Framework & API
* fastapi >= 0.115.7
* uvicorn >= 0.34.0

📌 Database & Authentication
* SQLAlchemy >= 2.0.37
* psycopg2-binary >= 2.9.10

📌 Frontend
* streamlit >= 1.41.1
  
📌 PDF & Data Processing
* reportlab >= 4.2.5
* pandas >= 2.2.3
* numpy >= 2.0.2
* matplotlib >= 3.10.0
---
### Usage Guide
### For Patients
* 🩸 Upload Blood Test Images – Analyze blood cell samples for abnormalities.
* 💬 Chat with AI Assistant – Get medical guidance and symptom insights.
* 📑 View & Download Reports – Access test results with recommendations.
* 📅 Book Appointments – Schedule consultations with doctors.

### For Doctors
* 📝 View Patient Reports – Access AI-generated risk assessments.
* 📊 Monitor Risk Levels – Evaluate patient conditions.
* 📅 Manage Appointments – Accept or reject patient consultations.

---
### Security & Authentication
* Uses JWT authentication for secure login sessions.
* Doctors and patients have separate access controls to manage data securely.
* Passwords are hashed using bcrypt.

---



