__Multi-Agent Customer Support System (Langflow + Agentic AI)__
A multi-agent AI system built with Langflow and OpenAI, designed to handle end-to-end customer support tasks across multiple domains.

This project extends Customer Support Agent into a multi-agent architecture, where specialized AI agents collaborate -  from FAQ retrieval to order 

management - to deliver accurate, context-aware, and automated customer service.

__Overview__

The system leverages Langflow’s flow-based orchestration to coordinate multiple autonomous agents, each specializing in a different area of support. It combines Retrieval-

Augmented Generation (RAG), Azure AI Search, and agent-to-agent reasoning to provide seamless conversational experiences.

Each agent performs distinct subtasks (retrieval, lookup, summarization, decision-making) and communicates with others through Langflow’s node connections -  forming an agentic 

support ecosystem.

__Architecture__

| Agent                    | Role                | Description                                                    |
| ------------------------ | ------------------- | -------------------------------------------------------------- |
| **FAQ Agent**            | Knowledge retrieval | Answers company FAQs using vector search + OpenAI completions. |
| **Manager Agent**        | Coordinator         | Routes complex requests to specialized agents (product/order). |
| **Order Lookup Agent**   | Data agent          | Queries Azure DB for customer order details.                   |
| **Product Lookup Agent** | Data agent          | Retrieves product specifications or related data.              |
| **Parser**               | Data normalizer     | Converts query results into readable format for LLMs.          |
| **Prompt Template**      | Instruction builder | Standardizes agent prompts with consistent tone and structure. |
| **Chat Output**          | Response handler    | Sends back unified, natural language responses to the user.    |


__Key Features__

🧩 Flow-Based Design: Modular Langflow architecture - easy to visualize, edit, and extend.

🔍 RAG Pipeline: Integrates document loaders, embeddings, and vector stores to retrieve contextually relevant knowledge.

🗣️ LLM-Driven Conversations: Uses GPT-based models to provide natural, accurate responses.

📚 Custom Knowledge Base: Trained on company-specific FAQs, manuals, and policy documents.

🛠️ Parser Error Handling: Implements improved type validation and flow guards to prevent List of Data objects not supported errors.

⚡ Scalable Backend: Easily deployable via FastAPI or Langflow’s hosted interface.

| Layer                   | Tools / Frameworks                                      |
| ----------------------- | ------------------------------------------------------- |
|  Framework            | **Langflow** (for visual orchestration)                 |
|  LLM Backend          | **OpenAI GPT-4**                                        |
|  Retrieval            | **Azure AI Search**                                     |
|  Database Integration | **Azure DB Tools** (custom queries for products/orders) |
|  Preprocessing        | Langflow File Loader, Split Text, Parser                |
|  Deployment           | Langflow Cloud                                          |

Features

 Agent Collaboration: FAQ, Manager, Product, and Order Agents coordinate seamlessly.

 Contextual RAG: Retrieves accurate information from company documents, PDFs, and knowledge bases.

 Decision Routing: Manager Agent dynamically routes requests to the right expert agent.

 Conversational Memory: Maintains dialogue context across multiple exchanges.

 Structured Query Handling: Azure DB Tools connect to real customer/product databases.

 Modular Flow Design: Easily extend to new domains (billing, technical support, etc.).

 __Example Use Cases__

“Where can I track my shipment?” → Routed to Order Lookup Agent

“Tell me the warranty policy for Product X.” → Routed to Product Lookup Agent

“How do I reset my password?” → Handled by FAQ Agent

“I need help updating my billing info.” → Delegated by Manager Agent

__Flow Snapshot__

Below is the visual representation of the flow built in Langflow:

<img width="900" height="605" alt="image" src="https://github.com/user-attachments/assets/e823a6d2-796d-4858-b361-e38b015c2d1d" />

__Impact & Use Cases__

50–70% reduction in manual support workload

Consistent, brand-aligned customer responses

24×7 intelligent support without human intervention
