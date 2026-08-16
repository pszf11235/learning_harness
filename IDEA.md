# Learning Harness (CLI Interactive Tutor)

## Concept

A CLI-based interactive learning tool that generates structured, project-based curricula for any tech stack using LLMs. Think "Rustlings meets boot.dev meets AI tutor" — but for ANY language or framework, generated on the fly.

## Core Features

1. **Dynamic Curriculum Generation** — Tell it what you want to learn + what to build, and it generates progressive chapters with reading material, exercises, and tests
2. **Interactive CLI** — Work through chapters in your terminal. Commands like `next`, `hint`, `why`, `check`, `skip`, `status`
3. **LLM-Powered Explanations** — Ask "why does this work this way?" at any point and get contextual answers
4. **Test-Driven Validation** — Each exercise has tests that must pass. The LLM gives feedback on failures
5. **Provider Agnostic** — Works with OpenAI, Anthropic, Ollama (local), or any OpenAI-compatible API
6. **Progress Tracking** — See your learning progress, streaks, and completed chapters

## Example Usage

```bash
# Install
npm install -g learnit

# Start learning
learnit start --topic "TypeScript REST APIs with Express" --llm ollama/llama3

# Or more specific
learnit start --topic "Rust CLI tools" --project "build a todo CLI" --difficulty intermediate

# Work through it
learnit next              # show current chapter
learnit hint              # contextual help
learnit why "middleware"  # explain a concept
learnit check             # run tests on your code
learnit status            # progress dashboard
```

## Output Structure

```
.learnit/
  config.yaml
  paths/
    typescript-rest-api/
      chapter-01-setup/
        README.md          ← reading material
        exercise.ts        ← starter code with TODOs
        solution.ts        ← hidden reference solution
        test.ts            ← tests that must pass
      chapter-02-routing/
        ...
      progress.json        ← completion tracking
```

## Tech Stack

- TypeScript + Node.js
- CLI: Commander.js or Ink (React for terminals)
- LLM: Unified provider interface (OpenAI/Anthropic/Ollama)
- Testing: Spawns language-native test runners
- TUI: Ink or chalk for pretty terminal output

## Differentiators

- **Not locked to one language** — generates curricula for any tech stack
- **Project-based** — you build something real, not isolated exercises
- **AI explains the "why"** — not just "do this", but "here's why this pattern exists"
- **Local-first** — works fully offline with Ollama
- **Open source** — no $30/month subscription

## Target Users

- Developers learning a new language/framework
- Teams onboarding members to unfamiliar tech stacks
- Self-taught developers who want structured progression
- Anyone who prefers terminal over browser-based learning

## Status

📋 **Idea** — Not yet implemented
