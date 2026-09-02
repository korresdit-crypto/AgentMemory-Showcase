# 🎬 Demo Scenarios

Ниже перечислены сценарии, которые хорошо демонстрируют возможности AgentMemory.

## 1. Исправление бага

```text
Bug
 ↓
Reproduce
 ↓
Context Retrieval
 ↓
Codex Fix
 ↓
Regression Test
 ↓
Independent Review
 ↓
Gate
```

## 2. Архитектурная задача

```text
Requirements
    ↓
Claude Architecture Review
    ↓
Implementation Plan
    ↓
Codex Implementation
    ↓
Verification
```

## 3. Security finding

```text
Finding
  ↓
Evidence
  ↓
Root Cause
  ↓
Remediation
  ↓
Security Tests
  ↓
Independent Verification
```

## 4. Recovery после timeout

```text
Timeout
  ↓
Persist Failure State
  ↓
Validate Repository
  ↓
Determine Resume Point
  ↓
Retry / Fallback / Human Review
```

## 5. Долговременная память

```text
Session 1
  ↓
Project Decisions Saved
  ↓
Session Ends
  ↓
Session 2
  ↓
Relevant Context Restored
```

Эти сценарии показывают работу системы без публикации приватной codebase или production data.
