# Coding Rules & Guidelines: MatrixOps AI

## 1. General Principles
- Keep code modular, clean, and thoroughly commented.
- Strictly adhere to zero-cost architectural limits (Always Free tiers).
- Never hardcode API keys; always utilize environment variables (`GEMINI_API_KEY`).

## 2. Backend (Python / FastAPI)
- Use asynchronous route handlers (`async def`) for optimal performance.
- Validate all incoming payloads using Pydantic data models.
- Handle exceptions gracefully with appropriate HTTP status codes (e.g., 500 for internal errors).
- Follow PEP 8 style conventions for Python code formatting.

## 3. Frontend (React / Tailwind CSS)
- Maintain a responsive mobile-first or desktop-first dark theme (`slate-950` palette).
- Use Lucide React icons for clean visual indicators.
- Implement clear loading spinners and error handling states during asynchronous fetch operations.