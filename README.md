

 Agent_marketplace
# Agent Marketplace

## GitHub Repository

[https://github.com/harinisri2/Agent_marketplace](https://github.com/harinisri2/Agent_marketplace)


## Track Chosen + Why

**Track: AI Agent Marketplace**

This track was selected to design and implement a platform where multiple AI agents can be created, managed, and accessed from a centralized marketplace. The project focuses on agent orchestration, API-based communication, and scalable backend architecture aligned with real-world AI applications.


## Features Implemented

*  AI agent marketplace interface
*  Agent creation and configuration
*  Backend REST APIs for agent management
*  OpenAI API integration for agent responses
*  Database persistence for agent data
*  Dockerized frontend and backend setup
*  Environment-based configuration management

## Tech Stack

* **Frontend:** React, HTML, CSS, JavaScript
* **Backend:** Node.js, Express.js
* **Database:** MongoDB
* **AI:** OpenAI API
* **DevOps:** Docker, Docker Compose
* **Version Control:** Git, GitHub


## How to Run Locally

```bash
git clone https://github.com/harinisri2/Agent_marketplace.git
cd Agent_marketplace
cp .env.example .env
docker-compose up --build
```

Application URL:

http://localhost:3000

---

## API Endpoints List

| Method | Endpoint        | Description                |
| ------ | --------------- | -------------------------- |
| GET    | /api/agents     | Retrieve all agents        |
| POST   | /api/agents     | Create a new agent         |
| GET    | /api/agents/:id | Fetch agent details        |
| PUT    | /api/agents/:id | Update agent configuration |
| DELETE | /api/agents/:id | Delete an agent            |

---

## Data Model

### Agent

* `id` – ObjectId
* `name` – String
* `description` – String
* `model` – String
* `systemPrompt` – String
* `createdAt` – Date

---

## AI Usage Log

* OpenAI API is used to generate agent responses
* Agent-specific prompts are dynamically constructed
* API keys are managed using environment variables
* AI calls are processed server-side for security

---

## Trade-offs + Next Improvements

* Single AI provider used to simplify initial implementation
* Minimal authentication to reduce setup complexity
* Basic UI design focused on functionality

**Next Improvements**

* User authentication and role-based access
* Support for multiple AI models/providers
* Agent usage analytics and monitoring
* Rating and feedback system
* Cloud deployment and scalability enhancements

---

## Sample Data

```json
[
  {
    "name": "Interview Preparation Agent",
    "description": "Assists users with technical interview preparation",
    "model": "gpt-4",
    "systemPrompt": "You are an AI assistant specialized in interview preparation."
  }
]
