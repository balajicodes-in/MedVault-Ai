🏥 MedVault AI

From Scattered Medical Reports to One Secure Patient Story

«AI-powered Medical Document Intelligence & Patient Timeline»

MedVault AI is a healthcare technology platform designed to transform fragmented medical documents into a structured, chronological view of a patient's medical history.

The project was developed as part of a 24-hour Healthcare Hackathon organized by KPR Institute of Engineering and Technology (KPRIET), Coimbatore, where our team was selected among the Top 50 teams out of 200+ participating teams.

---

🏆 Hackathon Achievement

Achievement| Details
🏫 Organizer| KPR Institute of Engineering and Technology (KPRIET), Coimbatore
⏱️ Event| 24-Hour Healthcare Hackathon
🏆 Selection| Top 50 Teams
👥 Participation| 200+ Teams
🏥 Domain| Healthcare
🎯 Problem Statement| HE-05 — Medical Document Intelligence & Patient Timeline

---

📌 Problem Statement

Patient information is frequently distributed across different medical documents such as:

- Laboratory reports
- Prescriptions
- Discharge summaries
- Imaging reports
- Clinical notes

Understanding a patient's complete medical history requires connecting information across these different documents.

The HE-05 challenge is to build a medical-document intelligence system that:

- Extracts relevant structured information
- Understands different document types
- Organizes relevant medical information
- Orders information chronologically
- Generates a patient-event timeline
- Identifies relationships between medical events
- Provides clear traceability to source documents

🎯 Key Challenge

«Transform fragmented medical documentation into a coherent longitudinal view of a patient's history.»

---

💡 Our Solution

MedVault AI addresses this challenge by creating a centralized medical-document intelligence platform.

The system follows the workflow:

Medical Documents
       ↓
Document Processing
       ↓
Information Extraction
       ↓
Structured Medical Data
       ↓
Chronological Timeline
       ↓
Summary & Retrieval
       ↓
Doctor / Patient Access

The system is designed around an important principle:

«NO SOURCE, NO MEDICAL DATA»

Medical information should originate only from authorized manual entry or uploaded medical documents.

AI is used to extract, structure, summarize, and retrieve information — not to invent patient medical data.

---

✨ Key Features

📄 Medical Document Intelligence

Process different types of medical documents, including:

- Laboratory reports
- Prescriptions
- Discharge summaries
- Imaging reports
- Clinical notes

The system extracts relevant information from the source document and converts it into structured data.

---

🕒 Patient Timeline

Medical events are organized chronologically to provide a longitudinal view of the patient's history.

Example:

2026-01-10
    ↓
Laboratory Test

2026-01-15
    ↓
Doctor Consultation

2026-01-15
    ↓
Prescription

2026-02-10
    ↓
Follow-up Test

---

🔗 Medical Event Relationships

MedVault AI can represent relationships between medical events.

Example:

Blood Test
    ↓
Doctor Consultation
    ↓
Prescription
    ↓
Follow-up Test

This helps users understand how different events in the medical history are connected.

---

🔍 Source Traceability

Extracted information should remain traceable to its original source document.

Example:

Hemoglobin
12.4 g/dL

Source:
Blood_Report.pdf
Page 2

Status:
High Confidence

If information cannot be reliably extracted:

⚠️ Needs Verification

If information is not present:

Not available in source document

---

👥 Role-Based Access

MedVault AI uses role-based access to separate responsibilities.

Role| Access
👨‍⚕️ Doctor| Authorized patient records, documents, timeline, appointments
🧪 Lab Assistant| Patient creation and document upload
👤 Patient| Own medical records and timeline
🛡️ Admin| User and system management

Lab Assistant

The lab assistant can:

- Create a new patient
- Generate a patient ID
- Enter basic patient information
- Upload medical documents
- Upload documents for an existing patient ID

The lab assistant cannot browse the patient's complete medical history.

Doctor

The doctor can:

- Search patients by patient ID
- View authorized medical information
- View source documents
- View the patient timeline
- Review extracted information
- Create appointments

Patient

The patient can:

- Log in using their patient ID
- View their own medical history
- View their timeline
- View uploaded documents
- View appointments
- Ask questions about their available medical records

Admin

The admin can:

- Create doctor accounts
- Create lab assistant accounts
- Manage users
- Disable accounts
- View audit logs
- Manage system settings

---

🆔 Patient ID System

For the hackathon prototype, patient IDs are generated sequentially.

P1000
P1001
P1002
P1003
...

The IDs are:

- Unique
- Sequential
- Persistent
- Automatically generated

Prototype Login

For demonstration purposes:

Patient ID: P1000
Password: P1000

«⚠️ This password design is intended only for the hackathon prototype. A production healthcare system should use secure authentication, password hashing, reset mechanisms, and stronger identity verification.»

---

🤖 AI Medical History Assistant

MedVault AI includes an AI-powered assistant that can retrieve and summarize information from the patient's available records.

Example questions:

How many hospital visits have I had?

What tests were performed?

What was my previous prescription?

When is my next appointment?

Show my previous laboratory results.

What happened during my last hospital visit?

