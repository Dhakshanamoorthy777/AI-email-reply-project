\# 🤖 AI Email Reply Generator



An AI-powered Gmail Chrome Extension that generates professional email replies using Google Gemini AI.



This project combines a Chrome Extension, React + Vite frontend, Spring Boot backend, and Gemini API to generate AI-powered email responses directly inside Gmail.



\## ✨ Features



\- 🤖 Generate AI-powered email replies

\- 📧 Generate replies directly inside Gmail

\- 🎨 Simple and user-friendly interface

\- 📝 Support for different email tones

\- ⚡ React + Vite frontend

\- ☕ Spring Boot REST API

\- 🧠 Google Gemini API integration

\- 🔗 WebClient for AI API communication

\- 🔐 API credentials managed using environment variables



\## 📸 Project Preview



\### AI Reply inside Gmail



!\[AI Reply](screenshots/ai-reply-gmail.png)



\## 🛠️ Technologies Used



\### Frontend



\- React.js

\- Vite

\- JavaScript

\- Axios

\- HTML

\- CSS



\### Backend



\- Java 17

\- Spring Boot 3.5.4

\- Spring Web

\- Spring WebFlux

\- WebClient

\- Maven



\### AI



\- Google Gemini API



\### Browser Extension



\- Chrome Extension



\## 🏗️ Architecture



```text

Gmail

&#x20;  ↓

Chrome Extension

&#x20;  ↓

React + Vite

&#x20;  ↓

Axios

&#x20;  ↓

Spring Boot REST Controller

&#x20;  ↓

EmailGeneratorService

&#x20;  ↓

WebClient

&#x20;  ↓

Google Gemini API

&#x20;  ↓

AI Generated Reply

&#x20;  ↓

Gmail

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

│   ├── public/

│   ├── package.json

│   └── vite.config.js

│

├── writer-sb/

│   ├── src/

│   ├── pom.xml

│   └── mvnw

│

├── screenshots/

│   └── ai-reply-gmail.png

│

├── .env.example

├── .gitignore

└── README.md

🔌 Backend API

Generate Email Reply

POST /api/email/generate



Example request:



{

&#x20; "emailContent": "Can you please send me the project report by tomorrow?",

&#x20; "tone": "professional"

}



The backend sends the email content to the Gemini API and returns the generated reply.



🔐 Environment Variables



The Gemini API credentials are not stored directly in the source code.



The backend uses:



gemini.api.url=${GEMINI\_URL}

gemini.api.key=${GEMINI\_KEY}



Create environment variables for:



GEMINI\_URL=your\_gemini\_api\_url

GEMINI\_KEY=your\_gemini\_api\_key



Never commit your actual Gemini API key to GitHub.



🚀 Running the Backend



Navigate to the backend:



cd writer-sb



Run the Spring Boot application:



.\\mvnw.cmd spring-boot:run



The backend runs locally on:



http://localhost:8080

⚛️ Running the React Application



Navigate to:



cd Email-Writer-React



Install dependencies:



npm install



Start the development server:



npm run dev

🔄 Application Flow

1\. User opens an email in Gmail

&#x20;            ↓

2\. User clicks "AI Reply"

&#x20;            ↓

3\. Chrome Extension captures the email content

&#x20;            ↓

4\. Request is sent to the Spring Boot backend

&#x20;            ↓

5\. Spring Boot creates the AI prompt

&#x20;            ↓

6\. WebClient sends the request to Gemini

&#x20;            ↓

7\. Gemini generates the email reply

&#x20;            ↓

8\. Backend returns the generated reply

&#x20;            ↓

9\. AI reply is displayed in Gmail

🚀 Future Improvements

Add more AI response tones

Add response length controls

Improve reply personalization

Deploy the backend to cloud hosting

Publish the Chrome Extension to the Chrome Web Store

Add authentication and user-specific settings

👨‍💻 Author



Dhakshana Moorthy



Java Full Stack Developer | Spring Boot | React | AI Applications

