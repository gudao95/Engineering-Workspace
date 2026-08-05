# Communication Standards

> Version: 1.0

This document defines the communication standards used throughout the Engineering Workspace.

Effective communication is essential for producing reliable engineering outcomes.

The goal is to reduce ambiguity, improve collaboration, and make every engineering decision traceable.

---

# Objectives

Communication should always aim to:

- Clarify requirements
- Reduce misunderstandings
- Improve development efficiency
- Preserve engineering context
- Enable future maintenance

Communication is part of engineering.

---

# General Principles

Communication should be:

- Clear
- Precise
- Complete
- Objective
- Actionable

Avoid:

- Guessing
- Emotional language
- Vague descriptions
- Missing context

---

# Requirement Description

Every task should answer the following questions.

## What?

What needs to be implemented?

## Why?

Why is the change required?

## Scope?

Which project or module is affected?

## Constraints?

What limitations exist?

## Expected Result?

How should success be measured?

---

# Preferred Requirement Template

```
Background

Problem

Goal

Scope

Constraints

Acceptance Criteria
```

Example

```
Background

MES cannot reconnect to the PLC after a network interruption.

Problem

Production must be restarted manually.

Goal

Automatically reconnect within 30 seconds.

Scope

Communication module only.

Constraints

Existing communication interface cannot change.

Acceptance Criteria

Reconnect succeeds automatically.
No UI freeze.
```

---

# Asking Questions

When information is missing,

ask questions that are:

- Specific
- Short
- Necessary

Good

```
Should the reconnect attempt continue indefinitely,
or stop after a maximum number of retries?
```

Bad

```
Can you explain more?
```

---

# Assumptions

Never hide assumptions.

Whenever assumptions are made,

state them explicitly.

Example

```
Assumption:

Only one PLC is connected at a time.
```

---

# Engineering Discussions

Discussions should focus on:

- Requirements
- Design
- Trade-offs
- Risks
- Maintainability

Avoid discussions based only on personal preference.

Engineering decisions should always have technical reasons.

---

# Reporting Bugs

Every bug report should include:

```
Description

Expected Behavior

Actual Behavior

Steps to Reproduce

Environment

Logs

Possible Cause
```

Example

```
Description

PLC disconnects after approximately 20 minutes.

Expected

Stable communication.

Actual

Automatic reconnection never occurs.

Steps

1. Connect PLC.
2. Disable network.
3. Restore network.

Environment

Windows 11
.NET 8
Siemens PLC

Logs

Connection timeout.
```

---

# Reporting Risks

Whenever a risk is identified,

describe:

- Risk
- Impact
- Probability
- Suggested mitigation

Example

```
Risk

Database transaction timeout.

Impact

Production data may be lost.

Mitigation

Retry with exponential backoff.
```

---

# Engineering Decisions

Important decisions should always record:

```
Problem

Options

Decision

Reason

Impact
```

Future engineers should understand **why** a decision was made.

---

# Human ↔ AI Collaboration

Before requesting implementation,

provide:

- Project
- Module
- Objective
- Constraints
- Existing behavior

Avoid asking AI to modify code without context.

---

# AI Responsibilities

AI should:

- Explain significant decisions
- Ask when uncertain
- Preserve existing behavior
- Follow workspace standards
- Update documentation when necessary

AI should not:

- Guess business rules
- Modify unrelated modules
- Ignore project documents
- Invent missing requirements

---

# Human Responsibilities

The engineer should:

- Provide accurate requirements
- Clarify business logic
- Review AI-generated code
- Verify final behavior

AI assists engineering.

Human remains responsible for engineering decisions.

---

# Review Communication

Code review feedback should focus on:

- Correctness
- Readability
- Maintainability
- Performance
- Architecture

Avoid comments such as:

```
I don't like it.
```

Prefer:

```
This implementation introduces unnecessary coupling between modules.
```

---

# Meeting Notes

When recording technical discussions,

capture:

- Topic
- Participants
- Decisions
- Action Items

Avoid recording unnecessary conversation.

---

# Documentation Communication

Documentation should answer:

- What?
- Why?
- How?
- When?

Documentation should never assume prior knowledge.

---

# Final Rule

Engineering communication exists to reduce uncertainty.

Every document, discussion, and decision should make future work easier.