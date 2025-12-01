🤖 The R.O.A.S.T. Agent: Rote Observation and Accelerated STEM Tutoring

😈 Your Smartest (and Meanest) STEM Tutor

The R.O.A.S.T. Agent is a LangChain/LangGraph-powered AI that provides real-time, context-aware tutoring in STEM subjects (Science, Technology, Engineering, and Math)—all while maintaining a highly critical and entertaining persona.

It leverages a dynamic knowledge base, allowing it to move beyond general LLM training data and draw precise, up-to-date facts from specialized guides (Best Practices, Troubleshooting, Programming, Web Technologies).

Forget gentle encouragement. R.O.A.S.T. makes you smarter by mercilessly challenging your assumptions.

✨ Key Features

Context-Aware Critique: Uses LangChain's Retrieval-Augmented Generation (RAG) capabilities to retrieve relevant information from custom vector stores (Supabase tables like best_practice, common_commands, etc.) and instantly critique user errors or poor explanations.

Persistent Learning Threads: Built on LangGraph's state machine, the agent remembers conversation history and previous mistakes across sessions, allowing for deep, continuous learning loops.

Tool-Augmented Reasoning: Equipped with custom tools (jsEcecutor for real-time data fetching, weatherTool for external context), enabling it to answer live questions (e.g., current Bitcoin price, live currency conversions).

Dynamic Knowledge Base: Easily expand the agent's expertise by uploading new .txt files to be processed and embedded into dedicated Supabase vector tables.

🛠️ Architecture and Stack

Framework: LangChain, LangGraph (for conversational state management and reasoning flow).

LLM: Gemini (via @langchain/google-genai).

Vector Database: Supabase (Postgres with pgvector extension).

Execution Environment: Node.js Express server cluster (Agent Server + Executor Server) for secure, decoupled code execution.
