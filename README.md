# AI Instructions and Prompts

This repository contains AI prompts, instructions, and code snippets for various AI tools and use cases.

## Directory Structure

```
.
├── prompts/           # AI prompts and instructions for various tools
├── snippets/          # Code snippets and templates
└── README.md          # This file
```

## Naming Convention

### Prompts and Instructions

Files in the `prompts/` directory follow this naming pattern:

```
<purpose>-<ai-tool>.md
```

**Examples:**
- `image-generation-gemini.md` - Image generation instructions for Gemini
- `code-examples-copilot.md` - Code example generation for GitHub Copilot
- `api-examples-copilot.md` - API example instructions for Copilot agents
- `social-media-agent.md` - Social media content generation agent
- `newsletter-tools.md` - Newsletter preparation tools and workflows

**Guidelines:**
- Use lowercase with hyphens (kebab-case)
- Purpose comes first, then the AI tool if specific to one
- Use `.md` extension for markdown files
- Be descriptive but concise

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

### prompts/

Contains AI prompts, instructions, and agent guidelines for:
- Image generation (Gemini, DALL-E, etc.)
- Code generation (GitHub Copilot, etc.)
- Content creation (social media, newsletters, etc.)
- Development workflows (TDD, API examples, etc.)

### snippets/

Contains code snippets and templates:
- VS Code snippet files (`.code-snippets.json`)
- Reusable prompt templates

## Contributing

When adding new AI instructions or prompts:

1. Choose the appropriate directory (`prompts/` or `snippets/`)
2. Follow the naming convention outlined above
3. Use descriptive, lowercase, hyphenated names
4. Include clear documentation within the file about its purpose and usage

## Usage

1. Browse the `prompts/` directory for AI instructions
2. Copy the relevant prompt or instruction to your AI tool
3. Use snippets from the `snippets/` directory in your IDE

## Examples

### Using a Prompt

```markdown
# To generate images with Gemini
1. Open prompts/image-generation-gemini.md
2. Copy the instructions
3. Paste into Gemini with your specific requirements
```

### Using Code Snippets

```markdown
# To use Copilot snippets in VS Code
1. Copy snippets/copilot-mailinator.code-snippets.json
2. Add to your VS Code user snippets
3. Trigger with the defined prefix
```
