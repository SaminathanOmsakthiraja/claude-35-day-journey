# Day 03 - Claude Projects & Persistent Context

## 🎯 Objective

Today I explored **Claude Projects** and how project-level context can make AI-assisted development more consistent and useful.

The main question I wanted to explore was:

> **What changes when Claude has persistent project context instead of treating every conversation as a completely new task?**

---

## 🧠 The Problem

In a normal chat, I might repeatedly have to explain:

- What project I'm working on
- Which technologies I'm using
- How the project is structured
- What constraints I have
- What I want Claude to avoid
- How I want Claude to work with me

For example:

```text
I'm working on a Java project.
It's a console application.
I'm using OOP.
I don't want file handling.
There are Admin, Teacher and Student roles...
```

If I have to repeat this information across multiple conversations, the workflow becomes inefficient.

---

## 💡 What I Learned About Claude Projects

A Claude Project provides a dedicated workspace where project-specific instructions, knowledge, files, and conversations can be organized around a common objective.

Instead of thinking:

```text
New Chat
	 ↓
Explain Project
	 ↓
Ask Question
```

I can structure it as:

```text
Claude Project
			│
			├── Project Instructions
			├── Relevant Knowledge
			├── Project Files
			└── Project Conversations
							│
							↓
					New Task
							│
							↓
						Claude
```

This creates a more focused environment for long-running work.

---

## 🛠️ My Experiment

I created a Claude Project around my Java project:

### V3 Quiz Analyser

#### Project Type

Java console-based application

#### Technology

- Java
- Eclipse
- Object-Oriented Programming

#### Main Roles

```text
Admin
	↓
Teacher
	↓
Student
```

The project includes subjects such as:

- Java
- DSA
- Aptitude
- Python

---

## 📋 Project Context

I provided Claude with project-level information including:

```text
Project objective
Technology
Architecture
Roles
Features
Current limitations
Development constraints
Preferred workflow
```

I also instructed Claude not to immediately generate code whenever I describe a problem.

Instead, it should:

```text
Understand
		↓
Analyze
		↓
Identify missing requirements
		↓
Plan
		↓
Wait for approval
		↓
Implement
		↓
Test
		↓
Review
```

---

## 🧪 Experiment 1 - Understanding the Project

After providing the project context, I asked Claude:

> Tell me what you understand about this project and separate your assumptions from the information I explicitly provided.

### Why I asked this

I wanted to check whether Claude could distinguish between:

- **Known information**
- **Assumptions**

This is important because AI can sometimes fill missing information with reasonable-sounding assumptions.

---

## 🧪 Experiment 2 - Adding a New Feature

I then gave Claude a feature requirement:

> Multiple teachers should be able to manage the same subject.

Instead of asking for code immediately, I asked Claude to:

1. Understand the requirement.
2. Identify affected parts of the project.
3. Propose a design.
4. Identify missing information.
5. Avoid writing code until the approach is clear.

This helped me understand how project context can be combined with a new task.

---

## 🔍 What I Observed

### Without project context

Claude needs to ask or infer:

```text
What project?
What technology?
What architecture?
What constraints?
What existing classes?
```

### With project context

The conversation can start closer to the actual development task:

```text
Existing project context
				+
New requirement
				↓
More focused discussion
```

This reduces unnecessary repetition and makes the interaction more project-oriented.

---

## ⚠️ Important Lesson

Persistent context does **not** mean I should put everything into a project.

Project-level information should generally be:

### Relevant

It should help Claude work on the project.

### Stable

It should remain useful across multiple conversations.

### Clear

It should be easy for Claude to understand and follow.

For example:

```text
Good project context:
Java 17
OOP architecture
Project requirements
Coding conventions
Project constraints
```

Instead of:

```text
Unnecessary context:
Today's temporary task
Random questions
Unrelated college information
Temporary debugging details
```

---

## 🧠 Prompt vs Project Context

One of today's most useful distinctions:

### Prompt

Describes the **current task**.

```text
Add a feature for multiple teachers per subject.
```

### Project Context

Describes the **environment in which the task exists**.

```text
This is a Java console application.

It follows an OOP design.

The project has Admin, Teacher and Student roles.

Data is currently stored in code.

File handling is not being used.
```

Together:

```text
Project Context
			 +
Current Task
			 ↓
Better AI Collaboration
```

---

## 🔄 My Current AI Development Workflow

After today's learning, my workflow is becoming:

```text
										PROJECT CONTEXT
													 │
													 ↓
										Current Requirement
													 │
													 ↓
											 Claude
													 │
										┌──────┴──────┐
										↓             ↓
								 Analysis       Questions
										│             │
										└──────┬──────┘
													 ↓
												 Plan
													 ↓
												Review
													 ↓
										 Implementation
													 ↓
												 Testing
													 ↓
												 Review
```

The important part is that **I remain involved in the decision-making process**.

---

## 💡 Key Takeaways

1. Context can be organized at the project level.
2. Persistent project information reduces unnecessary repetition.
3. Stable project information should be separated from temporary tasks.
4. Claude should not be expected to know information that was never provided.
5. I should distinguish Claude's assumptions from actual project requirements.
6. AI-assisted development works better when I define the workflow instead of simply asking for code.

---

## 🔗 Connection to Day 2

### Day 2

**Context Engineering**

> Give AI the right context.

### Day 3

**Claude Projects**

> Organize that context around a long-running project.

So the progression is:

```text
Day 2
Context Engineering
			 ↓
Day 3
Project-level Context
			 ↓
Day 4
Project Knowledge & Files
			 ↓
Day 5+
Advanced Claude Workflows
```

---

## 🚀 Next Step

Tomorrow I want to explore how **files and project knowledge** can be incorporated into a Claude Project.

The goal is to move from:

```text
Claude knows what I tell it
```

towards:

```text
Claude can work with the actual project information
```

---

## 📌 Progress

| Topic | Status |
|---|---|
| Claude Fundamentals | ✅ |
| Context Engineering | ✅ |
| Claude Projects | ✅ |
| Project-level Context | ✅ |
| Project Knowledge & Files | 🔜 |
| Advanced Instructions | 🔜 |
| Claude Code | 🔜 |
| MCP | 🔜 |
| Claude API | 🔜 |
| AI Application | 🔜 |

**Day 03 / 35 - Completed**

> Learn → Experiment → Build → Document → Improve
