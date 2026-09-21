# Day 02 - Context Engineering
 
## 🎯 Objective

Today I learned about **Context Engineering** and how providing the right information to an AI model can significantly improve the relevance and usefulness of its responses.

The main idea I explored:

> **Good AI interaction is not only about writing a good prompt. It is also about providing the right context.**

---

## 🧠 What is Context Engineering?

Context Engineering is the practice of providing an AI model with the relevant information, instructions, constraints, examples, and background needed to perform a task effectively.

Instead of thinking only about:

```text
Prompt -> Response
```

I started thinking about:

```text
Context
   +
Goal
   +
Constraints
   +
Workflow
   v
AI Response
```

The objective is not to provide as much information as possible.

The objective is to provide **relevant information at the right time**.

---

## 🔍 Prompt vs Context

### Basic Prompt

For example:

```text
Build a Java login system.
```

This leaves many things unspecified.

Claude may need to make assumptions about:

- Java version
- Application type
- Database
- Architecture
- Authentication method
- Security requirements
- Existing project structure
- Dependencies

The result may therefore be technically valid but unsuitable for the actual project.

### Context-Rich Request

A better request can provide:

```text
I'm building a Java 17 Spring Boot application.

The project follows:

Controller -> Service -> Repository

The application uses MySQL.

I need email/password authentication.

Follow the existing architecture.

Don't introduce unnecessary dependencies.

Security is important.

Before writing code, analyze the requirements
and provide an implementation plan.
```

Now Claude has much more information about the environment and expectations.

---

## 🧩 Four Important Context Layers

During today's exploration, I identified four useful layers of context.

### 1. Goal

What are we trying to accomplish?

Example:

```text
Build an authentication system.
```

### 2. Environment

Where will the solution operate?

Example:

```text
Java 17
Spring Boot
MySQL
Controller -> Service -> Repository
```

### 3. Constraints

What rules or limitations should be followed?

Example:

```text
Don't modify the existing architecture.

Don't introduce unnecessary dependencies.

Follow the existing coding conventions.
```

### 4. Workflow

How should Claude approach the task?

Example:

```text
1. Understand the requirements.
2. Analyze the existing architecture.
3. Identify missing information.
4. Create an implementation plan.
5. Wait for approval.
6. Implement.
7. Test.
8. Review the changes.
```

This changes Claude from simply generating an answer into following a defined development process.

---

## 🧪 Experiment

I compared two approaches.

### Experiment 1 - Minimal Context

```text
Build a Java login system.
```

#### Observation

The request is ambiguous.

Claude has to make several assumptions about the project and requirements.

### Experiment 2 - Context-Rich Request

```text
I'm building a Java 17 Spring Boot application.

The application uses:

- Controller
- Service
- Repository
- MySQL

I want to implement authentication.

Follow the existing architecture.

Don't introduce unnecessary dependencies.

Security is important.

Before writing code:
1. Analyze the requirements.
2. Identify missing information.
3. Create an implementation plan.
4. Wait for my approval.
```

#### Observation

The second request provides:

- Project context
- Technology context
- Architectural constraints
- Security expectations
- A defined workflow

This makes the expected output more specific and reduces unnecessary assumptions.

---

## 🔄 Workflow I Learned

A useful AI-assisted development workflow is:

```text
Understand
	v
Analyze
	v
Plan
	v
Approve
	v
Implement
	v
Test
	v
Review
	v
Improve
```

Instead of asking Claude to immediately generate everything, I can control the process step by step.

---

## ⚠️ Important Lesson

### More context does NOT automatically mean better context.

Adding irrelevant information can make the interaction unnecessarily complicated.

For example, while debugging a Java method, Claude may only need:

```text
Problem
+
Relevant code
+
Expected output
+
Actual output
+
Constraints
```

It does not need unrelated project information.

So the goal is:

> **Relevant context, not maximum context.**

---

## 💡 Key Takeaways

1. AI output depends heavily on the quality and relevance of the context provided.
2. A prompt should communicate more than just the task when the task is complex.
3. Project architecture and constraints are important when asking AI to modify existing software.
4. AI can be given a workflow instead of simply being asked for an answer.
5. Human review is still important.

The goal is not:

```text
AI does everything.
```

It is:

```text
Human + AI
	 v
Better development workflow
```

---

## 🧠 Mental Model

My current mental model for effective Claude usage is:

```text
			  CONTEXT
				 |
	   +---------+---------+
	   v         v         v
	 Goal   Environment  Constraints
	   |         |         |
	   +---------+---------+
				 v
			 Workflow
				 v
			  Claude
				 v
			  Output
				 v
			Human Review
```

---

## 🚀 What's Next?

The next step is to move from individual prompts to **persistent project context**.

I want to explore how Claude can maintain useful project-level information instead of requiring the same context to be provided repeatedly.

### Next Topic

**Day 3 -> Projects & Persistent Context**

---

## 📌 Progress

| Item | Status |
| --- | --- |
| Claude fundamentals | ✅ |
| Context Engineering | ✅ |
| Goal + Environment + Constraints | ✅ |
| AI workflow control | ✅ |
| Persistent project context | 🔜 |
| Claude Code | 🔜 |
| MCP | 🔜 |
| Claude API | 🔜 |

**Day 02 / 35 - Completed**
