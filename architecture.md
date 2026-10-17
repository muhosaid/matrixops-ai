# Project Architecture: MatrixOps AI

## 1. System Topology
MatrixOps AI uses a serverless cloud-native architecture optimized for zero cost, high scalability, and fast execution during the hackathon sprint.

[ User Browser / UI ]
│ (HTTPS POST)
▼
[ Firebase Hosting (Frontend - Next.js/React) ]
│ (REST API Call)
▼
[ Google Cloud Run (Backend - FastAPI / Python) ]
├──► [ Google Gemini API (gemini-1.5-flash) ]
└──► [ Cloud Firestore (Incident Database Persistence) ]

## 2. Component Breakdown
- **Frontend Layer:** Built with React/Next.js and Tailwind CSS, hosted globally on Firebase Hosting.
- **Backend Service:** Containerized Python FastAPI application packaged via Docker and deployed serverlessly on Google Cloud Run.
- **Intelligence Layer:** Google GenAI SDK communicating with `gemini-1.5-flash` using Pydantic models to guarantee strict JSON output structures.
- **Data Persistence:** Cloud Firestore NoSQL database storing timestamped incident traces.