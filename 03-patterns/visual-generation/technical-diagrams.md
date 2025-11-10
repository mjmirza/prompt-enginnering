# Technical Diagrams and Flowcharts Pattern

Structured prompts for generating clear, informative technical diagrams, flowcharts, and system architecture visuals.

## Purpose

Create precise technical diagrams that clearly communicate system architectures, processes, workflows, and technical relationships.

## When to Use

- Explaining system architecture
- Documenting workflows and processes
- Illustrating data flow
- Showing component relationships
- Creating technical documentation
- Visualizing algorithms or logic
- Design specifications

## Template Structure

```
Create a [TYPE OF DIAGRAM] showing [WHAT TO ILLUSTRATE].

Diagram specifications:
- Type: [Flowchart/Architecture diagram/Sequence diagram/ERD/Network diagram/etc.]
- Style: [Technical/clean/minimal/detailed]
- Complexity: [Simple/moderate/complex]
- Orientation: [Horizontal/vertical/hierarchical]

Elements to include:
1. [Component/Step 1] - [description]
2. [Component/Step 2] - [description]
3. [Component/Step 3] - [description]
[...]

Relationships:
- [Element A] → [Element B]: [type of relationship]
- [Element C] ↔ [Element D]: [type of relationship]

Notation:
- [Specify symbols, shapes, colors if particular standard needed]
- Labels: [Yes/No, level of detail]
- Legend: [Include if needed]

Output format: [Mermaid/PlantUML/ASCII/Description for tool X]
```

## Pattern Variations

### Simple Flowchart
```
Create a flowchart for: [PROCESS NAME]

Steps:
1. Start: [initial state]
2. [Decision point 1]
   - If yes: [action]
   - If no: [action]
3. [Process step]
4. [Decision point 2]
   - If condition A: [path A]
   - If condition B: [path B]
5. End: [final state]

Format: Mermaid diagram syntax
Style: Clean, easy to follow
Include: Decision diamonds, process rectangles, arrows with labels
```

### System Architecture Diagram
```
Design a system architecture diagram for: [SYSTEM NAME]

Components:
- Frontend: [technologies/details]
- Backend: [technologies/details]
- Database: [type/details]
- External services: [list]
- Infrastructure: [cloud/on-prem details]

Show:
- Component relationships
- Data flow directions
- API connections
- Authentication/security layers
- Scaling components

Style: Modern, clean, professional
Format: [Specify diagram tool or description]
Annotations: Key technologies and protocols
```

### Data Flow Diagram
```
Create a data flow diagram for: [SYSTEM/PROCESS]

Data sources:
- [Source 1]: [type of data]
- [Source 2]: [type of data]

Processing steps:
1. [Data ingestion]
2. [Transformation 1]
3. [Transformation 2]
4. [Storage]
5. [Output/Delivery]

Show:
- Data movement between components
- Transform operations
- Data stores
- External systems
- Validation points

Level: [Level 0 (context)/Level 1 (detailed)/Level 2 (very detailed)]
```

### Sequence Diagram
```
Create a sequence diagram showing: [INTERACTION DESCRIPTION]

Actors/Systems:
- [Actor 1]
- [System A]
- [System B]
- [Database]

Interaction flow:
1. [Actor 1] → [System A]: [action/message]
2. [System A] → [System B]: [request]
3. [System B] → [Database]: [query]
4. [Database] → [System B]: [response]
5. [System B] → [System A]: [result]
6. [System A] → [Actor 1]: [final response]

Include:
- Lifelines for each participant
- Synchronous/asynchronous calls
- Return messages
- Alt/opt/loop blocks if needed

Format: PlantUML or Mermaid
```

## Real-World Examples

### Example 1: User Authentication Flow
```
Create a detailed flowchart for user authentication process:

Flow:
1. Start: User lands on login page
2. User enters credentials
3. Decision: Are credentials present?
   - No → Show error "Please enter credentials" → Return to step 2
   - Yes → Continue
4. Submit to server
5. Decision: Do credentials match?
   - No → Show error "Invalid credentials" → Return to step 2
   - Yes → Continue
6. Decision: Is 2FA enabled?
   - No → Generate session token → Redirect to dashboard → End
   - Yes → Continue to 2FA
7. Send 2FA code to user
8. User enters code
9. Decision: Is code valid?
   - No → Show error "Invalid code" → Return to step 8 (max 3 attempts)
   - Yes → Generate session token → Redirect to dashboard → End

Special cases:
- Account locked after 5 failed attempts
- 2FA code expires after 5 minutes

Format: Mermaid flowchart
Style: Professional, clear decision points
Colors: Use green for success paths, red for error paths
```

