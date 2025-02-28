# Resume Matcher - Job Description Based Resume Ranking

## 📂 Project Structure
```
/resume_matcher_app
│── app.py                # Flask API for resume ranking
│── templates/
│   └── index.html        # Frontend UI for file upload and results
│── uploads/              # Directory for storing uploaded resumes
│── requirements.txt      # Python dependencies
└── README.md             # Project Documentation
```

## 📦 Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/resume_matcher_app.git
cd resume_matcher_app
```

### 2️⃣ Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows use `venv\Scripts\activate`
```

### 3️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```

### 4️⃣ Run the Flask App
```bash
python app.py
```
Now, open [http://127.0.0.1:5000/](http://127.0.0.1:5000/) in your browser.

---

## 🏗 How It Works
1. **Upload multiple resumes** (PDF, DOCX, TXT supported) and enter a job description.
2. **Text Extraction**: Extracts text from resumes.
3. **Vectorization**: Converts text data into numerical representations using **TF-IDF Vectorizer**.
4. **Similarity Calculation**: Computes cosine similarity scores between the job description and each resume.
5. **Ranking**: Displays the top 5 resumes based on their similarity scores.

---

## 📂 Supported File Formats
- **PDF** (`.pdf`)
- **Word Documents** (`.docx`)
- **Text Files** (`.txt`)

---

## 📝 Output
- Displays the **top 5 matching resumes** along with their similarity scores.
- If no resumes or job descriptions are provided, an appropriate message is shown.

---

## 🚀 Deployment
### 1️⃣ Docker Deployment
```bash
docker build -t resume-matcher-app .
docker run -d -p 5000:5000 resume-matcher-app
```

### 2️⃣ Deploy on AWS EC2
```bash
sudo apt update && sudo apt install -y docker.io
scp -i your-key.pem -r resume_matcher_app ubuntu@your-ec2-ip:~/
docker run -d -p 80:5000 resume-matcher-app
```
Access the app at [http://your-ec2-ip/](http://your-ec2-ip/).

---



**Happy Coding! 🚀**

