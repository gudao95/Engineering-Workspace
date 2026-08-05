\# Standard Operating Procedure (SOP)



> Version: 1.0



This document defines the standard workflow for executing engineering tasks inside the Engineering Workspace.



Every development task, regardless of project size, should follow this procedure.



\---



\# Purpose



The purpose of this SOP is to ensure that every task follows a consistent engineering process.



The objective is not only to complete work, but also to improve the engineering workspace continuously.



\---



\# Scope



This SOP applies to:



\- New feature development

\- Bug fixing

\- Refactoring

\- Documentation updates

\- Architecture improvements

\- Code review

\- Technical investigation



\---



\# Execution Workflow



Every engineering task follows the same lifecycle.



```

Receive Task

&#x20;       │

&#x20;       ▼

Understand Requirement

&#x20;       │

&#x20;       ▼

Locate Target Project

&#x20;       │

&#x20;       ▼

Read Required Documents

&#x20;       │

&#x20;       ▼

Analyze Existing Implementation

&#x20;       │

&#x20;       ▼

Design Solution

&#x20;       │

&#x20;       ▼

Implement

&#x20;       │

&#x20;       ▼

Self Verification

&#x20;       │

&#x20;       ▼

Update Documentation

&#x20;       │

&#x20;       ▼

Update Memory

&#x20;       │

&#x20;       ▼

Complete

```



No step should be skipped without a valid reason.



\---



\# Step 1 — Receive Task



Objectives:



\- Understand the user's request.

\- Identify the expected outcome.

\- Clarify ambiguous requirements before implementation.



Deliverable:



\- A clear implementation objective.



\---



\# Step 2 — Understand Requirement



Determine:



\- Business objective

\- Functional scope

\- Constraints

\- Risks

\- Expected behavior



If any critical information is missing:



Stop implementation.



Ask concise clarification questions.



\---



\# Step 3 — Locate Target Project



Identify the correct project.



Example:



```

projects/

&#x20;   MES/

```



Do not modify another project unless explicitly requested.



\---



\# Step 4 — Read Required Documents



Always read:



```

README.md



↓



AGENTS.md



↓



workspace.yaml

```



Then read project documentation related to the current task.



Examples:



\- Project README

\- Requirements

\- Architecture

\- API

\- Existing SOP



Read only documents relevant to the task.



\---



\# Step 5 — Analyze Existing Implementation



Before writing code:



Understand:



\- Existing architecture

\- Current implementation

\- Dependencies

\- Naming convention

\- Existing reusable components



Prefer extending existing implementation instead of creating duplicates.



\---



\# Step 6 — Design Solution



Before coding:



Evaluate:



\- Simplicity

\- Maintainability

\- Readability

\- Compatibility

\- Reusability



The preferred solution is the simplest one that satisfies the requirements.



\---



\# Step 7 — Implement



Implementation principles:



\- Small changes

\- Clear logic

\- Consistent style

\- Reuse existing components

\- Avoid unnecessary abstractions



Do not introduce unrelated modifications.



\---



\# Step 8 — Self Verification



Before finishing:



Verify:



\- Functional correctness

\- Existing behavior unchanged

\- Build success

\- No obvious regressions



When applicable:



\- Run tests

\- Review generated code

\- Check edge cases



\---



\# Step 9 — Update Documentation



Implementation is incomplete until documentation is updated.



Update documentation whenever:



\- Architecture changes

\- Workflow changes

\- Public behavior changes

\- New engineering rules are introduced



Possible documents:



\- README

\- Development Standards

\- Coding Style

\- Architecture

\- Project Documentation



\---



\# Step 10 — Update Memory



If reusable knowledge is discovered:



Update:



```

memory/

```



Possible categories:



\- Compound

\- Pitfalls



Do not store reusable knowledge only inside project notes.



\---



\# Completion Checklist



Before closing a task, confirm:



\- Requirement completed

\- Existing functionality preserved

\- Documentation updated

\- Memory updated if applicable

\- No unrelated files modified

\- Engineering standards followed



\---



\# Escalation Rules



Stop implementation and ask for clarification if:



\- Requirements conflict

\- Business logic is unknown

\- Architecture impact is significant

\- Required information is missing

\- Multiple reasonable solutions exist without clear preference



Never guess critical business behavior.



\---



\# Continuous Improvement



Every completed task should improve at least one of the following:



\- Code quality

\- Documentation

\- Engineering standards

\- Reusable templates

\- Engineering memory



Engineering quality improves incrementally.



\---



\# Success Criteria



A task is considered complete only when:



\- Implementation is correct.

\- Documentation is synchronized.

\- Reusable knowledge has been captured.

\- The workspace is in a better state than before the task started.



```

Good engineering is repeatable engineering.

```

