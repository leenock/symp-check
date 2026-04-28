# 🩺 Symptom Checker AI – Project Instructions

## 🎯 Project Goal
Build a symptom checker system that allows users (parents/guardians) to input symptoms and receive safe, non-diagnostic health guidance using AI.

The system must prioritize:
- Simplicity
- Safety
- Accuracy (within scope)
- Scalability

---

## ⚠️ Core Rule (VERY IMPORTANT)

This system MUST NOT:
- Provide medical diagnosis
- Claim certainty about diseases
- Replace professional medical advice

All outputs MUST include:
> "This information is for informational purposes only and does not replace professional medical advice."

---

## 🧱 System Architecture (High-Level)

Flow:
User Input → Symptom Processing → Follow-up Questions → Retrieval → AI Response → Risk Classification → Output

---

## 📋 Functional Modules

### 1. User Management
- Create account (email or phone)
- Create child profile:
  - Age
  - Weight
  - Known conditions

---

### 2. Symptom Input
- Accept natural language input
- Example:
  - "My child has fever and cough"
- Extract key symptoms

---

### 3. Follow-Up Engine
- Generate simple follow-up questions based on symptoms

Examples:
- Fever → "What is the temperature?"
- Cough → "How long has the cough lasted?"

---

### 4. Symptom Processing
- Match user input against dataset (corpus)
- Use embedding + similarity search

---

### 5. Health Guidance Generation
Output must include:
- Possible explanations (NOT diagnosis)
- Basic care advice
- Next steps

---

### 6. Risk Classification

Define 3 levels:

- LOW:
  - Mild symptoms
  - Show home care advice

- MEDIUM:
  - Monitor condition
  - Suggest doctor visit

- HIGH:
  - Urgent
  - Recommend immediate medical attention

---

### 7. Alerts System
- Trigger alerts for high-risk symptoms
- Show strong recommendation to seek care

---

### 8. History Tracking
Store:
- Symptoms
- Responses
- Guidance

Allow:
- Viewing past sessions

---

### 9. Subscription Model

Free:
- Basic symptom checking

Premium:
- Advanced insights
- Growth tracking
- More detailed recommendations

---

### 10. Language Support
- Support multiple languages (future)
- Default: English

---

### 11. Data Sync
- Store locally when offline
- Sync when online

---

### 12. Disclaimer
Always display:
- Informational use only
- Not medical advice

User must acknowledge before using system

---

## 🧰 Tech Stack

- Python
- Streamlit (UI)
- FAISS (vector search)
- SentenceTransformers (embeddings)
- OpenAI API (response generation)

---

## 📂 Project Structure

app/
- core/
- services/
- data/
- ui/
- utils/

---

## 🧠 Development Rules

- Start simple (MVP first)
- Avoid over-engineering
- Keep logic modular
- Separate:
  - UI
  - Logic
  - Data

---

## 🧪 MVP Scope (Phase 1)

Must include:
- Symptom input
- Basic dataset matching
- Simple response
- Risk level

NOT required yet:
- Accounts
- Payments
- Notifications
- Multilingual

---

## 🚫 What to Avoid

- Complex AI pipelines initially
- Medical claims
- Large datasets early on
- Overcomplicated UI

---

## ✅ Success Criteria

System is successful if:
- User can input symptoms
- System responds clearly
- Risk level is shown
- Output is safe and understandable

---

## 🚀 Future Enhancements

- Voice input
- Multilingual support
- Doctor consultation
- WhatsApp integration
- Better datasets
- Personalization

---