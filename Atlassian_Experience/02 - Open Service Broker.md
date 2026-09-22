# 02 - Building the Open Service Broker

**Tags:** #python #fastapi #dynamodb #sqs #architecture #platform-engineering

## The "Fire Hose" Phase
Joining Atlassian is often described as "drinking from the fire hose" due to the sheer volume of information. The primary initial task was to fulfill the promise made during the interview: building an Open Service Broker.

## Open Service Broker Architecture
The goal was to facilitate self-service load balancing for internal developers in a Kubernetes-oriented environment.

- **Framework Evolution:** Started with `Connexion` (a Python library that generates API handlers from an OpenAPI document), migrated to pure `Flask`, and eventually settled on `FastAPI`.
- **Infrastructure:** DynamoDB for state and AWS SQS for asynchronous task queuing.
- **Workflow:**
  1. A client submits a provisioning request (e.g., "please provision load balancing").
  2. The FastAPI web worker drops the task details into an SQS queue.
  3. An asynchronous worker picks up the task and performs the actual provisioning (e.g., creating DNS records, CloudFront distributions).
  4. The worker writes the completed state to DynamoDB.
  5. The client polls the web server, which checks DynamoDB and responds when the resource is ready.