The assistant should answer using available source-backed records.

If information is unavailable:

Not available in source document.

The AI should not invent missing patient information.

---

⚠️ Conflict Detection

When conflicting medication information is found, the system should not decide which medication is correct.

Instead, it displays:

«"Conflicting medication information found. Please verify with the doctor."»

This keeps the final medical decision with the appropriate healthcare professional.

---

🏥 Multi-Hospital Support

The platform can associate medical documents and appointments with different hospitals or healthcare organizations.

Example:

Hospital A
    ↓
Blood Report

Hospital B
    ↓
Doctor Consultation

Hospital C
    ↓
Imaging Report

This allows the patient's longitudinal history to remain connected even when information originates from different healthcare organizations.

---

🔐 Security & Privacy

Because medical information is sensitive, MedVault AI follows a role-based access approach.

Key principles include:

- Role-Based Access Control
- Restricted patient access
- Authorized doctor access
- Limited lab assistant access
- Audit logging
- Source traceability
- Controlled document access
- Secure database storage

Data Principle

NO SOURCE
    ↓
NO MEDICAL DATA

The application should never generate fake patient medical information.

---

🏗️ System Architecture

                    ┌──────────────────────┐
                    │      Users           │
                    │ Doctor / Patient     │
                    │ Lab / Admin          │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │   React Web App      │
                    │ Tailwind + shadcn/ui │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │    Flask Backend     │
                    │      Python API      │
                    └──────────┬───────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
      ┌─────────────┐   ┌─────────────┐   ┌──────────────┐
      │ PyMuPDF     │   │ Tesseract   │   │ Gemini API   │
      │ PDF Parsing │   │ OCR         │   │ AI Processing│
      └──────┬──────┘   └──────┬──────┘   └──────┬───────┘
             │                 │                 │
             └─────────────────┼─────────────────┘
                               ▼
                    ┌──────────────────────┐
                    │ Structured Medical  │
                    │ Information          │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ Supabase / PostgreSQL│
                    │ Database + Storage   │
                    └──────────┬───────────┘
                               │
             ┌─────────────────┼─────────────────┐
             ▼                 ▼                 ▼
      ┌─────────────┐   ┌─────────────┐   ┌─────────────┐
      │ Patient     │   │ Doctor      │   │ Admin       │
      │ Timeline    │   │ Dashboard   │   │ Dashboard   │
      └─────────────┘   └─────────────┘   └─────────────┘

---

🛠️ Technology Stack

Frontend

- React.js
- Tailwind CSS
- shadcn/ui
- Recharts
- React Flow

Backend

- Python
- Flask

AI

- Google Gemini API

Document Processing

- PyMuPDF
- Tesseract OCR

Database & Storage

- Supabase
- PostgreSQL
- Supabase Auth
- Supabase Storage

Notifications

- Email
- SMS
- In-app notifications

---

📂 Project Structure

A recommended project structure:

medvault-ai/
│
├── frontend/
│   ├── src/
│   ├── components/
│   ├── pages/
│   ├── services/
│   └── App.jsx
│
├── backend/
│   ├── app.py
│   ├── routes/
│   ├── services/
│   ├── models/
│   ├── document_processing/
│   └── ai/
│
├── database/
│   └── schema.sql
│
├── docs/
│   ├── architecture/
│   └── screenshots/
│
├── .env.example
├── .gitignore
├── README.md
└── LICENSE

---

🗄️ Core Data Model

The system can maintain entities such as:

Patients
   │
   ├── Documents
   │       └── Medical Events
   │
   ├── Appointments
   │
   └── Notifications

Example tables

patients
documents
medical_events
appointments
audit_logs

---

🔄 Patient Workflow

1. Create Patient

Lab Assistant
      ↓
Create New Patient ID
      ↓
System generates P1000
      ↓
Enter Basic Patient Details

2. Upload Document

Lab Assistant
      ↓
Enter Patient ID
      ↓
Upload Medical Document
      ↓
Document Processing

3. Extract Information

PDF / Image
      ↓
PyMuPDF / OCR
      ↓
Gemini AI
      ↓
Structured Information

4. Generate Timeline

Extracted Medical Events
          ↓
Date Identification
          ↓
Chronological Ordering
          ↓
Patient Timeline

5. Doctor Review

Doctor Login
     ↓
Search Patient ID
     ↓
View Authorized Records
     ↓
Review Timeline & Documents
     ↓
Create Appointment

6. Patient Access

Patient Login
     ↓
Patient ID + Password
     ↓
Own Medical Dashboard
     ↓
Timeline + Documents + Appointments

---

📊 Dashboard Capabilities

Doctor Dashboard

Potential dashboard components:

- Patient search
- Patient overview
- Medical timeline
- Document list
- Medical trends
- Source references
- Appointment management
- AI history assistant

Lab Assistant Dashboard

- Create patient
- Patient ID generation
- Upload document
- Document type selection
- Upload status
- Processing status

Patient Dashboard

- Personal profile
- Medical timeline
- Medical documents
- Appointments
- Notifications
- AI history assistant

Admin Dashboard

