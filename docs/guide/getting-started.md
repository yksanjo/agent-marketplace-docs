# Getting Started

Welcome to AgentHub! This guide will help you get started with the AI Agent Marketplace.

## Prerequisites

- Node.js 18+
- npm or yarn
- A modern web browser

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/yksanjo/agent-marketplace.git
cd agent-marketplace
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start the Development Server

```bash
npm run dev
```

This will start both the backend API (port 3001) and frontend (port 5173).

## Using the Marketplace

### Browse Agents

Navigate to the Marketplace page to browse all available AI agents. Use category filters to narrow down your search.

### Deploy an Agent

1. Find an agent you want to use
2. Click the "Deploy" button
3. The agent will be added to your dashboard

### Manage Deployed Agents

Go to the Dashboard to:
- Start/stop agents
- View usage statistics
- Remove agents

### Create Workflows

Use the Orchestration page to:
1. Create a new workflow
2. Add multiple agents to the workflow
3. Run the workflow to execute agents in sequence

## API Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/agents` | GET | List all agents |
| `/api/agents/:id` | GET | Get agent details |
| `/api/deploy` | POST | Deploy an agent |
| `/api/deployed` | GET | List deployed agents |
| `/api/workflows` | GET | List workflows |
