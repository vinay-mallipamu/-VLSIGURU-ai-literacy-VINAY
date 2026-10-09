
6:Explain chatbot vs. RAG vs. agent, with a flow diagram

## 1. Understanding the Terms

**LLM (Large Language Model)**

An LLM is an AI model that understands text and generates answers based on patterns it learned during training. For example, ChatGPT uses an LLM to answer questions.

**AI Application**

An AI application is a software product that uses AI to help people with different tasks. For example, a customer support chatbot on a website helps customers find answers to their questions.

**RAG (Retrieval-Augmented Generation)**

RAG is a method where AI searches for useful information from documents or other sources before generating an answer. For example, a college chatbot can use college rules and notices to answer students' questions.

**Tool-Using Assistant**

A tool-using assistant can use tools to complete tasks or find information. For example, an assistant can use a calculator to solve a calculation or search for information online.

**Agent**

An agent is an AI system that can work toward a goal by taking multiple steps. It can use tools, check the results, and decide what to do next. For example, a travel-planning agent can compare transport and hotel prices to help plan a trip.

## 2. Flow Diagram

```text
       ┌──────────────┐
       │     USER     │
       │ Asks a       │
       │ question     │
       └──────┬───────┘
              |
              v
       ┌──────────────┐
       │    MODEL     │
       │ Understands  │
       │ the request  │
       └──────┬───────┘
              |
              v
       ┌──────────────┐
       │ TOOL /       │
       │ RETRIEVAL    │
       │ Gets useful  │
       │ information  │
       └──────┬───────┘
              |
              v
       ┌──────────────┐
       │    RESULT    │
       │ Information  │
       │ comes back   │
       └──────┬───────┘
              |
              v
       ┌──────────────┐
       │   RESPONSE   │
       │ Gives an     │
       │ answer or    │
       │ takes action │
       └──────────────┘
```

An agent can repeat the process of using a tool and checking the result until it completes the task or needs help from the user.

## 3. Comparison Table

| Term                 | What it means                                              | Example                                                            |
| -------------------- | ---------------------------------------------------------- | ------------------------------------------------------------------ |
| LLM                  | An AI model that generates text based on learned patterns. | ChatGPT answering a question.                                      |
| AI application       | Software that uses AI to perform a task.                   | A customer support chatbot.                                        |
| RAG                  | Retrieves information before generating an answer.         | A chatbot answering questions from college documents.              |
| Tool-using assistant | An assistant that uses tools when needed.                  | An assistant using a calculator.                                   |
| Agent                | An AI system that takes multiple steps to achieve a goal.  | An assistant that searches for travel options and compares prices. |

## 4. Everyday Example of an Agent

Imagine I want to plan a weekend trip to Goa within ₹15,000. An agent can search for transport, compare hotel prices, and calculate the total cost. It can use the results to find suitable options and suggest a plan. Before making a booking or spending money, it should ask me for confirmation.

## 5. What I Learned

I learned that an LLM mainly generates text, while an AI application uses AI to provide a service. RAG helps AI find relevant information, and a tool-using assistant can perform tasks using available tools.

An agent goes a step further by working through multiple steps toward a goal. This helped me understand that a chatbot can answer questions, while an agent can also use tools and work toward completing a task.
