🤖 The R.O.A.S.T. Agent: Rote Observation and Accelerated STEM Tutoring

😈 Your Smartest (and Meanest) STEM Tutor

The R.O.A.S.T. Agent is a sophisticated, LangChain/LangGraph-powered AI that delivers critical, entertaining, and context-aware tutoring in STEM subjects. Unlike standard LLM chatbots, it moves far beyond static, dated training data by drawing precise, up-to-date facts from a robust, dynamic knowledge base of specialized guides. This ensures that the agent's corrections and challenges are always based on the latest industry standards and factual knowledge.

Forget gentle encouragement. R.O.A.S.T. makes you smarter by mercilessly challenging your assumptions and demanding evidence for your claims. This unique, high-pressure persona is designed to solidify learning and improve critical thinking skills through direct, memorable feedback.

✨ Key Features

Context-Aware Critique via RAG: The agent utilizes Retrieval-Augmented Generation (RAG) to instantly critique user errors.  Instead of relying solely on its internal memory, it queries dedicated Supabase vector stores (e.g., best_practice, troubleshooting_guide) to retrieve precise, factual snippets. This immediate grounding in expert documentation ensures corrections are highly relevant, specific, and actionable.

Persistent Learning (Long-Term Memory): LangGraph's state machine enables continuous, multi-session learning. By leveraging its persistent checkpointer, the agent actively remembers conversation history, previous mistakes, and successful concepts across all sessions tied to a unique thread_id. This allows the agent to build on past interactions and tailor its intensity and subject matter depth over time.

Tool-Augmented Reasoning (Real-Time Actions): The agent's intelligence is augmented by custom tools. The powerful jsEcecutor enables real-time data fetching by generating and executing external code. This means the agent can confidently answer live, dynamic questions that require current information, such as checking the latest Bitcoin price, performing complex currency conversions, or fetching current market data.

Dynamic Knowledge Base Expansion: The agent's subject expertise is designed for easy scaling. New, specialized documentation is seamlessly integrated by processing and embedding new .txt files directly into dedicated Supabase vector tables. This modular approach allows users to rapidly expand the R.O.A.S.T. agent's knowledge without retraining the core language model.

🛠️ Architecture and Stack

The R.O.A.S.T. Agent operates on a robust, decoupled architecture designed for stability and security:

Framework: Utilizes the advanced chaining capabilities of LangChain and the state machine management provided by LangGraph for complex conversational flows and decision-making.

LLM: Powered by the speed and effectiveness of the Gemini model (via @langchain/google-genai), ensuring high-quality reasoning and fast response times.

Vector Database: Uses Supabase (Postgres with the pgvector extension) as the secure and scalable backend for storing high-dimensional vector embeddings, which is the backbone of the agent's precise RAG capabilities.

Execution Environment: A decoupled Node.js Express server cluster manages the agent's operation. This includes the Agent Server (running the LangGraph logic) and a separate, sandboxed Executor Server. This separation ensures secure, isolated execution of user-requested JavaScript code, protecting the core application integrity.

🚀 Deployment & Run

To launch the complete R.O.A.S.T. Agent application, including both its backend intelligence and the user interface, two separate processes must be initiated:

Start the Agent and Executor Servers (Backend):

node index.js


(This command typically initiates the primary Agent server (e.g., on port 3001) alongside any required Executor servers (e.g., on port 3000) that handle external API calls and code execution.)

Start the Client (Frontend):

npm run dev


(This command starts the development server for the user interface, making the application accessible in a web browser, usually listening on a port like 5173 or 3000, depending on your development environment setup.)
