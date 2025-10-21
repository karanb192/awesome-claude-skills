# Contributing to awesome-claude-skills

First off, thank you for considering contributing to awesome-claude-skills! It's people like you that make this resource valuable for the Claude community.

## Table of Contents

- [How Can I Contribute?](#how-can-i-contribute)
- [Adding a New Skill](#adding-a-new-skill)
- [Skill Quality Criteria](#skill-quality-criteria)
- [Skill Format Requirements](#skill-format-requirements)
- [Category Guidelines](#category-guidelines)
- [Style Guide](#style-guide)
- [Pull Request Process](#pull-request-process)
- [Code of Conduct](#code-of-conduct)

## How Can I Contribute?

### Adding a New Skill

We're always looking for new skills to add to the list! Here's how:

1. **Fork this repository**
   ```bash
   # Click the "Fork" button on GitHub
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/karanb192/awesome-claude-skills.git
   cd awesome-claude-skills
   ```

3. **Create a branch**
   ```bash
   git checkout -b add-skill-name
   ```

4. **Add your skill** to the appropriate category in `README.md`

5. **Commit your changes**
   ```bash
   git add README.md
   git commit -m "Add [skill-name] to [category]"
   ```

6. **Push to your fork**
   ```bash
   git push origin add-skill-name
   ```

7. **Submit a Pull Request**

### Other Ways to Contribute

- **Improve descriptions** - Make skill descriptions clearer and more helpful
- **Add usage examples** - Show how to use specific skills effectively
- **Fix broken links** - Report or fix skills that are no longer maintained
- **Suggest new categories** - Propose better organization schemes
- **Report issues** - Found a problem? Open an issue!
- **Share your experience** - Add "Pro Tips" or "Common Pitfalls" sections

## Skill Quality Criteria

All submitted skills must meet these quality standards:

### Required ✅

- **Working `SKILL.md` file** - Must have valid YAML frontmatter and markdown content
- **Clear documentation** - Purpose, usage, and benefits must be obvious
- **Claude Code relevance** - Specifically useful for CLI development workflows
- **Active maintenance** - Repository shows commits within the last 6 months
- **Open source** - Publicly accessible on GitHub (or similar)
- **No malicious code** - Code reviewed for security issues and harmful patterns

### Bonus Points ⭐

- **Real-world usage** - Demonstrated use by actual developers
- **Good test coverage** - If skill includes code, it should have tests
- **Comprehensive README** - Installation instructions, examples, troubleshooting
- **Multiple contributors** - Community involvement indicates quality
- **GitHub stars** - Popular skills are usually higher quality

## Skill Format Requirements

### Basic Structure

Each skill entry must follow this format:

```markdown
#### skill-name
**Source:** [owner/repo](https://github.com/owner/repo)
**Description:** One-sentence description of what the skill does (max 150 chars)
**Use Case:** When and why to use this skill
**Stars:** ⭐⭐⭐⭐⭐ (1-5 stars based on quality/utility)
```

### For Community-Needed Skills

If proposing a skill idea that doesn't exist yet:

```markdown
#### skill-name
**Status:** Community-needed
**Description:** What this skill should do
**Use Case:** When and why it would be useful
```

### Example

```markdown
#### test-driven-development
**Source:** [obra/superpowers](https://github.com/obra/superpowers)
**Description:** Implements the RED-GREEN-REFACTOR cycle workflow for test-driven development
**Use Case:** When building new features with strong test coverage guarantees
**Stars:** ⭐⭐⭐⭐⭐
```

## Category Guidelines

Choose the most appropriate category for your skill:

### 🧪 Testing & Quality
Skills related to testing, TDD, code quality, and validation

### 🐛 Debugging & Troubleshooting
Skills for finding and fixing bugs, performance issues, and system problems

### 🤝 Collaboration & Workflow
Skills for git workflows, code review, team collaboration, and project management

### ⚙️ Development & Architecture
Skills for building applications, system design, and architectural patterns

### 🔒 Security & Performance
Skills for security auditing, vulnerability scanning, and optimization

### 📚 Documentation & Automation
Skills for generating docs, automating workflows, and CI/CD

### 🎯 Meta Skills
Skills about creating, testing, and sharing skills themselves

**Not sure which category?** Open a draft PR and ask for guidance!

## Style Guide

### Writing Style

- **Be concise** - Descriptions should be under 150 characters
- **Be specific** - Avoid vague terms like "helps with" or "improves"
- **Use active voice** - "Implements TDD workflow" not "TDD workflow is implemented"
- **Focus on outcomes** - What does the user achieve, not just what the skill does

### Formatting

- **Skill names** - Use kebab-case: `test-driven-development`, not `Test Driven Development`
- **Bold important info** - Use **bold** for field labels like `**Source:**`
- **Links** - Always link to source repositories
- **Emojis** - Use category emojis consistently: 🧪 🐛 🤝 ⚙️ 🔒 📚 🎯

### Star Rating Guidelines

Rate skills honestly based on utility and quality:

- ⭐⭐⭐⭐⭐ - Essential, game-changing, widely used (100+ GitHub stars, proven in production)
- ⭐⭐⭐⭐ - Very useful, high quality, well-maintained (50+ stars, good documentation)
- ⭐⭐⭐ - Solid, useful for specific cases (working, maintained, clear purpose)
- ⭐⭐ - Niche use case, needs improvement (limited use, sparse docs)
- ⭐ - Experimental, early stage (beta, incomplete, proof-of-concept)

**When in doubt:** Start with ⭐⭐⭐ and adjust based on adoption and quality.

## Pull Request Process

1. **Check existing PRs** - Make sure someone hasn't already submitted the same skill

2. **Follow the format** - Use the exact format specified above

3. **One skill per PR** - Makes review easier and faster

4. **Descriptive PR title** - Use format: `Add [skill-name] to [category]`

5. **Fill out PR template** - Answer all questions in the template

6. **Be patient** - Maintainers will review as quickly as possible

7. **Respond to feedback** - Address review comments promptly

### PR Template

When you open a PR, please include:

```markdown
## Skill Information
- **Skill Name:** [name]
- **Category:** [category]
- **Repository:** [link]
- **I am the author:** [ ] Yes [ ] No

## Quality Checklist
- [ ] Has working SKILL.md file
- [ ] Clear documentation
- [ ] Active maintenance (commits in last 6 months)
- [ ] Relevant to Claude Code CLI
- [ ] No security issues
- [ ] Follows format requirements
- [ ] Alphabetically sorted within category

## Additional Context
[Any extra information about why this skill is valuable]
```

## Skill Submission Checklist

Before submitting, verify:

- [ ] Skill has been tested and works with Claude Code
- [ ] README.md entry alphabetically sorted within category (by skill name)
- [ ] All links are valid and working (test them!)
- [ ] Description is clear, concise, and under 150 characters
- [ ] Use case is specific and helpful
- [ ] Star rating is justified (1-5 stars based on utility)
- [ ] No typos or grammatical errors
- [ ] Follows markdown formatting guidelines
- [ ] Source repository has commits within last 6 months
- [ ] Skill has proper SKILL.md file with YAML frontmatter

## Code of Conduct

### Our Standards

- **Be respectful** - Treat all contributors with respect and kindness
- **Be inclusive** - Welcome contributors of all backgrounds and skill levels
- **Be constructive** - Provide helpful feedback, not just criticism
- **Be collaborative** - Work together to improve the resource
- **Be patient** - Remember that everyone is learning

### Unacceptable Behavior

- Harassment, discrimination, or personal attacks
- Trolling, insulting comments, or inflammatory language
- Spam or promotional content
- Publishing others' private information
- Any conduct that could be considered unprofessional

### Enforcement

Instances of unacceptable behavior may result in:
1. Warning from maintainers
2. Temporary ban from contributing
3. Permanent ban from the project

Report issues to the repository maintainers.

## Questions?

- **Not sure if your skill qualifies?** Open an issue and ask!
- **Need help with formatting?** Check existing skills as examples
- **Want to discuss major changes?** Open an issue first for discussion
- **Found a bug?** Open an issue with details

## Recognition

All contributors will be:
- Listed in the repository contributors page
- Credited in release notes (if applicable)
- Appreciated by the community!

---

**Thank you for contributing!** Your efforts help make Claude Code better for everyone.
