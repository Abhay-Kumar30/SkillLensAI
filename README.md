# SkillLensAI Full Stack (Spring Boot + React)         
[![Live App](https://img.shields.io/badge/Live-App-brightgreen)](https://resume-analyser-kp0f.onrender.com/)

## Description

• Designed and developed a scalable full-stack web application for AI-based resume analysis and evaluation
• Built RESTful APIs using Spring Boot to handle resume uploads, user management, and analysis workflows
• Integrated Google Gemini AI to extract skills, analyze resume content, and generate intelligent improvement suggestions
• Implemented JWT-based authentication, email verification, and secure password reset flows using Brevo
• Developed responsive and reusable React components for seamless user interaction and real-time insights
• Used MySQL to manage user profiles, resume data, and analysis results with efficient relational mapping
• Followed clean layered architecture and best practices to ensure maintainability and scalability
• Tested APIs using Postman and managed version control using Git & GitHub
• Collaborated using Agile development practices, focusing on clean, testable, and efficient code

## Tech Stack
Frontend: React.js | HTML5 | CSS3 | JavaScript (ES6+)
Backend: Java | Spring Boot | RESTful APIs | JWT Authentication
Database: MySQL (Relational Database)
AI Integration: Google Gemini AI
Security & Auth: JWT | Email Verification | Password Reset (Brevo)
Tools & Practices: Git | GitHub | Postman | Agile Development
Architecture: Layered Architecture (Controller, Service, Repository)

## Frontend & Backend Integration Notes

- The frontend UI is developed using **React**
- For deployment, the React application is **built and served by the Spring Boot backend** as static files
- The React production build files are placed inside the backend’s **static** directory

### Static & Template Files
- The `static` folder contains the **React production build files**
- The `templates` folder inside `static` is used to store **email templates**
  - Used for **email verification** and **password reset**

## How to Run the Project Locally

#### 1. Clone the Repository
```bash
git clone https://github.com/Mohamed-Imran-12/Resume-Analyser.git
```

#### 2. Open Project in IDE
Open the project in **IntelliJ IDEA / Eclipse**

Open `pom.xml` and allow Maven to download dependencies

#### 3. Configure Credentials (`application.properties`)

###### Database (ONLY MySQL)
```properties
spring.datasource.url=your_DB_URL
spring.datasource.username=your_DB_USERNAME
spring.datasource.password=your_DB_PASSWORD
```

###### Google Cloud Platform (Google Sign-In)
```properties
spring.security.oauth2.client.registration.google.client-id=your_GCP_ID
spring.security.oauth2.client.registration.google.client-secret=your_GCP_SECRET
```

###### Google Gemini AI (Resume Analysis)
```properties
genKey=your_GEMINI_API_KEY
```

###### Mail Service (ONLY Brevo)
```properties
apiKey=your_BREVO_MAIL_API
```

#### 4. Run Backend
Run `ResumeAnalyserApplication.java`

#### 5. Open in Browser
```
http://localhost:8080/
```



## Important Notes (Must Read)

- Only **Gemini AI** is configured in this project.  
To use another AI provider, update AI-related code in `appservice.java`.

- Email functionality works **only with Brevo API**.  
To use another mail provider, update mail-related code in `mailservice.java`.

- AI models evolve quickly.  
If the configured Gemini model is removed or replaced, update the model in `appservice.java`.



## Modifying the Frontend UI

Do **not** edit files inside the backend `static` folder directly.

### 1. Run Frontend Separately (Development Mode)
```bash
cd "frontend src"
npm install
npm run dev
```

This starts the React development server for UI changes.



### 2. Build Frontend for Backend Deployment
```bash
cd "frontend src"
npm run build
```

#### Backend Static Structure
```text
static/
├── assets/
│   ├── *.css
│   ├── *.js
├── index.html
```

Steps:
- Delete old `index.html` and files inside `assets`
- Copy new build files from `dist`
- Paste them into backend `static` directory

Thank you.
