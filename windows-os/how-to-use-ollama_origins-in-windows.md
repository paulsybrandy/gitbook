---
description: >-
  The direct command of "OLLAMA_ORIGINS="https://radostllm.radostit.com" ollama
  serve" does not work in Windows Terminal. This is a work-around.
---

# How to use OLLAMA\_ORIGINS in Windows

The example command of `OLLAMA_ORIGINS="https://radostllm.radostit.com" ollama serve` does not work in Windows Terminal, Command Prompt, or Powershell. However, running the following commands in Git Bash will accomplish the same result.

1. Open Git Bash.
2.  Run the first command with the word export in front of it:

    1. `export OLLAMA_ORIGINS="https://radostllm.radostit.com"`


3. Then run `ollama serve`
4. Done.