- User management
- Doctor management
- Lab assistant management
- Account disabling
- Audit logs
- System settings

---

📈 Medical Data Visualization

Where appropriate, extracted numerical medical information can be visualized using charts.

For example:

Test Result Trend

Result
  │
  │       ●
  │   ●       ●
  │ ●           ●
  └──────────────────
      Date → 

Charts should be generated only from actual available records.

No values should be fabricated simply to populate a graph.

---

🔔 Notifications

The system architecture supports:

- In-app notifications
- Email
- SMS
- WhatsApp integration

For the hackathon prototype, notification behavior may be simulated where real external integrations are not configured.

Appointments should appear only when a doctor explicitly creates them.

---

🧠 Responsible AI Principles

MedVault AI is designed with a source-first approach.

1. No hallucinated patient data

AI must not create medical information that is absent from the source.

2. Source traceability

Important extracted information should reference its original document.

3. Missing information

Display:

Not available in source document

4. Uncertain information

Display:

Needs Verification

5. Medication conflicts

Display:

Conflicting medication information found.
Please verify with the doctor.

6. Human decision-making

The system is intended to support medical information retrieval and organization. It does not replace professional medical decision-making.

---

🚀 Getting Started

Prerequisites

Install:

- Node.js
- Python 3.x
- Git
- Tesseract OCR
- Supabase account
- Google Gemini API access

---

Clone the Repository

git clone https://github.com/YOUR_USERNAME/medvault-ai.git

cd medvault-ai

---

Frontend Setup

cd frontend

npm install

npm run dev

---

Backend Setup

cd backend

python -m venv venv

Windows

venv\Scripts\activate

Linux / macOS

source venv/bin/activate

Install dependencies:

pip install -r requirements.txt

Run the backend:

python app.py

---

🔑 Environment Variables

Create a ".env" file locally.

Example:

GEMINI_API_KEY=your_gemini_api_key
SUPABASE_URL=your_supabase_url
SUPABASE_ANON_KEY=your_supabase_anon_key

⚠️ Never commit ".env"

Add this to ".gitignore":

.env
.env.local
venv/
__pycache__/
node_modules/

Never upload API keys, passwords, Supabase service-role keys, or private credentials to GitHub.

---

🧪 Demo Data

The public repository should use synthetic/demo patient information only.

Example:

Patient ID: P1000
Name: Demo Patient
Hospital: Demo Hospital

Do not upload real patient medical records.

---

📸 Screenshots

Add your application screenshots here:

docs/screenshots/
├── landing-page.png
├── role-selection.png
├── doctor-dashboard.png
├── lab-dashboard.png
├── patient-dashboard.png
├── medical-timeline.png
└── ai-assistant.png

Example Markdown:

![MedVault AI Dashboard](docs/screenshots/doctor-dashboard.png)

---

🎥 Demo Flow

For a hackathon demonstration:

Landing Page
     ↓
Role Selection
     ↓
Lab Assistant Login
     ↓
Create Patient ID
     ↓
P1000 Generated
     ↓
Enter Patient Details
     ↓
Upload Medical Report
     ↓
Document Processing
     ↓
Information Extraction
     ↓
Timeline Generation
     ↓
Doctor Login
     ↓
Search P1000
     ↓
Review Patient Timeline
     ↓
Create Appointment
     ↓
Patient Login
     ↓
View Medical History
     ↓
Ask AI History Assistant

---

🌟 Future Enhancements

Potential future improvements include:

- Multilingual patient interface
- Advanced document classification
- Improved OCR for handwritten reports
- Medical event relationship visualization
- Advanced trend analysis
- Real-time notification integrations
- Stronger authentication
- Multi-hospital interoperability
- Enhanced audit and compliance capabilities
- More advanced source-evidence visualization

---

👨‍💻 Team

Team MedVault AI

Member| Role
Dahilia S| Team Member
Balaji J S| Team Member
Harishkumar S| Team Member
Dhanusya T| Team Member

---

🏫 Hackathon

24-Hour Healthcare Hackathon

Organized by:

KPR Institute of Engineering and Technology (KPRIET), Coimbatore

Achievement

🏆 Selected among the Top 50 teams out of 200+ participating teams

Problem Statement

HE-05 — Medical Document Intelligence & Patient Timeline

---

📜 Certificate

Our team received a participation certificate for the hackathon.

Add the certificate image to:

docs/
└── hackathon-certificate.png

Then display it in the README:

![Hackathon Certificate](docs/hackathon-certificate.png)

---

⚖️ Disclaimer

MedVault AI is a hackathon prototype and educational project.

It is designed to demonstrate medical document intelligence, information organization, timeline reconstruction, and source traceability.

It should not be used as a substitute for professional medical advice, diagnosis, or treatment.

All demonstration patient information should be synthetic and used only for development or presentation purposes.

---

📄 License

This project is intended for educational and hackathon purposes.

Add an appropriate open-source license if you decide to make the repository publicly reusable.

---

⭐ Support the Project

If you find MedVault AI interesting, consider giving the repository a ⭐ on GitHub!

MedVault AI — From Scattered Medical Reports to One Secure Patient Story.
