# API Reference

Base URL: `http://localhost:3001/api`

## Agents

### List All Agents

```
GET /agents
```

Query Parameters:
- `category` (optional) - Filter by category
- `search` (optional) - Search by name/description
- `sort` (optional) - Sort by: popularity, rating, price-low, price-high

Response:
```json
[
  {
    "id": "agent-001",
    "name": "CodeMaster Pro",
    "vendor": "DevTools Inc.",
    "category": "Development",
    "description": "...",
    "price": 49.99,
    "rating": 4.8,
    "reviews": 342,
    "icon": "⚡",
    "tags": ["code-generation"],
    "stats": { "deployments": 12500, "uptime": 99.9 }
  }
]
```

### Get Agent

```
GET /agents/:id
```

### Get Deployed Agents

```
GET /deployed
```

### Deploy Agent

```
POST /deploy
```

Body:
```json
{
  "agentId": "agent-001",
  "config": {}
}
```

### Update Deployed Agent

```
PATCH /deployed/:id
```

Body:
```json
{
  "status": "running" | "stopped",
  "config": {}
}
```

### Remove Deployed Agent

```
DELETE /deployed/:id
```

## Workflows

### List Workflows

```
GET /workflows
```

### Create Workflow

```
POST /workflows
```

Body:
```json
{
  "name": "My Workflow",
  "nodes": [],
  "edges": []
}
```

### Update Workflow

```
PATCH /workflows/:id
```

### Delete Workflow

```
DELETE /workflows/:id
```

## Statistics

### Get Dashboard Stats

```
GET /stats
```

Response:
```json
{
  "totalDeployed": 5,
  "activeWorkflows": 2,
  "totalApiCalls": 1250,
  "uptime": 99.8
}
```
