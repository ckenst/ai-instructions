# AI Instructions and Prompts

This repository contains AI prompts, instructions, and code snippets for various AI tools and use cases, primarily focused on GitHub Copilot in VS Code.

## Directory Structure

```
.
├── .github/
│   ├── copilot-instructions.md    # Main Copilot instructions (TDD guidelines)
│   ├── prompts/                   # Copilot prompts (*.prompt.md)
│   └── instructions/              # Copilot instructions (*.instructions.md)
├── snippets/                      # Code snippets and templates
└── README.md                      # This file
```

## Naming Convention

### GitHub Copilot Files

#### `.github/copilot-instructions.md`
The main Copilot instructions file that is automatically loaded by GitHub Copilot in VS Code. Contains general development guidelines and practices (e.g., TDD rules).

**Important:** This file should not be renamed or moved.

#### `.github/prompts/`
Contains prompts to be used with GitHub Copilot Chat. These are templates you reference in conversations.

**Naming pattern:**
```
<purpose>.prompt.md
```

**Examples:**
- `blog-editor.prompt.md` - Blog post editing prompt
- `image-generation-gemini.prompt.md` - Image generation prompt for Gemini
- `social-media-content.prompt.md` - Social media content creation

**Guidelines:**
- Use lowercase with hyphens (kebab-case)
- Be descriptive about the purpose
- Use `.prompt.md` extension
- These are meant to be referenced in Copilot Chat

#### `.github/instructions/`
Contains instructions for GitHub Copilot agents and specific task guidelines.

**Naming pattern:**
```
<purpose>.instructions.md
```

**Examples:**
- `mailinator-code-examples.instructions.md` - Instructions for generating Mailinator code examples
- `mailinator-api-examples.instructions.md` - Agent guide for Mailinator API examples
- `newsletter-tools.instructions.md` - Newsletter preparation tools

**Guidelines:**
- Use lowercase with hyphens (kebab-case)
- Be descriptive about the purpose
- Use `.instructions.md` extension
- These provide detailed guidance for specific tasks or domains

### Code Snippets

Files in the `snippets/` directory follow this naming pattern:

```
<tool>-<purpose>.code-snippets.json
```

**Examples:**
- `copilot-mailinator.code-snippets.json` - VS Code snippets for Mailinator prompts

**Guidelines:**
- Use lowercase with hyphens (kebab-case)
- Tool name comes first
- Use `.code-snippets.json` extension for VS Code snippet files

## File Organization

### `.github/copilot-instructions.md`
The main instructions file that GitHub Copilot automatically reads in VS Code. Keep this focused on general development practices and coding standards.

### `.github/prompts/`
Prompts for various AI tools (Copilot, Gemini, etc.) that can be referenced in conversations:
- Image generation prompts
- Content creation prompts
- Blog editing prompts
- Social media content generation

### `.github/instructions/`
Detailed instructions and agent guidelines for specific tasks:
- API example generation
- Code example patterns
- Tool-specific workflows
- Domain-specific guidance

### `snippets/`
Code snippets and templates for VS Code:
- Snippet files (`.code-snippets.json`)
- Reusable prompt templates

## Contributing

When adding new AI instructions or prompts:

1. **For general Copilot guidelines:** Edit `.github/copilot-instructions.md`
2. **For prompts:** Add to `.github/prompts/` with `.prompt.md` extension
3. **For task instructions:** Add to `.github/instructions/` with `.instructions.md` extension
4. **For code snippets:** Add to `snippets/` with `.code-snippets.json` extension
5. Follow the naming conventions outlined above
6. Use descriptive, lowercase, hyphenated names
7. Include clear documentation within the file about its purpose and usage

## Usage

### Using GitHub Copilot Instructions

The `.github/copilot-instructions.md` file is automatically loaded by GitHub Copilot in VS Code. It contains general guidelines that Copilot follows while assisting you.

### Using Prompts with Copilot Chat

1. Browse `.github/prompts/` for available prompts
2. Reference them in Copilot Chat conversations
3. Example: "Follow the guidelines in .github/prompts/blog-editor.prompt.md to review my blog post"

### Using Instructions Files

1. Browse `.github/instructions/` for task-specific guidance
2. Reference them when working on specific tasks
3. Example: "Use .github/instructions/mailinator-code-examples.instructions.md to generate a code sample"

### Using Code Snippets

1. Copy snippet files from `snippets/` directory
2. Add to your VS Code user snippets or workspace snippets
3. Trigger with the defined prefix while coding

## Examples

### Referencing a Prompt in Copilot Chat

```markdown
Follow the rules in .github/prompts/image-generation-gemini.prompt.md 
and create an image description for my blog post about testing.
```

### Using Instructions for Code Generation

```markdown
Follow the rules in .github/instructions/mailinator-code-examples.instructions.md 
and generate a single-file JavaScript demo that fetches inbox messages. 
Name the file fetch-messages-demo.js.
```

### Adding Custom Snippets to VS Code

```markdown
1. Open VS Code settings
2. Go to File > Preferences > Configure User Snippets
3. Select your language (e.g., "markdown")
4. Copy content from snippets/copilot-mailinator.code-snippets.json
5. Save and use the snippet prefix to trigger it
```
