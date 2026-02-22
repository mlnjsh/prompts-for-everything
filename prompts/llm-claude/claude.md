# Claude AI Prompts

> Prompts optimized for Claude 3.5, Claude Code, and the Anthropic API. Leverage Claude's strengths in analysis, coding, and structured thinking.

**Best with:** Claude 3.5 Sonnet/Opus, Claude Code

---

## Analysis & Reasoning

### 1. Document Analyzer
```
Analyze this document thoroughly. Provide:

1. **Executive Summary** (3 sentences max)
2. **Key Claims** — List every factual claim made
3. **Evidence Quality** — Rate each claim: Strong/Moderate/Weak/Unsupported
4. **Logical Gaps** — What's missing or assumed without justification?
5. **Bias Check** — Any slant, framing effects, or one-sided arguments?
6. **Actionable Takeaways** — What should I do based on this?

Document: [paste document]
```

### 2. Code Review Expert
```
Review this code as a senior engineer doing a thorough PR review.

Check for:
- Bugs and edge cases
- Security vulnerabilities (OWASP Top 10)
- Performance issues
- Code style and readability
- Missing error handling
- Test coverage gaps

For each issue:
- Severity: Critical / Major / Minor / Nitpick
- Line reference
- What's wrong
- How to fix it (with code)

Code: [paste code]
```

### 3. Architecture Advisor
```
I'm building [describe system/app]. Help me design the architecture.

Context:
- Scale: [expected users/requests]
- Team size: [X developers]
- Budget: [constraints]
- Timeline: [deadline]

Provide:
1. High-level architecture diagram (describe in text/ASCII)
2. Technology choices with justification for each
3. Data flow between components
4. Scaling strategy
5. What could go wrong and how to prevent it
6. What I'll regret if I don't think about it now
```

### 4. Contract / Legal Analyzer
```
Analyze this contract/agreement for me (I am NOT asking for legal advice,
just help understanding the document):

1. **Plain English Summary** — What does this actually say?
2. **Key Obligations** — What am I agreeing to do?
3. **Rights** — What rights do I have?
4. **Red Flags** — Unusual or potentially unfavorable clauses
5. **Missing Provisions** — What's NOT covered that should be?
6. **Questions to Ask** — What should I clarify before signing?

Agreement text: [paste text]
```

### 5. Data Interpretation
```
Here is a dataset/results. Analyze it and provide:

1. **Pattern Summary** — What are the main trends?
2. **Anomalies** — Anything unexpected or outlier-ish?
3. **Correlations** — What seems to move together?
4. **Causation Warning** — What correlations might NOT be causal?
5. **Missing Data** — What additional data would strengthen analysis?
6. **Visualization Recommendations** — Best chart types for this data
7. **Plain English Conclusion** — What does this mean in practical terms?

Data: [paste data]
```

## Claude Code Specific

### 6. Codebase Explorer
```
I'm new to this codebase. Help me understand it:
1. What is the overall architecture?
2. What are the main entry points?
3. How is the project structured (key directories)?
4. What are the core abstractions/patterns used?
5. Where is the business logic vs infrastructure code?
6. What dependencies does it rely on?
7. How do I run/test/build it?
```

### 7. Bug Hunter
```
There's a bug: [describe the bug — what happens vs what should happen].

Help me fix it:
1. First, let's narrow down where the bug could be
2. What are the most likely causes?
3. What should I check first?
4. Can you find the relevant code and identify the issue?
5. Propose a fix with minimal changes
6. What tests should I add to prevent regression?
```

### 8. Refactoring Guide
```
I want to refactor [file/module/function] because [reason].

Requirements:
- Don't change external behavior (no functional changes)
- Improve: [readability / performance / testability / maintainability]
- Follow [language/framework] best practices
- Keep the diff minimal and reviewable

Show me the refactored code and explain each change.
```

### 9. Test Writer
```
Write comprehensive tests for [function/module/class].

Include:
- Happy path tests (normal expected behavior)
- Edge cases (empty input, null, boundary values)
- Error cases (invalid input, failures, exceptions)
- Integration tests if relevant

Use [pytest/jest/unittest/etc.] framework.
Follow AAA pattern: Arrange, Act, Assert.
Name tests descriptively: test_[function]_[scenario]_[expected_result]
```

### 10. API Designer
```
Design a REST API for [describe the feature/resource].

Provide:
1. Endpoints (method, path, description)
2. Request/Response schemas (JSON)
3. Authentication approach
4. Error response format
5. Pagination strategy
6. Rate limiting recommendation
7. Example curl commands for each endpoint

Follow REST best practices. Use consistent naming conventions.
```

## Structured Output

### 11. JSON Extractor
```
Extract structured data from this unstructured text and return valid JSON.

Schema I need:
{
  "field1": "type and description",
  "field2": "type and description",
  "field3": ["array of items if applicable"]
}

If a field is not found in the text, use null.
If you're unsure about a value, add a "confidence" field (high/medium/low).

Text: [paste text]
```

### 12. Comparison Table Builder
```
Create a detailed comparison table for [items to compare].

Columns: [list the criteria/features to compare]

Requirements:
- Use consistent rating system (checkmarks, scores, or descriptive)
- Include a "Best For" row at the bottom
- Add brief notes where a simple rating isn't enough
- Format as a clean markdown table

Output the table, then a 2-3 sentence verdict.
```

### 13. Technical Documentation
```
Write technical documentation for [code/API/system].

Include:
1. **Overview** — What it does, why it exists (2-3 sentences)
2. **Quick Start** — Minimum steps to get running
3. **API Reference** — All public methods/endpoints with params and returns
4. **Examples** — 3 real-world usage examples
5. **Configuration** — All options with defaults
6. **Troubleshooting** — Common issues and solutions

Style: Clear, concise, developer-friendly. No fluff.
```

## Creative Uses

### 14. Explain My Code to Non-Technical People
```
Explain what this code does to a non-technical stakeholder
(business person, manager, client).

Use:
- Zero jargon
- Real-world analogies
- Focus on WHAT it does, not HOW
- Why it matters to the business
- Any risks or limitations they should know

Code: [paste code]
```

### 15. Technical Interview Prep
```
I'm preparing for a [role] interview at [company type].

Give me:
1. Top 10 technical questions I should expect
2. For each question:
   - The question itself
   - What the interviewer is really testing
   - A strong answer framework
   - Common mistakes to avoid
3. One system design question with a walkthrough
4. Behavioral questions with STAR format answers

My experience level: [years] years in [technologies].
```

---

*30+ Claude-optimized prompts for analysis, coding, and structured output*
