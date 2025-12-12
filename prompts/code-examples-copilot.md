```markdown
# Mailinator Copilot Prompt — Quick Template for generating beginner-friendly code samples

Purpose
- A reusable prompt you can reference in GitHub Copilot Chat to generate single-file, beginner-friendly Mailinator JavaScript demo scripts for the docs.

How to use (quick)
1. Reference this file from your repository at prompts/code-examples-copilot.md
2. Open GitHub Copilot Chat in VS Code and enable workspace/repository context (see instructions below).
3. In the chat input say: "Follow the rules in prompts/code-examples-copilot.md and generate a single-file JavaScript demo that <short description>. Name the file <file-name.js>."

Audience & Style
- Audience: absolute beginners. Short, plain-language comments and step-by-step explanations.
- Tone: friendly, concise, and explanatory. Avoid jargon. Explain "why" not just "what".

Rules (apply these exactly)
1. Language: JavaScript (unless requested otherwise).
2. Output: exactly one single-file script per request.
3. No external libraries — only built-in Node APIs (https, fs, fetch if Node 18+).
4. No inheritance, no dependency injection.
5. Prefer async/await; do not use callbacks for async flows.
6. Do not use environment variables; use clear constants in the file and instruct users to replace them.
7. Keep code short and simple (target ~25–80 lines).
8. Include top-of-file comments that explain prerequisites and how to run the script.
9. Inline comments: explain each non-trivial step in plain language and why it works.
10. Demonstrate only one focused feature per script (e.g., send message, list inbox).
11. Console.log example expected output or response shape.

Request template (example)
- After referencing this file in Copilot Chat, append a single-line request:
  "Generate a single-file JavaScript demo that <short description>. Name the file <suggested-filename.js> and keep it under ~80 lines."

Example usage in Copilot Chat
- "Follow the rules in prompts/code-examples-copilot.md and generate a single-file JavaScript demo that lists the 5 most recent messages in a Mailinator inbox. Name the file list-inbox-demo.js."

Notes
- If you want Copilot to read this file automatically, ensure Copilot Chat's workspace/repo context is enabled.
```