### Example 2: Microservices Architecture
```
Design a system architecture diagram for an e-commerce platform:

Frontend Components:
- Web application (React)
- Mobile app (React Native)
- Admin dashboard

Backend Services (microservices):
- API Gateway (Kong)
- User Service (Node.js)
- Product Catalog Service (Python)
- Order Service (Java)
- Payment Service (Node.js)
- Notification Service (Go)
- Inventory Service (Python)

Data Layer:
- User DB (PostgreSQL)
- Product DB (MongoDB)
- Order DB (PostgreSQL)
- Cache (Redis)
- Message Queue (RabbitMQ)

External Services:
- Payment gateway (Stripe)
- Email service (SendGrid)
- SMS service (Twilio)
- CDN (CloudFlare)

Infrastructure:
- Container orchestration (Kubernetes)
- Cloud provider (AWS)
- Load balancer
- API gateway

Show:
- Service-to-service communication
- Database connections
- Message queue pub/sub
- External API calls
- Authentication flow
- Caching layer

Style: Clean, modern, professional
Include: Technology labels, communication protocols (REST/gRPC)
Highlight: Security boundaries, public vs. private services
```

### Example 3: Data Pipeline
```
Create a data flow diagram for analytics pipeline:

Data Sources:
- Application database (PostgreSQL) - user events
- Web analytics (Google Analytics) - page views
- Third-party API - market data
- Log files - system logs

Pipeline Stages:
1. Ingestion:
   - Database CDC (Change Data Capture)
   - API polling (hourly)
   - Log streaming (real-time)
   - Web analytics export (daily)

2. Processing:
   - Data validation and cleaning
   - Format standardization
   - Enrichment with reference data
   - Aggregation and calculations

3. Storage:
   - Raw data lake (S3)
   - Processed data warehouse (Snowflake)
   - Real-time cache (Redis)

4. Consumption:
   - BI dashboards (Tableau)
   - ML models (SageMaker)
   - Reports (automated email)
   - API for applications

Technologies:
- Ingestion: Apache Kafka, Fivetran
- Processing: Apache Spark, dbt
- Orchestration: Airflow
- Monitoring: Datadog

Show:
- Data flow direction with arrows
- Batch vs. streaming paths
- Data transformation points
- Error handling/dead letter queues
- Monitoring touchpoints

Format: Comprehensive DFD with annotations
Complexity: Level 1 (show main processes and data stores)
```

## Best Practices

1. **Clear Purpose**: Define what the diagram should communicate
2. **Appropriate Detail**: Match complexity to audience
3. **Consistent Notation**: Use standard symbols and conventions
4. **Logical Flow**: Arrange elements for natural reading (top-to-bottom, left-to-right)
5. **Clear Labels**: Name everything precisely
6. **Show Relationships**: Make connections explicit
7. **Use Colors Purposefully**: Highlight important elements, group related items
8. **Include Legend**: If using non-standard notation

## Common Pitfalls

- Too much information on one diagram
- Inconsistent symbols or notation
- Unclear arrows or relationships
- Missing labels
- Poor layout causing crossed lines
- Using wrong diagram type for the message
- Skipping important components
- Not showing error/exception paths

## Tips for Optimization

- Specify the exact diagram type needed
- Indicate your preferred tool/format
- Mention the target audience (technical level)
- Request specific notation standards (UML, BPMN, etc.)
- Indicate if you need multiple views (high-level + detailed)
- Specify important aspects to emphasize
- Request both diagram and supporting description
- Ask for annotations or notes if needed

## Diagram Types Guide

**Flowcharts**: Processes, algorithms, workflows, decision trees
**Architecture Diagrams**: System components, infrastructure, deployments
**Sequence Diagrams**: Interactions over time, API calls, protocols
**ERD**: Database schema, entity relationships
**Class Diagrams**: Object-oriented design, code structure
**Network Diagrams**: Network topology, connections, infrastructure
**State Diagrams**: State transitions, lifecycle, FSM
**Data Flow Diagrams**: Data movement, transformations, processing
**Component Diagrams**: Software components, dependencies, interfaces
**Deployment Diagrams**: Physical deployment, servers, nodes

## Output Format Options

### Mermaid Syntax
```
graph TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Process]
    B -->|No| D[Alternative]
    C --> E[End]
    D --> E
```

### PlantUML
```
@startuml
actor User
User -> System: Request
System -> Database: Query
Database --> System: Data
System --> User: Response
@enduml
```

### ASCII Art
```
+----------+      +----------+      +----------+
|  Client  | ---> |  Server  | ---> | Database |
+----------+      +----------+      +----------+
```

## Combining with Other Techniques

- **Diagrams + Documentation**: Embed diagrams in technical docs
- **Diagrams + Code**: Generate from code or config
- **Diagrams + Presentations**: Use in architecture reviews
- **Diagrams + Testing**: Document test scenarios
- **Multiple Diagram Types**: Show different views of same system

## Related Patterns

- System Architecture Pattern
- Process Documentation Pattern
- API Documentation Pattern
- Visual Metaphor Pattern (for conceptual diagrams)
- Technical Writing Pattern
