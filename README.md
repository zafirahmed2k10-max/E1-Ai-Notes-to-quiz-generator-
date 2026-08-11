# E1-Ai-Notes-to-quiz-generator-
AI-powered Notes-to-Quiz Generator that converts study notes into structured multiple-choice quizzes using Python, OpenAI Agents SDK, Gemini, FastAPI, and Pydantic.
E1 — Notes-to-Quiz Generator 🎓🤖

AI-Powered Educational Quiz Generator

An AI-powered educational service that converts study notes into structured multiple-choice quizzes using Python, OpenAI Agents SDK, Gemini 2.5 Flash, FastAPI, and Pydantic.

Background

Teachers and students often need to create practice questions from textbooks, lecture notes, and study material. Creating quizzes manually can be time-consuming and repetitive.

AI can generate questions quickly, but normal AI responses may be unstructured and difficult for an application to process. This project solves that problem by generating a properly structured quiz with questions, options, correct answers, explanations, and Bloom's Taxonomy levels.

Purpose of the Project

The main purpose of this project is to make quiz creation faster and easier for students and teachers.

The project converts educational notes into a ready-to-use practice quiz. It also demonstrates how an AI agent can work as a real software service rather than just a chatbot.

Main Goals

Automatically generate quizzes from notes.

Save time for teachers and students.

Generate questions at different difficulty levels.

Provide four options for every question.

Identify the correct answer.

Explain why the answer is correct.

Classify questions using Bloom's Taxonomy.

Return reliable, structured data that other applications can use.


How the Project Works

Study Notes → AI Agent → Quiz Generation → Structured Output → Gradeable Quiz

The user provides notes, chooses the number of questions and difficulty, and the AI agent generates a structured quiz.

Main Features

📝 Notes-to-quiz generation

❓ Multiple-choice questions

🔢 User-selected question count

🎯 Easy, Medium, and Hard difficulty

4 options for every question

✅ Correct answer identification

💡 Answer explanations

🧠 Bloom's Taxonomy levels:

Recall

Apply

Analyse


📊 Quiz grading

🔒 Input validation

📦 Structured Pydantic output

🚀 FastAPI service

📖 Interactive API documentation


Example Input

{
  "notes": "Photosynthesis is the process by which green plants use sunlight to make food.",
  "count": 5,
  "difficulty": "medium"
}

Example Output

{
  "questions": [
    {
      "question": "What is photosynthesis?",
      "options": [
        "A process of respiration",
        "A process plants use to make food",
        "A process of digestion",
        "A process of reproduction"
      ],
      "correct_answer": 1,
      "explanation": "Plants use photosynthesis to make food using light energy.",
      "bloom_level": "recall"
    }
  ]
}

Technology Used

Python — Main programming language

OpenAI Agents SDK — AI agent framework

Gemini 2.5 Flash — AI model

FastAPI — Backend API

Pydantic — Structured data and validation

python-dotenv — Environment variable management

Uvicorn — Server


Agents SDK Concepts

This project focuses mainly on Agent, Runner, and Structured Output.

The most important concept is structured output. Instead of receiving unpredictable text from the AI, the application receives a properly defined Pydantic object containing the quiz data.

API Endpoints

Generate Quiz

POST /quiz/generate

Generates a quiz from the provided notes.

Get Quiz

GET /quiz/{id}

Retrieves a generated quiz.

Grade Quiz

POST /quiz/{id}/grade

Checks submitted answers and calculates the score.

Health Check

GET /health

Checks whether the service is running.

Project Structure

notes-to-quiz-generator/
│
├── agent_core.py
├── main.py
├── models.py
├── test_agent.py
├── requirements.txt
├── .gitignore
└── README.md

Why This Project Is Useful

This project can help:

Students prepare for exams.

Teachers create revision material.

Tutors create practice exercises.

Educational applications generate quizzes automatically.


It also provides a practical example of how AI can be integrated into a real backend service.

Future Improvements

Student and teacher accounts

Quiz history

Database storage

PDF quiz export

Web interface

Authentication

More question types

More Bloom's Taxonomy levels

Student performance analytics

Cloud deployment


Project Status

🚧 In Development

Authors

Zafir Ahmed & Masir Ahmed Khan

Project: E1 — Notes-to-Quiz Generator

Category: AI Agent / Education
