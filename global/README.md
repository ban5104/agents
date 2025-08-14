# Minimal Agents

Philosophy: **Least code that works**

## Agents

| Agent | When | What |
|-------|------|------|
| **Feature Analyzer** | Auto (NEW features only) | Quick scan of existing code |
| **Code Architect** | Manual (`@code-architect`) | Minimal plans for complex features |
| **Implementation** | Manual only | Execute plans exactly |
| **Code Reviewer** | Auto (after changes) | Catch critical issues |
| **Code Simplifier** | Manual (`@code-simplifier`) | Reduce complexity |

## Triggering

- **Auto:** Feature Analyzer (new features), Code Reviewer (after changes)
- **Manual:** Everything else (use `@agent-name`)

## Usage

**Simple tasks:** Let Claude implement directly. Code Reviewer auto-validates.

**Complex features:** 
1. `@feature-analyzer` (if needed)
2. `@code-architect` for plan
3. `@code-implementation` to execute

**Result:** ~100 lines instead of 800+ for basic features.

## Context

Agents only see what you pass them. Descriptions control this.

**Good:** `"Review modified files. Include CLAUDE.md if exists."`
**Bad:** `"Include ALL files examined, full content..."`