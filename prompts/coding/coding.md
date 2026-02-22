# Coding Prompts

> Prompts for AI-assisted coding — debugging, code generation, optimization, architecture, and more.

**Best with:** Claude Code, GitHub Copilot, Cursor, ChatGPT Code Interpreter

---

## Code Generation

### 1. Function Generator
```
Write a [language] function that [describe what it does].

Requirements:
- Input: [describe inputs with types]
- Output: [describe expected output with type]
- Handle edge cases: [list edge cases]
- Time complexity: O([target])
- Include docstring/comments
- Add type hints/annotations
- Write 3 example usages

No external dependencies unless absolutely necessary.
```

### 2. CRUD API Endpoint
```
Create a complete CRUD API for a [resource name] using [framework].

Model fields: [list fields with types]
Include:
- Create (POST) with input validation
- Read single (GET /:id) with 404 handling
- Read all (GET) with pagination, sorting, filtering
- Update (PUT /:id) with partial update support
- Delete (DELETE /:id) with soft delete
- Error handling middleware
- Request/response type definitions

Follow RESTful conventions.
```

### 3. React Component
```
Create a React component for [describe component].

Requirements:
- TypeScript with proper interfaces
- Props: [list props]
- State management: [useState/useReducer/context]
- Responsive design (mobile-first)
- Accessible (ARIA labels, keyboard navigation)
- Loading and error states
- Unit test file using [Jest/Vitest/RTL]

Style with [Tailwind CSS / CSS Modules / styled-components].
```

### 4. Database Schema
```
Design a database schema for [describe application].

Requirements:
- Use [PostgreSQL/MySQL/MongoDB]
- Include tables/collections for: [list entities]
- Define relationships (1:1, 1:N, M:N)
- Add indexes for common queries
- Include created_at, updated_at timestamps
- Write migration SQL / schema definition
- Seed data script with 5 example records per table

List the top 5 queries this schema will need to handle efficiently.
```

### 5. CLI Tool
```
Build a command-line tool in [language] that [describe functionality].

Features:
- Argument parsing with help text (--help)
- Subcommands: [list commands]
- Config file support (.json or .yaml)
- Colored output
- Progress bar for long operations
- Error messages with suggestions
- Exit codes (0 success, 1 error)

Include a README with installation and usage examples.
```

## Debugging & Fixing

### 6. Bug Diagnosis
```
This code produces [describe the wrong behavior].
Expected behavior: [what should happen].
Error message (if any): [paste error].

1. What is the root cause?
2. Why does this specific bug occur?
3. What is the minimal fix?
4. Are there similar bugs elsewhere that I should check?
5. How can I add a test to prevent this regression?

Code: [paste code]
```

### 7. Performance Optimizer
```
This code is slow. Profile it mentally and optimize:

1. Identify the bottleneck (which lines/operations are expensive)
2. What is the current time/space complexity?
3. What can we improve it to?
4. Show the optimized version
5. Explain the tradeoffs (readability vs speed, memory vs time)
6. Benchmark: how would you measure the improvement?

Code: [paste code]
```

### 8. Error Handler
```
Add comprehensive error handling to this code:

1. What can go wrong at each step?
2. Add try/catch with specific error types
3. Create custom error classes if needed
4. Add meaningful error messages (for developers AND users)
5. Implement retry logic where appropriate
6. Add logging at appropriate levels (error, warn, info)
7. Ensure resources are cleaned up (finally blocks, context managers)

Code: [paste code]
```

## Architecture & Design

### 9. Design Pattern Selector
```
I have this problem: [describe the problem]
Current code structure: [brief description]

1. Which design pattern(s) would solve this cleanly?
2. Why this pattern over alternatives?
3. Show me a concrete implementation in [language]
4. What are the tradeoffs of this pattern?
5. When would this pattern be overkill?
```

### 10. Microservice Splitter
```
I have a monolithic [language/framework] application that handles [describe features].
Help me plan a microservice decomposition:

1. Which services should I extract and why?
2. How should services communicate (REST, gRPC, events)?
3. What data does each service own?
4. Where are the transaction boundaries?
5. What are the deployment dependencies?
6. Migration strategy (big bang vs strangler fig)?

Current pain points: [describe scaling/maintenance issues]
```

### 11. Security Audit
```
Review this code for security vulnerabilities:

Check for:
- SQL injection / NoSQL injection
- XSS (Cross-Site Scripting)
- CSRF (Cross-Site Request Forgery)
- Authentication/authorization flaws
- Sensitive data exposure
- Insecure deserialization
- Missing input validation
- Hardcoded secrets
- Insecure dependencies

For each finding:
- Severity (Critical/High/Medium/Low)
- Location in code
- Attack scenario
- Fix with code example

Code: [paste code]
```

## Data Structures & Algorithms

### 12. Algorithm Explainer
```
Explain [algorithm name] step by step:

1. What problem does it solve?
2. Walk through with this example: [provide input]
3. Show each step with the data structure state
4. Time complexity (best, average, worst) with explanation
5. Space complexity
6. When to use this vs alternatives
7. Implement in [language] with comments on each line
8. Common interview variations
```

### 13. Data Structure Chooser
```
I need to [describe operations you need — insert, delete, search, sort, etc.].
Data size: [approximate N].
Most frequent operation: [which one].
Memory constraint: [if any].

1. What data structure should I use and why?
2. What are the operation complexities?
3. Show me the implementation in [language]
4. What about concurrent access — is it thread-safe?
5. What's the alternative if requirements change to [modified requirement]?
```

## DevOps & Infrastructure

### 14. Dockerfile Builder
```
Create a production-ready Dockerfile for my [language/framework] application.

Requirements:
- Multi-stage build (separate build and runtime)
- Minimal final image size
- Non-root user
- Health check
- Proper layer caching for dependencies
- Environment variable configuration
- .dockerignore file

App details: [describe your app, its dependencies, build process]
```

### 15. CI/CD Pipeline
```
Create a CI/CD pipeline for [GitHub Actions / GitLab CI / Jenkins] that:

1. Runs on push to main and PRs
2. Linting and formatting check
3. Unit tests with coverage report
4. Integration tests
5. Security scanning (SAST)
6. Build Docker image
7. Deploy to [staging/production]
8. Notification on failure

Tech stack: [describe your stack]
```

### 16. Monitoring Setup
```
Design a monitoring and alerting strategy for [describe your application]:

1. Key metrics to track (latency, error rate, throughput, saturation)
2. Dashboard layout (what graphs, what groupings)
3. Alert rules (what triggers, thresholds, escalation)
4. Logging strategy (what to log, structured format, retention)
5. Tracing setup for distributed systems
6. Tools recommendation (Prometheus, Grafana, Datadog, etc.)

SLOs: [your targets — 99.9% uptime, <200ms p99 latency, etc.]
```

---

*40+ coding prompts for generation, debugging, architecture, and DevOps*
