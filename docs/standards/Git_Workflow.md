\# Git Workflow



> Version: 1.0



This document defines the Git workflow used by Engineering Workspace projects.



The purpose is to maintain a clear, traceable, and recoverable development history.



\---



\# Objectives



A good Git workflow should provide:



\- Clear change history

\- Safe rollback capability

\- Easy collaboration

\- Reliable AI-assisted development

\- Controlled project evolution



\---



\# Core Principles



\## Commit is a Milestone



A commit represents a meaningful engineering state.



A commit should:



\- Have a clear purpose

\- Be understandable later

\- Keep the project buildable when possible



Avoid meaningless commits.



Bad:



```

update

fix

test

change

```



Good:



```

feat: add MES production order query



fix: handle PLC reconnect timeout



docs: update communication SOP

```



\---



\# Commit Frequency



Commit frequently.



Recommended:



\- After completing a small feature

\- After fixing a bug

\- After completing a refactoring step

\- After documentation changes



Avoid waiting until many unrelated changes accumulate.



\---



\# Commit Scope



One commit should solve one problem.



Good:



```

feat: add barcode scanner service

```



Bad:



```

feat: add scanner

fix database

change UI

update docs

```



Large changes should be separated.



\---



\# Commit Message Convention



Use Conventional Commits format.



Structure:



```

type: description

```



\---



\# Commit Types



\## feat



New feature.



Example:



```

feat: add production order management

```



\---



\## fix



Bug fix.



Example:



```

fix: prevent database connection leak

```



\---



\## refactor



Code improvement without behavior change.



Example:



```

refactor: simplify alarm service

```



\---



\## docs



Documentation changes.



Example:



```

docs: update coding standards

```



\---



\## test



Testing changes.



Example:



```

test: add order validation tests

```



\---



\## chore



Maintenance changes.



Example:



```

chore: update dependencies

```



\---



\# AI Assisted Development Workflow



When AI modifies code:



Follow this sequence.



```

Before Modification



↓



Create Checkpoint Commit



↓



AI Changes



↓



Review Diff



↓



Build/Test



↓



Commit

```



\---



\# Before AI Changes



Confirm:



\- Current branch is correct

\- Working tree is clean

\- Latest changes are committed



Recommended:



```

git status

```



\---



\# After AI Changes



Always review:



```

git diff

```



Check:



\- Changed files

\- Unexpected modifications

\- Logic changes

\- Architecture impact



Never blindly accept generated code.



\---



\# AI Modification Rules



AI should:



\- Make minimal changes

\- Avoid unrelated refactoring

\- Follow existing patterns

\- Explain important decisions



AI should not:



\- Modify large areas without approval

\- Rename major structures casually

\- Remove working code



\---



\# Branch Strategy



For personal development:



Small projects:



```

main

```



is acceptable.



\---



For larger projects:



Use:



```

main



develop



feature/\*

```



Example:



```

feature/mes-production-module

```



\---



\# Feature Branch Rules



A feature branch should:



\- Have one clear purpose

\- Be merged after verification

\- Be deleted after merge



\---



\# Pull Request Principles



Before merge:



Check:



\- Requirement completed

\- Code reviewed

\- Documentation updated

\- No unnecessary changes

\- Build successful



\---



\# Version Management



Use semantic versioning.



Format:



```

MAJOR.MINOR.PATCH

```



Example:



```

1.0.0

```



\---



\# Release Process



Before release:



Verify:



\- Build success

\- Important functions tested

\- Documentation updated

\- Change log updated



Create:



\- Release tag

\- Release notes



\---



\# Rollback Strategy



Every important change must be reversible.



Preferred methods:



\- Git revert

\- Restore previous commit

\- Feature branch isolation



Avoid destructive history modification on shared branches.



\---



\# Repository Hygiene



Do not commit:



\- Build output

\- Temporary files

\- IDE cache

\- Sensitive configuration

\- Local secrets



Use:



```

.gitignore

```



\---



\# AI Generated Code Review Checklist



Before commit:



\## Functionality



\- Does it solve the requirement?



\## Safety



\- Did it modify unrelated code?



\## Maintainability



\- Is the design consistent?



\## Documentation



\- Should any document be updated?



\## Memory



\- Is there reusable experience?



\---



\# Final Rule



Git is not only a backup system.



Git is the engineering history of the project.



Every commit should help future developers understand:



\- What changed

\- Why it changed

\- How it evolved

