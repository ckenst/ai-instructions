# AI Instructions

A collection of AI prompts, instructions, and code snippets for various development tasks and AI-assisted coding workflows.

## Contents

This repository contains:

- **GitHub Copilot Instructions** (`.github/co-pilot-instructions.md`) - Instructions that GitHub Copilot automatically picks up in your projects
- **Prompt Templates** - Reusable prompts for various AI tools:
  - Mailinator API documentation prompts
  - Gemini image generation prompts
  - Newsletter and content generation prompts
- **Code Snippets** (`.code-snippets.json` files) - VS Code snippet collections for quickly inserting AI prompts

## Using These Instructions in Your Projects

To make code editors automatically pick up these AI instructions in your development projects, you can symlink this repository's `.github` directory into your project.

### Symlinking Instructions

#### Option 1: Symlink the Entire `.github` Directory

If your project doesn't have a `.github` directory yet:

```bash
# Navigate to your project root
cd /path/to/your/project

# Create a symlink to this repository's .github directory
ln -s /path/to/ai-instructions/.github .github
```

#### Option 2: Symlink Individual Files

If your project already has a `.github` directory, symlink individual files:

```bash
# Navigate to your project's .github directory
cd /path/to/your/project/.github

# Symlink the Copilot instructions file
ln -s /path/to/ai-instructions/.github/co-pilot-instructions.md co-pilot-instructions.md

# Symlink other prompt files as needed
ln -s /path/to/ai-instructions/.github/social-media-content.prompt.md social-media-content.prompt.md
```

#### Option 3: Copy Files (Alternative)

If you prefer not to use symlinks, you can copy files directly:

```bash
# Copy the Copilot instructions to your project
cp /path/to/ai-instructions/.github/co-pilot-instructions.md /path/to/your/project/.github/
```

### Using Code Snippets

To use the code snippet files in VS Code:

1. **User Snippets (Global):**
   - Copy the `.code-snippets.json` files to your VS Code snippets directory
   - macOS/Linux: `~/.config/Code/User/snippets/`
   - Windows: `%APPDATA%\Code\User\snippets\`

2. **Project Snippets (Local):**
   - Create a `.vscode` directory in your project root if it doesn't exist
   - Symlink or copy the snippet files:
     ```bash
     cd /path/to/your/project
     mkdir -p .vscode
     ln -s /path/to/ai-instructions/mailinator-prompt.code-snippets.json .vscode/
     ```

### Using Prompt Templates

The markdown prompt files can be referenced or copied into your own documents as templates:

- `gemini-blog-image.prompt.md` - Template for generating blog images with Gemini
- `gemini-image-generation.md` - General image generation instructions
- `mailinator-api-example-instructions.md` - Guidelines for Mailinator API examples
- `mailinator-copilot.prompt.md` - Copilot prompt for Mailinator documentation
- `tcorg-newsletter-tools.md` - Newsletter content generation tools

## Verifying Setup

After symlinking, verify the setup:

```bash
# Check that the symlink was created correctly
ls -la /path/to/your/project/.github

# You should see something like:
# co-pilot-instructions.md -> /path/to/ai-instructions/.github/co-pilot-instructions.md
```

GitHub Copilot will automatically pick up the `co-pilot-instructions.md` file when you're working in your project.

## Tips

- **Keep Instructions Updated**: Since symlinks point to the original files, any updates to this repository will automatically be reflected in your projects
- **Version Control**: Add symlinks to your `.gitignore` if you don't want to commit them to your project repository
- **Multiple Projects**: You can symlink the same instructions into multiple projects to maintain consistency across your development work
- **Editor Restart**: You may need to reload your code editor after creating symlinks for changes to take effect

## Contributing

Feel free to add your own AI prompts and instructions to this repository to build a shared collection of useful AI workflows.

## License

This is a personal collection of AI instructions and prompts. Use freely in your own projects.
