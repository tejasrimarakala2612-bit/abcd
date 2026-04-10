# 🎵 Mood-Based Music Recommendation System

## 📌 1. Business Problem

People often listen to music based on their mood, but finding the right playlist manually takes time. There is no simple system that understands user emotions and suggests music automatically.

---

## 💡 2. Possible Solution

Build an intelligent system that:

* Takes user mood as input (text)
* Uses AI to understand the mood
* Automatically recommends music playlists

---

## 🚀 3. Implemented Solution

This project is a full-stack application that connects frontend and backend:

* User enters mood in frontend UI
* Frontend sends request to n8n webhook
* AI model (Llama3 via Ollama) detects mood
* Spotify API fetches relevant playlists
* Results are displayed to the user

---

## 🛠️ 4. Tech Stack Used

| Component | Technology                |
| --------- | ------------------------- |
| Frontend  | HTML, CSS, JavaScript     |
| Backend   | n8n (Workflow Automation) |
| AI Model  | Ollama (Llama3)           |
| API       | Spotify Web API           |
| Testing   | Postman                   |

---

## 🏗️ 5. Architecture Diagram

```
User (Frontend UI)
        ↓
Fetch API Request
        ↓
n8n Webhook (Backend)
        ↓
AI Model (Ollama - Llama3)
        ↓
Spotify API
        ↓
Response (JSON)
        ↓
Frontend Display
```

---

## ⚙️ 6. How to Run Locally

### Step 1: Start n8n

```bash
n8n start --cors
```

### Step 2: Activate Workflow

* Open n8n UI
* Import workflow
* Click **Publish (Active)**

### Step 3: Start Ollama

```bash
ollama run llama3
```

### Step 4: Run Frontend

* Open `index.html` in browser

### Step 5: Test

* Enter: *"I feel happy today"*
* Click **Get Music**
* Playlist will be displayed

---

## 🔗 7. References & Resources

* n8n Docs: https://docs.n8n.io/
* Ollama: https://ollama.com/
* Spotify API: https://developer.spotify.com/
* MDN Web Docs

-

## 🧩 10. Formatting

* Clear headings and sections
* Proper alignment and readability
* Clean markdown structure

---
11. Screenshots
    <img width="1775" height="699" alt="image" src="https://github.com/user-attachments/assets/2cd991d8-162f-4ccc-8681-441e63e33465" />
    <img width="827" height="814" alt="image" src="https://github.com/user-attachments/assets/176b86fd-585a-4038-afd4-6a9fb3631a13" />
    <img width="1409" height="875" alt="image" src="https://github.com/user-attachments/assets/aa346255-c1ec-46ec-854f-169560a27ace" />
    <img width="1208" height="819" alt="image" src="https://github.com/user-attachments/assets/5a913d16-2c5a-4ef4-a954-1db8b126a0dd" />




    


## ⚠️ 12. Problems Faced & Solutions

### 🔴 Problem 1: Invalid JSON Error

**Issue:** JSON body error in n8n
**Solution:** Fixed syntax and expressions

---

### 🔴 Problem 2: Ollama Connection Error

**Issue:** `ECONNREFUSED 127.0.0.1:11434`
**Solution:** Started Ollama properly

---

### 🔴 Problem 3: Empty Webhook Response

**Issue:** No data returned
**Solution:** Configured "Respond to Webhook" node correctly

---

### 🔴 Problem 4: CORS Error

**Issue:** Frontend couldn't call backend
**Solution:** Used:

```bash
n8n start --cors
```

---

### 🔴 Problem 5: Mood Mapping Issue

**Issue:** Mood not updating correctly
**Solution:** Fixed prompt and response mapping

---

## 🎯 Conclusion

This project demonstrates how AI, APIs, and automation tools can be combined to build a real-world application that provides personalized music recommendations based on user mood.
