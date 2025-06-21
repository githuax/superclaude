# SuperClaude

[![npm version](https://badge.fury.io/js/superclaude.svg)](https://badge.fury.io/js/superclaude)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

🚀 **Give Claude superpowers for GitHub workflows.** Transform your development process with AI-powered commit messages, intelligent changelogs, automated documentation, and code reviews that actually understand your codebase.

## Quick Install

```bash
npm install -g superclaude
```

**Prerequisites:** Node.js 18+, Git, [Claude Code](https://www.anthropic.com/claude-code), and optionally [GitHub CLI](https://cli.github.com/).

## Quick Start

```bash
cd your-project
superclaude commit          # AI generates perfect commit messages
superclaude changelog       # Creates intelligent project history
superclaude readme          # Writes comprehensive documentation
```

## Commands

### 🤖 `superclaude commit`
**AI-powered commits that actually make sense.**

Analyzes your git changes, understands the context, and generates conventional commit messages. No more "fix stuff" or "update files" - get meaningful commits that tell the story of your code.

```bash
superclaude commit                    # Quick AI commit
superclaude commit --interactive      # Review before committing  
superclaude commit --verbose          # See the AI thinking process
```

**How it works:**
- Scans all changed files and understands the modifications
- Analyzes code patterns to determine commit type (feat/fix/refactor/etc.)
- Generates conventional commit format with clear descriptions
- Automatically stages, commits, and pushes to your current branch

### 📅 `superclaude changelog`
**Turn raw commit history into readable project stories.**

Creates human-readable changelogs that focus on user impact, not technical noise. Generates daily, weekly, and monthly summaries that actually make sense to stakeholders.

```bash
superclaude changelog                 # Generate intelligent changelog
superclaude changelog --verbose       # See detailed analysis process
```

**How it works:**
- Analyzes entire commit history with AI understanding
- Filters out trivial changes, focuses on meaningful updates  
- Groups changes by time periods and impact
- Creates multiple changelog formats (daily/weekly/monthly)
- Writes in clear, non-technical language

### 📖 `superclaude readme`
**Professional documentation that writes itself.**

Analyzes your codebase architecture and creates comprehensive README files with installation guides, usage examples, and feature descriptions.

```bash
superclaude readme                    # Generate project README
```

**How it works:**
- Scans project structure and identifies key technologies
- Analyzes package.json and dependencies
- Understands code patterns and project purpose
- Creates professional documentation with examples
- Includes installation, usage, and contribution guides

### 🔍 `superclaude review`
**Code reviews that catch what humans miss.**

Performs deep code analysis for security vulnerabilities, performance issues, and maintainability problems. Provides actionable recommendations for improvement.

```bash
superclaude review                    # Comprehensive code analysis
superclaude review --verbose          # Detailed security assessment
```

**How it works:**
- Analyzes entire codebase for patterns and anti-patterns
- Identifies security vulnerabilities and performance bottlenecks
- Evaluates code quality and maintainability metrics
- Provides specific, actionable improvement recommendations
- Saves detailed review to `docs/code-review.md`

### 📚 `superclaude docs`
**Technical documentation that developers actually read.**

Creates comprehensive technical guides covering architecture, components, deployment, and troubleshooting.

```bash
superclaude docs                      # Generate technical documentation
```

**How it works:**
- Maps project architecture and component relationships
- Documents data flow and system interactions
- Creates deployment and configuration guides
- Includes troubleshooting and debugging information
- Saves to `docs/technical-docs.md`

### 💡 `superclaude brainstorm`
**AI-powered feature ideation and improvement suggestions.**

Analyzes your codebase capabilities and suggests new features, optimizations, and architectural improvements.

```bash
superclaude brainstorm                # Get improvement ideas
```

**How it works:**
- Evaluates current codebase capabilities and patterns
- Identifies optimization opportunities and technical debt
- Suggests new features based on project direction
- Recommends architecture evolution strategies
- Saves ideas to `docs/ideas.md`

### 📝 `superclaude annotate`
**Add intelligent context to your entire git history.**

Analyzes every commit in your repository and adds AI-generated notes that explain what each change actually accomplished.

```bash
superclaude annotate                  # Add AI notes to all commits
superclaude annotate --verbose        # See annotation process
```

**How it works:**
- Processes each commit's diff and understands changes
- Generates detailed technical explanations
- Adds git notes with context and purpose
- Creates searchable commit history
- View with `git log --show-notes`

## Project Integration

Add to your `package.json` for team workflows:

```json
{
  "scripts": {
    "commit": "superclaude commit --interactive",
    "release:prep": "superclaude changelog && superclaude readme",
    "code:review": "superclaude review --verbose",
    "docs:update": "superclaude docs"
  }
}
```

## Why SuperClaude?

### 🎯 **Intelligent, Not Automated**
Unlike simple automation tools, SuperClaude understands your code context. It reads your entire codebase, understands patterns, and generates content that makes sense for your specific project.

### 🚀 **GitHub + Claude = Superpowers** 
Combines Claude's deep reasoning with GitHub workflows. Get AI that understands not just syntax, but intent, architecture, and user impact.

### ⚡ **Saves Hours, Not Minutes**
- **Commit messages**: From 30 seconds to instant, every time
- **Changelogs**: From hours of manual work to 2 minutes
- **Documentation**: From days of writing to comprehensive docs in minutes
- **Code reviews**: Catch issues before they become problems

### 🧠 **Context-Aware AI**
- Understands your project's tech stack and patterns
- Maintains consistency with your existing code style
- Focuses on user impact, not just technical changes
- Learns from your codebase structure and conventions

## Examples

### Daily Workflow
```bash
# Make some changes
echo "new feature" >> src/feature.js

# AI commit with perfect message
superclaude commit
# ✅ Output: "feat: add user authentication with JWT tokens"

# Update documentation automatically  
superclaude readme
# ✅ Creates professional README with new feature documented

# Prepare for release
superclaude changelog
# ✅ Generates release notes that stakeholders actually understand
```

### Team Workflow
```bash
# Before standups - get project insights
superclaude brainstorm
# ✅ "Here are 8 improvement opportunities based on your codebase..."

# Before releases - comprehensive preparation
yarn release:prep
# ✅ Updated changelog + README + documentation

# Before code reviews - AI pre-screening
superclaude review
# ✅ "Found 3 security issues and 5 performance optimizations..."
```

## Installation Details

### Prerequisites
Install these first:
```bash
# Required
npm install -g @anthropic-ai/claude-code
# Then run: claude (and complete authentication)

# Recommended  
brew install gh          # GitHub CLI for enhanced workflows
gh auth login           # Authenticate with GitHub
```

**System Requirements:** Node.js 18+, Git configured with user info.

> 💡 **Authentication Tip:** When running `gh auth login`, choose **SSH** over HTTPS. SSH is more secure, eliminates password prompts, and provides seamless authentication for all git operations. If you don't have SSH keys, GitHub CLI can generate them for you automatically.

## Troubleshooting

### Common Issues

**Command not found**
```bash
npm install -g superclaude
# Ensure npm global bin is in your PATH
```

**Claude Code not authenticated**
```bash
claude
# Follow authentication prompts (Console/Pro/Enterprise)
```

**Git not configured**
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

**GitHub CLI issues (optional)**
```bash
brew install gh         # macOS recommended
gh auth login          # Authenticate with GitHub
```

### Debug Mode
Use `--verbose` for detailed output:
```bash
superclaude commit --verbose
# Shows step-by-step AI reasoning and git operations
```

### Getting Help
- Run `superclaude help` for command reference
- Check [Claude Code docs](https://www.anthropic.com/claude-code)
- Open issues on [GitHub](https://github.com/your-username/superclaude)

## Contributing

1. Fork the repository
2. Make your changes  
3. Use SuperClaude to commit: `superclaude commit --interactive`
4. Submit a pull request

## License

MIT License - see LICENSE file.

---

**Made with ❤️ and AI** - SuperClaude transforms your development workflow by giving Claude deep understanding of your GitHub projects. 