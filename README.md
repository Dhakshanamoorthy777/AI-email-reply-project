# AI Email Reply Generator

An AI-powered Gmail Chrome Extension that generates professional email replies using the Gemini API. The project combines a Chrome Extension, React frontend, and Spring Boot backend to provide AI-assisted email reply generation directly inside Gmail.

## 🚀 Features

- Generate professional email replies using AI
- Works directly inside Gmail
- One-click **AI Reply** button in the Gmail reply window
- Supports professional email tone
- React-based frontend
- Spring Boot REST API backend
- Gemini API integration
- Secure API key handling using environment variables
- Responsive and user-friendly interface
- Deployed Spring Boot backend
- Chrome Extension integration

## 🏗️ Project Architecture

```text
Gmail
   ↓
Chrome Extension
   ↓
Spring Boot REST API
   ↓
Gemini API
   ↓
AI Generated Email Reply
   ↓
Gmail Reply Box
🛠️ Technologies Used
Frontend
React.js
Vite
JavaScript
HTML
CSS
Axios
Backend
Java
Spring Boot
Spring WebFlux
WebClient
Maven
REST API
AI
Google Gemini API
Browser Extension
Chrome Extension
Manifest V3
Content Scripts
Tools & Deployment
Git
GitHub
Postman
Render
Docker
VS Code
📂 Project Structure
AI-email-reply-project/
│
├── Email-Writer-Extension/
│   ├── content.js
│   ├── content.css
│   └── manifest.json
│
├── Email-Writer-React/
│   ├── src/
│   │   ├── App.jsx
│   │   ├── App.css
│   │   └── main.jsx
│   ├── public/
│   ├── package.json
│   └── vite.config.js
│
├── writer-sb/
│   ├── src/
│   │   └── main/
│   │       ├── java/
│   │       └── resources/
│   ├── Dockerfile
│   ├── pom.xml
│   └── mvnw
│
├── screenshots/
│
└── README.md
⚙️ How It Works
Open Gmail in Google Chrome.
Open an email and click Reply.
The Chrome Extension adds an AI Reply button to the Gmail compose toolbar.
Click AI Reply.
The extension extracts the email content.
The content is sent to the Spring Boot REST API.
The backend creates an AI prompt.
The backend sends the request to the Gemini API.
Gemini generates a professional reply.
The generated response is returned to the Chrome Extension.
The reply is automatically inserted into the Gmail compose box.
🔌 API Endpoint

The backend provides the following endpoint:

POST /api/email/generate
Request
{
  "emailContent": "Original email content",
  "tone": "professional"
}
Response

The API returns the generated email reply as a text response.

🔐 Environment Variables

The Gemini API credentials are not stored in the source code or GitHub repository.

The Spring Boot backend uses environment variables:

GEMINI_URL=your_gemini_api_url
GEMINI_KEY=your_gemini_api_key

The application reads them using:

gemini.api.url=${GEMINI_URL}
gemini.api.key=${GEMINI_KEY}

This keeps the Gemini API key outside the public source code.

💻 Local Setup
1. Clone the Repository
git clone https://github.com/Dhakshanamoorthy777/AI-email-reply-project.git
cd AI-email-reply-project
2. Run the Spring Boot Backend
cd writer-sb

Set the required environment variables:

GEMINI_URL
GEMINI_KEY

Then run:

./mvnw spring-boot:run

On Windows:

.\mvnw.cmd spring-boot:run

The backend runs locally on:

http://localhost:8080
3. Run the React Application

Open another terminal:

cd Email-Writer-React

Install dependencies:

npm install

Start the development server:

npm run dev

To create a production build:

npm run build
4. Load the Chrome Extension
Open Google Chrome.
Go to:
chrome://extensions
Enable Developer mode.
Click Load unpacked.
Select:
Email-Writer-Extension
Open Gmail.
Open an email.
Click Reply.
Click AI Reply.
☁️ Deployment

The Spring Boot backend is deployed using Render with Docker.

Backend deployment flow:

GitHub
   ↓
Render
   ↓
Docker
   ↓
Spring Boot
   ↓
Gemini API
Backend

Live backend:

https://ai-email-reply-project.onrender.com

API endpoint:

https://ai-email-reply-project.onrender.com/api/email/generate

The Gemini API key is configured securely through Render environment variables.

📸 Screenshots
React Application

Gmail AI Reply

Generated Email

Note: Update the screenshot filenames above if your actual screenshot filenames are different.

🔒 Security
Gemini API key is not committed to GitHub.
API credentials are stored using environment variables.
The Chrome Extension communicates with the deployed backend instead of exposing the Gemini API key.
.gitignore is used to prevent sensitive/local files from being committed.
🚧 Future Improvements
Add multiple email tones such as friendly, formal, casual, and concise
Add customizable reply length
Add multilingual email generation
Improve Gmail UI integration
Add user authentication
Add email context awareness
Publish the extension to the Chrome Web Store
Add automated testing
Improve error handling and loading states
👨‍💻 Author

Dhakshana Moorthy B

Java Full Stack Developer

GitHub: https://github.com/Dhakshanamoorthy777
LinkedIn: Add your LinkedIn profile URL