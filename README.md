# SuperClaude

[![npm version](https://badge.fury.io/js/superclaude.svg)](https://badge.fury.io/js/superclaude)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

🚀 **AI-powered development toolkit** for generating commit messages, changelogs, documentation, and code reviews using Claude AI.

## Prerequisites

Before installing SuperClaude, ensure you have:

### Required
- **Node.js 18+** - [Download Node.js](https://nodejs.org/)
- **Git** - [Install Git](https://git-scm.com/downloads)
- **Claude Code** - Install with: `npm install -g @anthropic-ai/claude-code`

### Claude Code Setup
After installing Claude Code, authenticate:
```bash
claude auth login
```

You'll need an Anthropic API key. Get one at [console.anthropic.com](https://console.anthropic.com/).

## Installation

Install SuperClaude globally:

```bash
npm install -g superclaude
```

Or with Yarn:
```bash
yarn global add superclaude
```

## Quick Start

1. Navigate to any git repository
2. Run your first AI commit:
   ```bash
   superclaude commit
   ```

That's it! SuperClaude will analyze your changes and create an intelligent commit message.

## Commands

### Core Commands

| Command | Description | Example |
|---------|-------------|---------|
| `commit` | Generate AI commit messages and push | `superclaude commit` |
| `changelog` | Create intelligent changelogs from history | `superclaude changelog` |
| `readme` | Generate comprehensive README files | `superclaude readme` |
| `review` | Perform AI code review and analysis | `superclaude review` |
| `docs` | Generate technical documentation | `superclaude docs` |
| `brainstorm` | Get AI suggestions for improvements | `superclaude brainstorm` |
| `annotate` | Add AI notes to commit history | `superclaude annotate` |
| `help` | Show detailed help information | `superclaude help` |

### Command Flags

| Flag | Short | Description |
|------|-------|-------------|
| `--verbose` | `-v` | Show detailed progress output |
| `--interactive` | `-i` | Enable interactive mode for commit confirmation |

### Usage Examples

```bash
# Basic AI commit
superclaude commit

# Commit with detailed progress
superclaude commit --verbose

# Interactive commit with confirmation
superclaude commit --interactive

# Both verbose and interactive
superclaude commit --verbose --interactive

# Generate changelog with progress details
superclaude changelog --verbose

# Generate README and save to file
superclaude readme

# Perform comprehensive code review
superclaude review --verbose

# Add AI annotations to all commits
superclaude annotate
```

## Project Integration

Add SuperClaude to your project's `package.json` for team workflows:

```json
{
  "scripts": {
    "commit": "superclaude commit",
    "commit:interactive": "superclaude commit --interactive",
    "commit:verbose": "superclaude commit --verbose",
    "changelog": "superclaude changelog",
    "readme": "superclaude readme",
    "review": "superclaude review",
    "docs": "superclaude docs",
    "brainstorm": "superclaude brainstorm"
  }
}
```

Then use with your package manager:
```bash
# With npm
npm run commit
npm run commit:interactive

# With yarn
yarn commit
yarn commit:interactive
```

## Features

### 🤖 Smart Commits
- Analyzes git changes with detailed context
- Generates conventional commit messages
- Interactive mode for review and editing
- Automatic staging, committing, and pushing

### 📅 Intelligent Changelogs
- Creates human-readable summaries (not raw commits)
- Generates daily, weekly, and monthly overviews
- Filters trivial changes, focuses on user impact
- Multiple changelog formats

### 🔍 Code Review & Analysis
- Security vulnerability assessment
- Code quality and maintainability analysis
- Actionable improvement recommendations
- Technical debt identification

### 📚 Documentation Generation
- Comprehensive README creation
- Technical documentation
- Architecture overviews
- Installation and usage guides

### 💡 AI-Powered Insights
- Feature and improvement brainstorming
- Performance optimization suggestions
- Architecture evolution recommendations
- Integration possibilities

### 📝 Commit Annotations
- AI-powered git notes
- Detailed commit explanations
- Historical context preservation

## Configuration

SuperClaude works out of the box but respects your git and Claude CLI configurations.

### Environment Variables

- `EDITOR` - Preferred editor for interactive mode (falls back to VS Code, nano, vim)
- Claude Code uses standard Anthropic environment variables

### Git Integration

SuperClaude requires a git repository and will:
- Check for uncommitted changes
- Stage all changes before committing
- Push to the current branch after committing

## Troubleshooting

### Common Issues

**"Claude Code not found"**
```bash
npm install -g @anthropic-ai/claude-code
claude auth login
```

**"Not in a git repository"**
```bash
cd your-project-directory
git init  # if needed
```

**"Nothing to commit"**
- Make some changes to your files first
- SuperClaude only commits when there are staged or unstaged changes

**Permission denied errors**
- Ensure you have write access to the repository
- Check if you need to authenticate with your git remote

### Debug Mode

Use `--verbose` flag for detailed output:
```bash
superclaude commit --verbose
```

This shows:
- Step-by-step progress
- File analysis details
- Claude AI processing status
- Git operations

### Getting Help

- Run `superclaude help` for command reference
- Check [Claude Code documentation](https://www.anthropic.com/claude-code)
- Open issues on [GitHub](https://github.com/your-username/superclaude)

## Examples

### Typical Workflow

```bash
# Make some changes to your code
echo "new feature" >> feature.js

# Generate AI commit message and push
superclaude commit

# Generate updated documentation
superclaude readme

# Create changelog for release
superclaude changelog
```

### Team Workflow

```bash
# Add to package.json scripts
{
  "scripts": {
    "commit": "superclaude commit --interactive",
    "release:docs": "superclaude readme && superclaude changelog"
  }
}

# Team members can then use
yarn commit      # Interactive AI commits
yarn release:docs # Update all documentation
```

## Contributing

SuperClaude is open source! Contributions welcome.

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Use SuperClaude to commit: `superclaude commit`
5. Submit a pull request

## License

MIT License - see LICENSE file for details.

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for version history (generated with SuperClaude itself!).

---

**Made with ❤️ and AI** - SuperClaude uses Claude AI to make development workflows smarter and more efficient. 