# 💼 SkillMatch AI: Intelligent Job Matching Platform

**SkillMatch AI** is an AI-powered application I developed to help job seekers find the most relevant job opportunities based on their skills, experience, and career preferences.  
It processes resumes, matches them with job descriptions, and provides personalized improvement insights.  

---

## 🚀 Features

- **Intelligent Job Matching**: Compares resumes with job listings and suggests the closest matches.  
- **Resume Parsing**: Extracts skills, education, and professional experience.  
- **Keyword Booster**: Highlights missing keywords and suggests improvements.  
- **Real-Time Suggestions**: Provides tips to refine resume content and structure.  
- **Automated Job Recommendations**: Recommends job listings aligned with the user profile.  
- **Multi-Language Resume Support**: Detects and translates resumes for better analysis.  
- **Employer Dashboard**: Allows recruiters to post jobs and view matched candidates.  

---

## 🛠️ Tech Stack

- **Java 11+**: Backend logic  
- **Spring Boot**: API services and infrastructure  
- **Apache POI**: For `.docx` file parsing  
- **PdfBox**: For `.pdf` file parsing  
- **OpenNLP**: Natural Language Processing  
- **DetectLanguage API**: Language identification  
- **Google Cloud Translate**: Resume translation  

---

## 📦 Installation

### Prerequisites
- Java 11+  
- Maven  

### Steps

1. **Clone the repository**  
```bash
git clone https://github.com/your-username/skillmatch-ai.git
```

2. **Navigate to project folder**  
```bash
cd skillmatch-ai
```

3. **Install dependencies**  
```bash
mvn install
```

4. **Build the project**  
```bash
mvn clean package
```

5. **Run the application**  
```bash
java -jar target/skillmatch-ai-0.1.0-SNAPSHOT.jar
```

---

## 🧑‍💻 Usage

### Start the Application
```bash
mvn spring-boot:run
```
App runs at `http://localhost:8081`.  

### Prepare Files
- Save your resume as `resume.txt`  
- Save job description as `job.txt`  
- Sample files included:  
  - `demo_resume.txt`  
  - `demo_job.txt`  

### Example API Request (via cURL)
```bash
curl -X POST http://localhost:8081/api/match   -F "resume=@demo_resume.txt"   -F "jobDescription=@demo_job.txt"
```

### Example JSON Response
```json
{
  "fitScore": 87.2,
  "competencies": ["Java", "Spring Boot", "REST APIs"],
  "missingKeywords": ["Docker", "AWS"],
  "improvements": [
    "Add cloud deployment experience",
    "Include more leadership/project management details"
  ]
}
```

---

## 🌐 API Endpoints

### `POST /api/match`
- **Purpose**: Compares resume with job description and returns fit score  
- **Parameters**:  
  - `resume`: Resume file  
  - `jobDescription`: Job description file  

### `GET /api/jobs/recommendations`
- **Purpose**: Provides job recommendations based on fit score  
- **Parameters**:  
  - `fitScore`: Score threshold  

---

## 📄 License
Licensed under **Apache 2.0 License**. See `LICENSE` file for details.  

---

### 🚀 Start Using SkillMatch AI to Land Your Next Role!
