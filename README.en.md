<div align="center">

🤖 AI Lead Qualification Assistant

A smart tool to optimize the Omie/OneFlow sales process, automating lead qualification and prospecting with the power of Google Gemini.

</div>

<p align="center">
<img alt="Status" src="https://www.google.com/search?q=https://img.shields.io/badge/status-completed-brightgreen%3Fstyle%3Dfor-the-badge">
<img alt="Technology" src="https://img.shields.io/badge/Google_Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white">
<img alt="Backend" src="https://img.shields.io/badge/Google_Cloud-4285F4?style=for-the-badge&logo=google-cloud&logoColor=white">
<img alt="Frontend" src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white">
<img alt="License" src="https://www.google.com/search?q=https://img.shields.io/badge/license-MIT-yellow%3Fstyle%3Dfor-the-badge">
</p>

<p align="center">
<a href="#-objective">Objective</a> •
<a href="#-features">Features</a> •
<a href="#-architecture-and-security">Architecture</a> •
<a href="#-technologies-used">Technologies</a> •
<a href="#-challenges-and-learnings">Learnings</a> •
<a href="#-author">Author</a>
</p>

<div align="center">
<a href="https://matheusterr.github.io/AI-Assistant/" target="_blank">
<img alt="Access Live Demo" src="https://www.google.com/search?q=https://img.shields.io/badge/Access_Live_Demo-34D399%3Fstyle%3Dfor-the-badge%26logo%3Drocket%26logoColor%3Dwhite">
</a>
</div>

<div align="center">
<a href="https://matheusterr.github.io/AI-Assistant/" target="_blank">
<img src="https://ik.imagekit.io/6iz6c073z/imagem_2025-06-17_023035247.png?updatedAt=1750138376033" alt="AI Assistant Interface" width="90%"/>
</a>
</div>

🎯 Objective

The B2B market is highly competitive. Sales professionals' time (SDRs and Sales Reps) is a precious resource, often spent on repetitive qualification tasks and crafting initial approaches.

This project directly addresses this pain point by proposing an automation solution that frees up the sales team's time to focus on high-value activities, such as negotiation and closing deals. It leverages AI to bring intelligence and scale to the top of the sales funnel.

✨ Features

✅ Smart Qualification: Analyzes input data to generate a Fit Score (High, Medium, Low), allowing for instant prioritization.

✉️ Relevant Message Generation: Creates personalized prospecting emails, connecting the lead's challenges with the company's solutions.

🤔 Strategic Question Suggestions: Provides open-ended follow-up questions to deepen the conversation and uncover client pain points.

📈 Response Analysis: Interprets the sentiment of a reply email and suggests the most appropriate next steps.

🔐 Secure Access Control: An access code authentication system that protects API resource consumption.

🏛️ Architecture and Security

Security was a fundamental pillar of development. The API key is never exposed on the frontend. To achieve this, an intermediate backend architecture (proxy) was implemented using Google Cloud Functions.

graph TD;
    A[👨‍💻 User on Frontend] -- "1. Sends prompt + Access Code" --> B[🛡️ Google Cloud Function];
    B -- "2. Validates Access Code" --> C{Valid Code?};
    C -- "No" --> D["Returns 401 Error"];
    D --> A;
    C -- "Yes" --> E["3. Uses API Key to call"];
    E --> F[🤖 Google Gemini API];
    F --> E;
    E --> A;

    style B fill:#e3f2fd,stroke:#4285F4,stroke-width:2px;
    style F fill:#dcedc8,stroke:#689f38,stroke-width:2px;


This approach ensures Security by Design, access control, and a scalable, low-cost serverless infrastructure.

🛠️ Technologies Used

Category

Technology / Tool

Frontend

HTML5, JavaScript (ES6)

Styling

Tailwind CSS

Artificial Intelligence

Google Gemini API

Backend

Google Cloud Functions (Node.js)

Hosting & Deploy

GitHub Pages & gcloud CLI

🧠 Challenges and Learnings

API Key Security: The main challenge was designing an architecture that did not expose the API key on the client side. The solution using a Cloud Function acting as a proxy was a crucial learning experience in web application security.

Infrastructure Debugging: Dealing with environment variable configuration in Google Cloud and debugging CORS and authorization errors (401 Unauthorized) provided valuable hands-on experience in DevOps and cloud infrastructure.

Async Handling: Reinforced knowledge in async/await and handling Promises to manage API requests and interface updates in a non-blocking manner.

🚀 How to Use

Access the Live Demo.

Fill in the information of the lead you want to analyze.

Enter the Access Code to enable AI features.

Use the buttons to qualify, generate messages, and get insights.

✍️ Author

<p>
Made with ❤️ by Matheus Terr.
</p>

<p>
<a href="https://linkedin.com/in/matheus-terr" target="_blank">
<img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white">
</a>
<a href="https://github.com/MatheusTerr" target="_blank">
<img alt="GitHub" src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white">
</a>
</p>
